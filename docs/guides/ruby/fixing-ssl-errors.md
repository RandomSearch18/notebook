# Fixing SSL errors from Ruby `gem install`

When trying to install Ruby gems for developing with the Ruby programming language, you may encounter SSL verfication errors:

```none
$ gem install jekyll bundler
ERROR:  SSL verification error at depth 0: unable to get local issuer certificate (20)
ERROR:  You must add /C=EN/CN=senso cloud 3 to your local trusted store
ERROR:  SSL verification error at depth 0: unable to get local issuer certificate (20)
ERROR:  You must add /C=EN/CN=senso cloud 3 to your local trusted store
ERROR:  SSL verification error at depth 0: unable to get local issuer certificate (20)
ERROR:  You must add /C=EN/CN=senso cloud 3 to your local trusted store
ERROR:  Could not find a valid gem 'jekyll' (>= 0), here is why:
          Unable to download data from https://rubygems.org/ - SSL_connect returned=1 errno=0 state=error: certificate verify failed (unable to get local issuer certificate) (https://rubygems.org/specs.4.8.gz)
```

## The fix

Edit the `.gemrc` file in your home directory, e.g. with PowerShell:

```ps
notepad.exe H:\.gemrc
```

Or with Git Bash:

```bash
micro ~/.gemrc
```

And add this line:

```ruby
:ssl_verify_mode: 0
```

Some SSL verfication errors will still be printed, but they won't stop the installation from completing.

## Sources

- [Answer to 'How to tell gem command not to use SSL' (Stack Overflow)](https://stackoverflow.com/a/54988565)
