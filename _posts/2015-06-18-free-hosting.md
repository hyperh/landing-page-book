---
layout: post
title: "Landing Page Guide Part 2: The Hosting"
tags: landing_page_guide
---

You _could_ always pay for hosting, but thanks to the Internet there are many good free hosting services out there we can take advantage of. A simple landing page shouldn't require anything complicated.

## Free Hosting
For our free hosting provider, we are going to use [GitHub Pages](https://pages.github.com). If you don't have a GitHub account, you can sign up [here](https://github.com/join).

> On a free GitHub account, anyone can see your files. But since we're just building a static landing page, anyone can see the HTML through `View Source` on any browser anyways.

### GitHub
1. Once you have an account, create a new repository.![Create a new repository](/assets/github-new-repo.png)
2. Enter a repository name.![Enter a repository name](/assets/github-repo-name.png) 
> You can change this later if you want in **Settings**.

3. Select **Initialize this repository with a README**.
![Initialize with a README](/assets/github-init-readme.png)
4. Create a new branch called `gh-pages`.
![Create a new branch](/assets/github-new-branch.png)
5. (Optional) Set the default branch to `gh-pages`.
	1. Go into the **Settings** of your repo.
	![GitHub repo settings](/assets/github-settings.png)
	2. Set default branch to `gh-pages`
	![Set default branch](/assets/github-default-branch.png)
6. Copy the clone URL of the repository.![Clone URL](/assets/github-clone-url.png) It should look like this: {% highlight html %} https://github.com/username/my-site.git {% endhighlight %}	

### Terminal
1. Clone the remote git repository by typing the following into your terminal. {% highlight bash %} git clone https://github.com/username/my-site.git {% endhighlight %}
2. Let's try modifying the `README` file. Open the file and type in `Hello world!`.
3. Add and commit the file to your local git repo. {% highlight bash %} git add README.md
git commit -m "Just sayin' hi." {%  endhighlight %}
4. Push the commit to GitHub. {% highlight bash %} git push origin gh-pages {%  endhighlight %}

### Setting Up a Custom Domain Name

1. Sign into your Namecheap account.
2. Click on **Your Domains / Products**.
![Namecheap Main Page](/assets/namecheap-main-page.png)
3. Click on the domain name you want to display the webpage currently at `username.github.io`.
![Namecheap Domains](/assets/namecheap-your-domains.png)
4. Click on **URL Forwarding**.
![Namecheap My Website](/assets/namecheap-my-website.png)
5. Setup two CNAME records. One for the root apex `(@)` and one for `www.` Both point to `username.github.io.`. The period at the end is required.
![Namecheap Modify Domain](/assets/namecheap-modify-domain.png)
6. Click on **Save Changes**.
7. Go to your url and check that it's redirecting properly.

Now that we've set up hosting and our domain name is redirecting to our GitHub Pages repo, let's move on to [adding content]({% post_url 2015-06-19-look %}).