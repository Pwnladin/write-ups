# Level 2

```sh
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level2# file leveltwo.jpeg
leveltwo.jpeg: ASCII text
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level2# cat leveltwo.jpeg
aW5mb3NlY19mbGFnaXNfd2VhcmVqdXN0c3RhcnRpbmc=
root@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level2# echo "aW5mb3NlY19mbGFnaXNfd2VhcmVqdXN0c3RhcnRpbmc=" | base64 -d
infosec_flagis_wearejuststartingroot@sanctuary:~/ctf/Infosec Institute n00bs CTF Labs/level2#
```

Another solution:

```
HTTP/1.1 200 OK
Date: Thu, 16 Apr 2015 08:16:55 GMT
Server: Apache/2.4.7 (Ubuntu)
Last-Modified: Fri, 13 Mar 2015 18:49:21 GMT
ETag: "2d-5112ff55e0058"
Accept-Ranges: bytes
Content-Length: 45
Keep-Alive: timeout=5, max=100
Content-Type: image/jpeg
Expires: Thu, 16 Apr 2015 09:15:52 GMT
Connection: keep-alive

aW5mb3NlY19mbGFnaXNfd2VhcmVqdXN0c3RhcnRpbmc=
```

> Flag: `infosec_flagis_wearejuststarting`