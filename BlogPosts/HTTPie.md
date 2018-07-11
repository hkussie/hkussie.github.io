## Using HTTPie to test RESTful API Services
---
HTTPie is a library that makes it possible to run HTTP requests from the command line. Using the HTTPie library enables us to visualize HTTP requests in an intuitive, easy to understand manner, that makes conceptualizing HTTP requests much easier to grasp.

Lets get started by importing HTTPie onto our local machine:

---
*This tutorial assumes your working on a mac, and that you have the brew installed on your local machine.*

```github
brew install httpie
```
Let's now verify that we have successfully installed HTTPie onto our local machine:

```github
http httpie.org
```
---
If installed correctly, our we should have this returned in our terminal session:

```github
http httpie.org

HTTP/1.1 301 Moved Permanently
CF-RAY: 4386fd3aa5c7bb1e-SEA
Cache-Control: max-age=3600
Connection: keep-alive
Date: Wed, 11 Jul 2018 00:00:19 GMT
Expires: Wed, 11 Jul 2018 01:00:19 GMT
Location: https://httpie.org/
Server: cloudflare
Transfer-Encoding: chunked
```
