
# Setting up your machine


![computer party](https://media.giphy.com/media/5yLgoccfChz3fX9oHaU/giphy.gif)

_Let's get this party started / computer ready_


# Setup

Link to this doc: [http://bit.ly/computer-setup](http://bit.ly/computer-setup)

Adopted from NPR's guide: [http://blog.apps.npr.org/2013/06/06/how-to-setup-a-developers-environment.html](http://blog.apps.npr.org/2013/06/06/how-to-setup-a-developers-environment.html)


## For your machine generally


### Developer tools

With the release of macOS 10.9, Apple decoupled its command line tools necessary for compiling some of the tools we use from Xcode, Apple's proprietary development suite.

All Macs come with an app called "Terminal." You can find it under Applications > Utilities.

Additionally, you should go to your App Store and download and install `XCode Developer Tools`.

Then find your Terminal (often easiest way to do this is to search for it in your Spotlight Search in the right upper corner of your Mac) and run this command:

```
xcode-select --install
```

Once you've done all that, you can run this command to check whether everything worked out:
```
xcode-select -p
```

If you get:
```
/Library/Developer/CommandLineTools
```

everything is installed.

If you want to know if you may have previously installed the full Xcode package, you can check by typing in Terminal:

```
xcode-select -p
```

If you see:
```
/Applications/Xcode.app/Contents/Developer
```
the full Xcode package is already installed.






### Homebrew

[Homebrew](http://brew.sh/) is like the Mac app store for programming tools. You can access Homebrew via the terminal, ([like all good things](http://www.amazon.com/Beginning-was-Command-Line-Neal-Stephenson/dp/0380815931)). Inspiration for this section comes from Kenneth Reitz's excellent [Python guide](http://docs.python-guide.org/en/latest/starting/install/osx/).

Install Homebrew by pasting this command into your terminal and then hitting "enter."

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


It will ask for your password, so type that in and hit "enter" again. Now, paste this line to test Homebrew.

```
brew doctor
```


This will test your Homebrew setup, and any tools you've installed to make sure they're working properly. If they are, Homebrew tell you

```
Your system is ready to brew.
```


If anything isn't working properly, follow their instructions to get things working correctly.

Note: If there are two lines inside any of the code blocks in this article, paste them separately and hit enter after each of them.

Next you'll need to go in and edit ~/.bash_profile to ensures you can use what you've just downloaded. `bash_profile` acts like a configuration file for your terminal.

_Note: There are many editors available on your computer. You can use a pretty graphical editor like [SublimeText2](http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%202.0.1.dmg) or you can use one built-in to your terminal, like [vim](http://www.vim.org/docs.php) or [nano](http://www.nano-editor.org/dist/v2.2/nano.html). We'll be using nano for this tutorial just to keep things simple._

Open your bash_profile with the following command.

```
nano ~/.bash_profile
```


Then copy and paste this line of code at the very top. This lets Homebrew handle updating and maintaining the code we'll be installing.

```
export PATH=/usr/local/bin:$PATH
```


Once you've added the line of code, you can save the file by typing control + O. Doing so lets you adjust the file name. Just leave it as is, then hit enter to save. Hit control + X to exit. You'll find yourself back at the command line and needing to update your terminal session like so. Copy and paste the next line of code into your terminal and hit enter.

```
source ~/.bash_profile
```


You'll only need to source the bash_profile since we're editing the file right now. It's the equivalent of quitting your terminal application and opening it up again, but source lets you soldier forward and setup Python.


### Set up SSH for Github

Github has written a great guide for setting up SSH authentication for Github. You will want to do this so Github knows about your computer and will allow you to push to repositories you have access to.

Read that tutorial [here](https://help.github.com/articles/generating-ssh-keys). Do not download the native app. Start at "Step 1: Check for SSH keys".

Configure the default identity

It's nice to have your name and email show up correctly in the commit log. To make sure this information is correct, run:


```
git config --global user.email "$YOUR_EMAIL@npr.org"
git config --global user.name "$YOUR_NAME"
```



### Text editors — Atom

While I prefer vim (see below) as my editor of choice, many people prefer an editor that is less dependent on memorizing keystrokes and has a user interface that you can interact with using your mouse or trackpad. If this is you, [Atom](https://atom.io/) is a good choice because it's free and intuitive to use with its defaults, yet highly customizable.

I have this installed on my system in case I'm pairing with someone who's not familiar with vim.


## For Python


### Python

Python comes with every Mac, for others use. If you don't already have Python installed, start by getting [Python up and running](http://docs.python-guide.org/en/latest/starting/installation/).

There are two versions, Python 2 and Python 3. Mac's usually come with Python 2 but we'll be using Python 3. Since we have Homebrew, you can type into your command line interface:
```
brew install python3
```

Now let’s confirm which version was installed:
```
python3 --version
```
The result should be:
```
Python 3.7.0
```
### Pip

Installing with get-pip.py
To install pip, securely download get-pip.py:

```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

As when running any script downloaded from the web, ensure that you have reviewed the code and are happy that it works as you expect. Then run the following:

```
python get-pip.py
```
