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
---
Now that we have HTTPie installed and working properly within our command line, we can start making HTTP requests. Let's start with a POST request:

```github
 http -f POST example.org message=MyFirstMessage!
```
If successful, this should be the output in the terminal:

```github
HTTP/1.1 200 OK
Accept-Ranges: bytes
Cache-Control: max-age=604800
Content-Encoding: gzip
Content-Length: 606
Content-Type: text/html
Date: Wed, 11 Jul 2018 21:57:04 GMT
Etag: "1541025663+gzip"
Expires: Wed, 18 Jul 2018 21:57:04 GMT
Last-Modified: Fri, 09 Aug 2013 23:54:35 GMT
Server: EOS (vny006/0450)
Vary: Accept-Encoding

<!doctype html>
<html>
<head>
    <title>Example Domain</title>

    <meta charset="utf-8" />
    <meta http-equiv="Content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <style type="text/css">
    body {
        background-color: #f0f0f2;
        margin: 0;
        padding: 0;
        font-family: "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;

    }
    div {
        width: 600px;
        margin: 5em auto;
        padding: 50px;
        background-color: #fff;
        border-radius: 1em;
    }
    a:link, a:visited {
        color: #38488f;
        text-decoration: none;
    }
    @media (max-width: 700px) {
        body {
            background-color: #fff;
        }
        div {
            width: auto;
            margin: 0 auto;
            border-radius: 0;
            padding: 1em;
        }
    }
    </style>    
</head>

<body>
<div>
    <h1>Example Domain</h1>
    <p>This domain is established to be used for illustrative examples in documents. You may use this
    domain in examples without prior coordination or asking for permission.</p>
    <p><a href="http://www.iana.org/domains/example">More information...</a></p>
</div>
</body>
</html>
```
---
We can also make mock file upload/download using HTTPie as follows:

```github
$ http example.org < package-lock.json

HTTP/1.1 200 OK
Accept-Ranges: bytes
Cache-Control: max-age=604800
Content-Encoding: gzip
Content-Length: 606
Content-Type: text/html
Date: Wed, 11 Jul 2018 23:22:45 GMT
Etag: "1541025663+gzip"
Expires: Wed, 18 Jul 2018 23:22:45 GMT
Last-Modified: Fri, 09 Aug 2013 23:54:35 GMT
Server: EOS (vny006/0450)
Vary: Accept-Encoding

<!doctype html>
<html>
<head>
    <title>Example Domain</title>

    <meta charset="utf-8" />
    <meta http-equiv="Content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <style type="text/css">
    body {
        background-color: #f0f0f2;
        margin: 0;
        padding: 0;
        font-family: "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;

    }
    div {
        width: 600px;
        margin: 5em auto;
        padding: 50px;
        background-color: #fff;
        border-radius: 1em;
    }
    a:link, a:visited {
        color: #38488f;
        text-decoration: none;
    }
    @media (max-width: 700px) {
        body {
            background-color: #fff;
        }
        div {
            width: auto;
            margin: 0 auto;
            border-radius: 0;
            padding: 1em;
        }
    }
    </style>    
</head>

<body>
<div>
    <h1>Example Domain</h1>
    <p>This domain is established to be used for illustrative examples in documents. You may use this
    domain in examples without prior coordination or asking for permission.</p>
    <p><a href="http://www.iana.org/domains/example">More information...</a></p>
</div>
</body>
</html>
```
Download files:

```github
http example.org/file > file
```
which will be saved onto your local machine, (assuming it's executed properly).

---
There are many other operations that can be performed using the HTTPie library, all of which can play a critical role in back-end  development and learning the fundamental concepts surrounding HTTP protocol. 
