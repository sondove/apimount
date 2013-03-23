apimount
========

Mount restful web services over fuse...

== Dependencies ==
* Requests [https://github.com/kennethreitz/requests/]

* python-fuse

== Use ==

Specify resource to mount:

  ./apimount 'https://api.example.com' test -c ./sample.cfg

Interrogate resource using filesystem primitives:

  sondove@atlas:~/projects/apimount$ ls -l test/                                                                                         │sondove@atlas:(master)~/projects/apimount-ref$ ls                  │ 'server': 'nginx',
  total 12                                                                                                                               │apimount.conf  mydest  sample.py  test.py                          │ 'transfer-encoding': 'chunked',
  drwxrwxr-x 2 sondove sondove 4096 Mar 23 20:19 resource1                                                                               │apimount.py    ref.py  sfs.log                                     │ 'x-request-id': 'fdf516b5-7c89-4102-97d8-66457e91113c',
  drwxrwxr-x 9 sondove sondove 4096 Mar 23 20:20 resource2                                                                               │sondove@atlas:(master)~/projects/apimount-ref$ cd ..               │ 'x-response-time': '0'}
  drwxrwxr-x 2 sondove sondove 4096 Mar 23 20:19 resource3


  sondove@atlas:~/projects/apimount$ tree test/                                                                                         │sondove@atlas:(master)~/projects/apimount-ref$ ls                  │ 'server': 'nginx',
  test/
  ├── resource1
  ├── resource2
  │   ├── subres1
  │   ├── subres2
  │   ├── subres3
  │   ├── subres4
  │   ├── subres5
  │   ├── subres6
  │   └── subres7
  └── resource3
  
  10 directories, 0 files

