apimount
========

Mount restful web services over fuse...

## Dependencies
* Requests [https://github.com/kennethreitz/requests/]

* python-fuse

## Use

Specify resource to mount:

```bash
  ./apimount 'https://api.example.com' test -c ./sample.cfg
```

Interrogate resource using filesystem primitives:

```bash
  sondove@atlas:~/projects/apimount$ ls -l test/
  total 12
  drwxrwxr-x 2 sondove sondove 4096 Mar 23 20:19 resource1
  drwxrwxr-x 9 sondove sondove 4096 Mar 23 20:20 resource2
  drwxrwxr-x 2 sondove sondove 4096 Mar 23 20:19 resource3

  sondove@atlas:~/projects/apimount$ tree test/
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
```
