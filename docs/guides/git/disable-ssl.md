# SSL certificate errors with Git

When trying to clone a Git repository, you may encounter an error related to SSL certificate verification or HTTPS certificates. This is becuase the school network intercepts HTTPS traffic for monitoring and website blocking, and gives a self-signed certificate to client devices.

Git often rejects this certificate (but not always, somehow), which produces an error like this one:

> SSL certificate problem: self-signed certificate in certificate chain

## Reccomended fix: Disable SSL verification

Set the `http.sslVerify` Git config option to `false` by running the following command in Git Bash:

```bash
git config --global http.sslVerify false
```

This stops Git from bothering to verify the SSL certificate it recives when cloning a repository (or pushing, fetching, etc).

## Futher reading

- [Answer to 'How can I make git accept a self signed certificate?' (Stack Overflow)](https://stackoverflow.com/a/11622001)
- [SSL certificate problem: self-signed certificate in certificate chain error in GIT (Bitbucket Cloud Knowledge Base)](https://confluence.atlassian.com/bbkb/ssl-certificate-problem-self-signed-certificate-in-certificate-chain-error-in-git-1224773006.html)
- [Answer to 'How do I configure Git to trust certificates from the Windows Certificate Store?' (Stack Overflow)](https://stackoverflow.com/a/48212753)