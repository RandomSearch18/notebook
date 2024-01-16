# Disabling SSL verification in Git

When trying to clone a Git repository, you may encounter an error related to SSL certificate verification or HTTPS certificates. This is becuase of the school network's setup that intercepts HTTPS traffic.

## Quick fix

Set the `http.sslVerify` Git config option to `false` by running the following command in Git Bash:

```bash
git config --global http.sslVerify false
```

## More info

- https://stackoverflow.com/a/11622001
