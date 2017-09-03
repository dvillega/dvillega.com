# Personal site

You can find this site at [dvillega.com](https://dvillega.com).

It is built with [Hugo](https://gohugo.io/), using the [goa theme](https://themes.gohugo.io/hugo-goa/), and [deployed to S3](https://lustforge.com/2016/02/27/hosting-hugo-on-aws/).

## Potential gotchas

I ran into a few problems when setting this up (2017-09-02).

- The about page needs to be located in `content/about.md` as opposed to `content/about/about.md` or `content/about/index.md`
- Permission denied issues for assets (js, css, imgs) following the deploy to s3 instructions. You can diagnose this by loading your site with the chrome dev tools open and look for 403 responses. I addressed this with a [bucket level policy](http://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html#example-bucket-policies-use-case-2).
- You must have tags and categories populated for each page or hugo throws a [bit of a fit](https://github.com/gohugoio/hugo/issues/3386).