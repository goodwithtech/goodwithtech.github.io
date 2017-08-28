---
layout: post
title:  "The way to build your corporate sites for free"
date:   2017-08-28
desc: ""
keywords: "gh-pages,website,cloudflare"
categories: [BLOG]
tags: [inflastructure]
icon: icon-html
---


# Conclusion
1. Corporate site : [GitHub Pages](https://help.github.com/articles/creating-a-github-pages-site-with-the-jekyll-theme-chooser/)
	2. Homepage
	3. BLOG
2. Mail : Forward mail to own personal Gmail
3. CDN/SSL : [Cloudflare](https://cloudflare.com/)
4. Chat : [Slack](https://slack.com/)

# Requirements
## 1. Corporate site
- Company blog
- i18n
- Secure
- No need maintain maintain the server

## 2. Mail
- No need corporate's mail server.
- Forwarding mail to personal Gmail account. I don't wanna switch Google accounts anymore.
- No need maintain the mailserver

## 3. CDN/SSL
- No need to maintain certification files and servers

# Comparison

## Corporate site
- [Heroku](https://heroku.com/) is a better way if you want to use wordpress or so on.

## Mail
- [Zoho mail](https://www.zoho.com/mail/) is a better way if you want to corporate's mailserver. You can use free until 10 users, 2GB.
- [mailgun](https://www.mailgun.com/) is a better way if you want to do something when receive a mail.

## CDN/SSL
- You can choose [Let's encrypt](https://letsencrypt.org/), but it takes some cost if you want to updating certificate files automatically.

# Settings

## At first

1. Create your account at some name Domain Name Registory service
2. Register your corporate's domain


## DNS/CDN/SSL
1. [Create a Cloudflare account and add a website](https://support.cloudflare.com/hc/en-us/articles/201720164-Step-2-Create-a-Cloudflare-account-and-add-a-website)
2. [Change your domain name servers to Cloudflare](https://support.cloudflare.com/hc/en-us/articles/205195708-Step-3-Change-your-domain-name-servers-to-Cloudflare)
3. cloud mark if you want to use SSL/CDN. You can choose simple DNS feature if you don't check cloud mark.


## Mail
It would be set forward to another mail domain only [Onamae.com]().
Please let me know if you know how to set another NS hosting service.


3. Setting > Mail > Add
4. Log into Gmail
5. Set two factor auth if you don't.
6. Gmail > Setting > Add some account
	7. Reference [this article](https://ossia.co.jp/blog/2017/02/06/gmail-onamae/)
7. Verify your domain [each ESP](https://help.mailgun.com/hc/en-us/articles/215238578-I-m-not-receiving-complaints-from-some-recipients-domains-How-can-I-fix-this-)




## GitHub Pages
1. Create or Login your personal GitHub account
2. Create your organization
3. Create repositories *your-organization*.github.io
4. Setting > GitHub pages
5. Choose a theme
5. Add CNAME www *your-organize-account*.github.io if you can access *your-organize-account*.github.io

## Each captures
- GitHub page
<!-- ![gh-page]({{ site.img_path }}/build_corporate_site/gh-page.png) -->

- Cloudflare
<!-- ![cloudflare]({{ site.img_path }}/build_corporate_site/onamae.png) -->

- Onamae.com
<!-- ![onamae]({{ site.img_path }}/build_corporate_site/onamae.png) -->

## Slack
1. No special way to setting. Create your team normally.

# Conclusion
Now You don't need money to create your new business environment.
Your payment is only to register your Domain.
Please advice to me if you know a better way than my article.
