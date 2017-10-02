[![](https://images.microbadger.com/badges/image/burgerdev/git.svg)](https://microbadger.com/images/burgerdev/git "MicroBadger")

# Docker-Git

A simple dockerized git daemon. Usage:

```bash
mkdir -p /tmp/git
git init --bare /tmp/git/foo.git
touch /tmp/git/foo.git/git-daemon-export-ok
docker run -d -v /tmp/git:/srv/git:ro -p 9418:9418 burgerdev/git
```

# References

The [git book](https://git-scm.com/book/en/v2/Git-on-the-Server-Git-Daemon)
provides more details on how to set up the git daemon.
