---
layout: post
title:  "Welcome! and How I Built This Blog"
tags:
  - jekyll
hero: https://source.unsplash.com/collection/430471/
overlay: red
published: true

---
I am very excited to start this blog just before my 20th birthday. I have been a programmer for a year and a half now. My journey into programming has not been easy, but definitely rewarding and enjoyable. I liked it so much that I decided to start writing about it and share it with the world.
{: .lead}
<!–-break-–>

This blog is built using a [jekyll template][jekyll_template] I found on github. This template is perfect for me because it has both blog and resume features, which is exactly what I want. It's also so pretty!! Now, how did I make it my own? To my surprise, it's not a hussle at all.

Our first step is to host the template onto our domain on `github.io` and it is unbelievably simple:

1. Clone the [repository][repository] to your own github account. Make a new branch from `master` and name it `gh_pages`. Make `gh_pages` your default branch.
2. In the branch you just made, edit the `_config.yml` file. Change the baseurl to the empty string "" and the url to `https://your-github-username.github.io`. Commit your changes.
3. Delete the old `master` branch and make a new one from `gh_pages`. Change the default to your new 'master' branch.

Now you should be able to see the template website from `https://your-github-username.github.io`. So exciting!

Next, we want to be able to edit the template to make it our own. We want to make a local repository, use a local server to test our website so that we can edit, maintain and debug locally.

1. Install a ruby environment on your machine. If you have a Windows machine, follow this [tutorial][tutorial] to install ruby. If you have a Mac (like I do), you should have a ruby installed in your system. However, this version of ruby is for MacOS's own use, which means you will not have access to use it to install gems. Of course, you can forcefully do so through the system version of ruby via `sudo` but this is very unsafe. A better option is to head over to install your version of ruby. A great tool for managing multiple versions of ruby is rbenv and you can find an installation guide [here][here].
2. We have to install jekyll and bundler on our non-system version of ruby. Open a terminal, run 
```markdown
$ gem install jekyll
$ gem install jekyll bundler
```
3. Clone your repository to your machine into a location on your machine.
4. `cd` into the local repository you just created and run 
```markdown
$ bundle install
```
to install all the dependencies stated in the Gemfile.
5. Serve your website by running 
```markdown
$ bunlde exec jekyll serve
```
Now you should see something like this on your command line:
```markdown
Configuration file: ...
            Source: ...
       Destination: ...
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.815 seconds.
 Auto-regeneration: enabled for '...'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```
6. Open your favorite web browser and enter the server address as shown above into as a url. If successful, you should see your webpage showing up.
7. To edit content in the template, read all the blog posts in the template blog as well as README.md for information on how to do so.

Lastly, initialize a github repository in our folder for use of version control so that you are able to commit changes to your online repository and see your changes on your website hosted on github pages. For this step, use the terminal as follows or install [Github Desktop][github_desktop]:

```markdown
$ git init
$ git add -A .
$ git commit -m "your-message"
$ git remote add origin https://github.com/username/reponame.git
$ git push -u origin master
```

Now you should be all set!

One last note, I found something that I might need to change in the future. The current search function in the archive page is not able to search through the archive yet, it can only search the whole Internet. I don't know how to fix it yet, but hopefully I'll figure it out soon.

2018.12.26

[jekyll_template]: https://github.com/melangue/dactl
[repository]:      https://github.com/melangue/dactl
[tutorial]:        https://www.tutorialspoint.com/ruby/ruby_installation_windows.htm
[here]:            https://www.youtube.com/watch?v=-DJz7yC3iOI
[github_desktop]:  https://desktop.github.com/
