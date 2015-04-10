## What is the difference between Rackspace CDN and Cloud Files CDN?

### What are the new features?
### How do I move from Cloud Files CDN to Rackspace CDN?


## How do I get started using the Rackspace CDN?
### Control Panel overview
### Command line tools?

## How do I get an SSL certificate for my domain that is compatible with Rackspace CDN?
### Steps
    Note: Key issue, your cert has to be signed by the Akamai CA

## Known Limitations
### Unclear (SSL?)

## Basic Use Cases for Rackspace CDN

### Static asset compilation for a web app?

### Ruby on Rails?

### Blogs and DB-powered content

Instead having your web servers render content for *every* unique visit, you can use a CDN to deliver cached content to website visitors instead. This will reduce the overall load on your local web server and database - because HTML is being served in a local edge location. Apart from this CPU efficiency, users will also get content faster, since the latency has improved.

### eCommerce stores

For eCommerce stores with lots of photos and static assets, rendering product pages can involve paying for a lot of outgoing bandwidth. If your eCommerce platform renders images on the fly (for custom dimensions, for example), this gets even more expensive. Rackspace CDN allows you to selectively cache certain sub-domains or URL patterns to edge locations - allowing assets.mydomain.com, for example, to be fully cacheable. Users will now hit the edge location, rather than your web servers.

### Video streaming

If your site broadcasts live feeds or video uploads, having to cope with spikes in traffic can be stressful and costly. If you implement a cache, however, you are in a much better position: your content is now distributed across the globe and there are no singular points of failure.

### Static Site hosting?

Like the previous version of Rackspace CDN, you can upload a static HTML website to Cloud Files and put a CDN in front of it. This is a very simple and scalable way of rendering simple content without having to pay for and maintain web servers and associated software. 
