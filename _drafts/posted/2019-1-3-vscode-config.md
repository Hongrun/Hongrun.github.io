---
layout: post
title:  "A New Year And A New Text Editor"
tags:
  - howto
hero: https://source.unsplash.com/collection/430471/
overlay: blue
published: true

---
So, an exciting new year has started. This year, I decided to change up my programming game a little bit by switching to a new text editor -- vscode.
<!–-break-–>

Before vscode, I have always been using sublime, which is an amazing text editor. It has a lot of cool shortcuts, great plugins and a pretty interface, but there's one thing I didn't like so much, that is, it always prompts me to buy a license... Of course, I don't blame sublime for this. I should register and pay for a product I enjoy using. So here's what I will do in the future, I will keep using sublime for my own projects, but for school I will use vscode, because it is less distracting.

Since I use ssh for my school projects, I need to figure out how to configure SFTP using vscode. I used a vscode plugin called SFTP but for some reason I couldn't get it to work... but I successfully installed a similar plugin called SSH FS and it worked beautifully.

So here is how I did it.

I searched for SSH FS, installed and enabled it. Then I went to SSH FS configuration under settings and edited the settings.json. There was a user settings page, in which I could add setting snippets to override the default. So I inserted a snippet like this:

{% highlight ShellSession %}
    "sshfs.configs": [
        {
            "root": "remote_path",
            "host": "remote_host",
            "port": 22,
            "username": "myusername",
            "password": "mypassword",
            "name": "sshname"
        }
    ],
{% endhighlight %}

After saving the changes, the configuration was done. I could go to explorer (the first icon on the left panel). There would be an item under a tab called "SSH FILE SYSTEM" by the name I gave in the json file. I could right click, select "Connect as Workspace folder". The little dot in front of the ssh name would turn green and I'd see my remote folders appearing in my folder panel.

In addition, [here][macos] is a helpful guide of vscode shortcuts for MacOS, and [here][windows] for Windows users.

Happy New Year and Happy Coding!

2019.1.3

[macos]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
[windows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf