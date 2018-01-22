---
layout: post
title:  "How to host static site by Google Cloud Storage"
date:   2018-01-23
desc: ""
keywords: "googke,gcp"
categories: [BLOG]
tags: [inflastructure]
icon: icon-html
---

Some of our front-end projects are hosted by [Google Cloud Storage](https://cloud.google.com/storage/), and cached by [Cloudflare](https://www.cloudflare.com/).
Today I will introduce how to host with GCS and Cloudflare.

# Steps
## 1. Verify your domain
I like verifying by Domain Name provider because no need to host servers and really easy.

1. Go [Webmaster Central](https://www.google.com/webmasters/verification/home?hl=en)
2. Click "ADD A PROPERTY"
3. Choose "Alternative methods"
4. Choose "Domain name provider"
5. Type: `TXT`, Name : `@`, Content: `google-site` in Cloudflare
6. Click "VERIFY"

<img src="{{ site.img_path }}/cloud_storage/verifying.png" width="75%">

This DNS record must not be deleted if you want to keep the verification.

## 2. Create Storage Bucket

1. Create Bucket : `gsutil mb gs://www.example.com`, if you host `https://www.example.com`
2. Upload files : `gsutil rsync -R /path/to/dir gs://www.example.com`
3. `chmod` your files : `gsutil acl -r ch -u AllUsers:R gs://www.example.com/*`
4. Set index/error pages : `gsutil web set -m index.html -e 404.html gs://www.example.com`

## 3. Add `CNAME` Record

1. Create a CNAME record that points to `c.storage.googleapis.com`

<img src="{{ site.img_path }}/cloud_storage/cloudflare_settings.png" width="75%">

# Conclusion

It's very easy to host static files.
