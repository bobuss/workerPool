# WorkerPool

from: [http://marcio.io/2015/07/handling-1-million-requests-per-minute-with-golang/](http://marcio.io/2015/07/handling-1-million-requests-per-minute-with-golang/)


NB : the "heavy work" only consists of a 1 second sleep ...


## how to ?

    $ go run server.go


Then, in another terminal

    $ curl -X POST -d '{}' localhost:8080


You also can stress it with [https://github.com/rakyll/boom](boom)

    $ ./boom -c 100 -n 10000 -m POST -d '{"data": [{"waza": 1}]}' http://localhost:8080


