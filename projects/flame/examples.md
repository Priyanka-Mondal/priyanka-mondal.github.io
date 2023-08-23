---
title: Flame Examples
layout: gridlay
sitemap: false
permalink: projects/flame/examples
---

We maintain a repository of useful and illustrative examples of the Flame applications in the repo 
       [flame-examples](https://bitbucket.org/decenters/flame-examples)

## Information Flow Control for REST-style Web Applications

  Web applications often store data for multiple users in
  a single data structure. While convenient, implementation
  errors could lead to information leaks.  Labeling each
  user's data with information flow policies and enforcing
  information flow control with Flame eliminates such errors
  by construction.  We took an existing <a
  href="https://github.com/krdlab/examples/tree/master/haskell-servant-webapp">
  Servant REST webapp</a> for storing and retrieving memos,
  added support for multiple users, and enforced information
  flow control to ensure only the user possessing a secret key
  may create, read, or delete the associated memos.
  </p>
  
  <p>
  Instructions:
<pre>
  > git clone https://bitbucket.org/decenters/flame-examples
  > cd flame-examples/memodb
  > stack build :memodb-server
  > stack exec memodb-server
</pre>
	  Then, from the command line, use curl to interact with the REST api:
<pre style="white-space:pre-wrap; word-wrap:break-word;">
  > curl http://localhost:8080/memos
  Missing auth header
  > curl -H "servant-auth-cookie:key1" \
         -H "Content-type: application/json" \
         -d '{"memo":"Flame rocks!" }' http://localhost:8080/memos
  > curl -H "servant-auth-cookie:key1" http://localhost:8080/memos
  [{"createdAt":"2017-09-14T19:24:17.720088Z","text":"Flame rocks!","id":1}]
</pre>
	  </p>

	  <p>
	  You can also use a sample webage that embeds Javascript that uses this API. First, browse to <a href="http://localhost:8080"><tt>http://localhost:8080</tt></a>.
	  Entering a valid secret key (try <tt>key1</tt>, <tt>key2</tt>, or <tt>key3</tt>) will list the memos for that user allow you to enter new ones.
          <center><image src="images/memodb.png"/></center>
	  </p>
	  <p>Finally, you can try a Flame-enabled Servant client:
<pre style="white-space:pre-wrap; word-wrap:break-word;">
  > stack build :memodb-client
  > stack exec memodb-client
  GET key1 before POST: []
  GET key1 after POST: [Memo {id = 1, text = "Try Flame and Servant!", createdAt = 2017-09-14 21:07:31.325636 UTC}]
</pre>
          A big advantage of this approach is that
          <code>memodb-client</code> and <code>memodb-server</code>
          link against the same API specification, ensuring that the same
          security policies are enforced on the client and the server.
        </p> 
        <h1 id="nmifc">Nonmalleable Information Flow Control for Basic Authentication</h1>
         
	  <p><a href="/publications/2017-10-02-nmifc.html">Nonmalleable information flow control</a> (NMIFC)
             enforces security for programs that <em>downgrade</em> confidentiality and integrity policies. 
             Like robust declassification, nonmalleability prevents attackers from controlling what information
             is declassified by a program.  NMIFC goes further to prevent attackers from leveraging endorsements
             to influence declassifications or manipulate confidential data.  </p>
         
          <p> NMIFC is useful for authentication mechanisms since they inherently require endorsement and declassification: 
             the result of an authentication attempt is public and trustworthy, despite having a secret dependency (the password or other secret authentication data) and an
             untrustworthy dependency (the password guess). 
          </p>
          <p> To demonstrate how Flame can be used to enforce NMIFC for authentication mechanisms, we have 
              implemented a <a href="https://www.ietf.org/rfc/rfc2617.txt">Basic Authentication</a>
              module for the Servant web application framework. We used this module to provide a new authentication to our
              <a href="#ifcapps">multi-user memo app</a>.
              <center><image src="images/nmauthdemo.png"/></center>
          </p>
	  <p>
	  Instructions:
<pre>
  git clone https://bitbucket.org/decenters/flame-examples
  cd flame-examples/memodb
  stack build :nmauthdemo
  stack exec nmauthdemo
</pre>
          Then, browse to <a href="http://localhost:8080"><tt>http://localhost:8080</tt></a>. You can use username "alice" and password "12345" to log in.
          <em>Hint: your browser may cache your authentication credentials, so try opening the page in a private browsing session if you want to try logging in multiple times.</em>
	  </p>
        <h1 id="macaroons">Flow-safe Decentralized Authorization with Macaroons</h1>
          <p><a href="https://research.google.com/pubs/pub41892.html">Macaroons</a> are authentication tokens like cookies, but may contain more sophisticated 
             <em>caveats</em> that constrain the authority of the token to access resources or perform actions. 
          </p>
          <p>
	  Instructions:
<pre>
  > git clone https://bitbucket.org/decenters/flame-examples
  > cd flame-examples/memodb-macaroons
  > stack build :memodb-macaroons
  > stack exec memodb-macaroons
  alice's macaroon:MDAxM2xvY2F0...
</pre>
	  Then, from the command line, use curl to interact with the REST api:
<pre style="white-space:pre-wrap; word-wrap:break-word;">
  > curl http://localhost:8080/memos
  Missing auth header
  > curl -H "servant-auth-macaroon:MDAxM2xvY2F0..." \
         -H "Content-type: application/json" \
         -d '{"memo":"Flame rocks!" }' http://localhost:8080/memos
  > curl -H "servant-auth-macaroon:MDAxM2xvY2F0..." http://localhost:8080/memos
  [{"createdAt":"2017-09-14T19:24:17.720088Z","text":"Flame rocks!","id":1}]
</pre>
	  </p>

        </div> <!-- intro -->
      </div>
   </div>
<!-- Global Site Tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-32820411-2"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments)};
  gtag('js', new Date());

  gtag('config', 'UA-32820411-2');
</script>
  </body>
</html>
