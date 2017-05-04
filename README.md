# Erlang on Alpine Linux with libphonenumber

This Dockerfile provides a full installation of Erlang on Alpine with libphonenumber, intended for running Erlang releases. This Erlang installation can manage NIFs.

## Usage

NOTE: This image sets up a `default` user, with home set to `/opt/app` and owned by that user. The working directory
is also set to `$HOME`. It is highly recommended that you add a `USER default` instruction to the end of your
Dockerfile so that your app runs in a non-elevated context.

To boot straight to a prompt in the image:

```
$ docker run --rm -it --user=root fabienhenon/alpine-erlang-libphonenumber erl
Erlang/OTP 19 [erts-8.2.1] [source] [64-bit] [smp:4:4] [async-threads:10] [hipe] [kernel-poll:false]

Eshell V8.2.1  (abort with ^G)
1>
BREAK: (a)bort (c)ontinue (p)roc info (i)nfo (l)oaded
       (v)ersion (k)ill (D)b-tables (d)istribution
a
```

Tags have been added for different Erlang versions.
You will also find a libphonenumber branch which installs the libphonenumber library to the system

## License

MIT
