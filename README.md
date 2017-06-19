# OYMotion Community Web Site

This web site (https://oymotion.github.io) is built upon GitHub Jekyll.

## How to Update
You can modify this web site and preview it locally before pushing it to
github. The following instructions guide you through setting up Jekyll on
Linux or [Bash on Ubuntu on Windows][BashOnUbuntuOnWindows] for Windows 10.

Open `bash`, and enter the following commands:

```
$ sudo apt install ruby
$ sudo gem install bundler
$ git clone https://github.com/oymotion/oymotion.github.io.git
$ cd oymotion.github.io
$ bundle install
$ bundle exec jekyll serve
```

Then you would be able to preview your local web site at http://localhost:4000

[BashOnUbuntuOnWindows]: https://msdn.microsoft.com/commandline/wsl/about
[Jekyll]: http://jekyllrb.com
