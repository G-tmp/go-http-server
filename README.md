# go-http-server

 A tiny http server map local files

 ```go run main.go [-p] [-d]```



## dev

* go version go1.22.1 linux/amd64

* detect files mime type ```github.com/gabriel-vasile/mimetype```

* MultipartReader support large size and multi-part upload 



## Encountered Problems

* fmt.Fprintf() and w.Write() do not flush content, response body may be empty

* http.DetectContentType() unable to detect flac 

* if err ==  no work, use Errors.Is() instead

* http.Error() delete content-type filed, so it detect content-type automatically

* URL en/decode ```url.PathUnescape(r.URL.EscapedPath()) & url.PathEscape()```

* https://stackoverflow.com/questions/51359930/sorting-strings-with-numbers-in-filenames-with-golang