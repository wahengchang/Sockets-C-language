# Sockets in C language


## compile

```
$ cc server.c -o server 
$ cc client.c -o client
```

## run

```
//1234 port
$ ./server 1234 


$ ./client localhost 1234 
```


## Knowledge 
1. *int socket(int domain, int type, int protocol)*
    - to create a network endpoint, and it returns a socket descriptor
    - return **-1** if there is an error
2. int bind(int sockfd, struct sockaddr *my_addr, socklen_t addrlen)
    - to bind the socket to a given address once the socket is created.
3. *int listen(int s, int backlog)*
    - ready to accept connections
4. int accept(int s, struct sockaddr *addr, socklen_t *addrlen)
    - actually accept and handle connection requests 
    - it runs in an endless loop
    - is a blocking function
