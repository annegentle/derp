## What is the difference between Rackspace CDN and Cloud Files CDN?

Cloud Files CDN requires files to be uploaded to a Cloud Files container. Then you enable the CDN on that container.

Rackspace CDN just requires a web server, in any location, to serve content.  This could include Cloud Servers, Dedicated Servers (with a Cloud Account), or any other system internal or external to Rackspace.

Comparison:

Rackspace CDN                             Cloud Files CDN
Price tiered by region + request fees     Price Tiered with no regions, no request fees
No need to change website code            Requires code changes to a website
Improved features:  Custom SSL, Access    Limited purging 
Controls, Unlimited Purges
Features for static and dynamic content   No custom SSL
Designed for full site delivery	          Acceleration for static assets
Available for use with any cloud or       No access controls
dedicated server with public access
Assets automatically discovered in        No "full site" delivery
origin when requested
  
### What are the new features?
### How do I move from Cloud Files CDN to Rackspace CDN?


## How do I get started using the Rackspace CDN?
### Control Panel overview

How to set up a new CDN service
1. You need your own DNS Domain name.  Rackspace CDN (CDNaaS) does not provide you with the domain rackcdn.com like Cloud Files CDN does.  This might change in the future.  In this example, I will use 'racked.me' as my domain, and 'cdn.racked.me' as my DNS CName.

2. Go to the CDN option in REACH under Storage.

3. Click "Create Service" button.

4. Setup a Human Readable "Service Name", the "Domain Name" will be the CName you will be using, and the Origin is a HTTP/HTTPS server that will respond to Origin Pull requests from the CDN Edge Nodes.

5. From here, you will be presented with the Service Details page with the CDN URL.
Note: For your CDN service to work, you must create a CNAME record with your domain provider. The CDN domain for cdn.racked.me is cdn.racked.me.cdn319.raxcdn.com. If you use Rackspace to manager your Cloud DNS entries, you can complete this task under Networking -> Cloud DNS.

6. Now that you have the CDN Domain Name (cdn.racked.me.cdn319.raxcdn.com), you need to create the DNS CName record pointing to that Domain name.

Because this can be done through the customer's own DNS Servers, or Cloud DNS, this step is not included here.

7. Once everything is setup, the default Origin (http://104.239.140.241/image.png) should display the same as the CDN Domain (http://cdn.racked.me/image.png).

Note: If you've just set this up, the CDN configuration might not have pushed to Akamai yet. You might get a text web page similar to the following: Servuce Unavailable - DNS failure.

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
