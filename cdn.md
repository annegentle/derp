## What is the difference between Rackspace CDN and Cloud Files CDN?

Cloud Files CDN requires files to be uploaded to a Cloud Files container. Then you enable the CDN on that container.

Rackspace CDN just requires a web server, in any location, to serve content.  This could include Cloud Servers, Dedicated Servers (with a Cloud Account), or any other system internal or external to Rackspace.
  
### What are the new features?

**Powered by Akamai – A Best in Class Content Delivery Network**

Using Akamai’s industry leading network, Rackspace employs a custom map of over 200 edge locations across six continents, designed to meet the specific needs of Rackspace’s global customer footprint.  This map includes 77 North American locations, 36 European regions, 73 Asian, Middle Eastern and Oceania regions, and 15 South America regions.
 
**Instant Provisioning**

Rackspace CDN service can be turned on in seconds, through the Rackspace Cloud Control Panel, or via the REST API and language bindings.  No professional services, ticket requests, or phone calls are needed to get your site up and running on one of the world’s fastest CDN networks.  

**Multiple Interface Options**

Rackspace CDN is fully supported via the Rackspace Cloud Control panel.  Customers can also interact with Rackspace CDN via our REST API or one of our Software Development Kits (SDK) in Ruby, PHP, Java, node.js, Python, or .NET.   

**Whole Site Delivery and Acceleration**

Rackspace CDN is more than just accelerating individual objects in storage.   Using origin pull technology and DNS, you can simply identify your website and content origin and the entire site will be accelerated.  Everything from images to style sheets can benefit from CDN.  With no long-term contracts, trying CDN with your entire site has never been easier.  

**Origin Protection**

Keeping your origin safe during a malicious attack is vital to the health of your website or application.  Rackspace CDN helps your prepare for the unknown by absorbing edge requests, whether good or bad.  Since all requests are first served by the edge, your origin won’t get the brunt force traffic associated with a DDOS attack.  This means your website can still serve good traffic while an attack is taking place, keeping your visitors engaged at all times.

**Custom SSL**

Serving content over https is quickly becoming standard for modern websites and applications.  Rackspace CDN gives users multiple options for using their own domain while serving over https, including SAN (Subject Name Alternative) certificates and dedicated certificates.  

**Access Controls To Protect Content**

Rackspace CDN can help you control who sees your content by setting access rules that are enforced on the edge.  Access rules can be set by geography and referring domain and help prevent unwanted linking and traffic from non-strategic regions.  

**Multiple Origins Flexibility**

Rackspace offers customers a full portfolio of public, dedicated, and private managed cloud solutions for your workload.  Rackspace CDN can use any of these resources as origins, with the flexibility to use multiple origins with a single website or domain.  If you want, you can even use Rackspace CDN with origins not hosted at Rackspace. 

**Dynamic Visitor Handling**

Not all web content is created equal.  Rackspace CDN will deliver both static and dynamic content.  Dynamic content that changes for every user or a set of users requires additional handling at the edge.  Rackspace CDN will allow users to set a TTL of zero for uncachable content, and supports dynamic content handling features like cookies, header forwarding, and cross-origin resource sharing (CORS).  

**Keep Your Content Up-To-Date**

Rackspace CDN supports content TTLs (time to live) in seconds- all the way down to zero.  In addition, customers can submit requests any time they need to update content outside of the TTL timeframe.  Unlike other providers, these updates won’t cost extra since we know that keeping your content up-to-date on the edge is important.  

**Granular Control**

We know that web applications contain different types of data that require multiple edge rules.  For that reason, Rackspace CDN will allow you implement edge rules based on resource path, meaning your rules can apply to multiple levels of granularity, from the entire site to a specific file. 


### How do I move from Cloud Files CDN to Rackspace CDN?
Rackspace plans to migrate customers from Cloud Files CDN to Rackspace CDN.

## How do I get started using the Rackspace CDN?

### Control Panel overview

**How to set up a new CDN service**
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

### Using the API
For information about getting started using the API, see Rackspace CDN Getting Started Guide at http://docs.rackspace.com/cdn/api/v1.0/cdn-gettingstarted/content/Overview.html.

### Using the SDKs
For information about using the SDKs available for Rackspace CDN, see https://developer.rackspace.com/sdks/ (SDKs will be available here when Rackspace CDN goes UA). (For now, see https://gist.github.com/ycombinator/175d316694965a9ad2d7 for instructions about how to download and use the SDKs.)

### Command line tools?
Currently, there is no CLI for Rackspace CDN.

## How do I get an SSL certificate for my domain that is compatible with Rackspace CDN?
### Steps
    Note: Key issue, your cert has to be signed by the Akamai CA

## Known Limitations
### Unclear (SSL?)

## Basic Use Cases for Rackspace CDN
Basic use cases for Rackspace CDN are described at https://one.rackspace.com/display/atlanta/Cloud+CDN+Use+Cases. Additional use cases are described below.

### Static asset compilation for a web app?

### Ruby on Rails?

### Blogs and DB-powered content

Instead having your web servers render content for *every* unique visit, you can use a CDN to deliver cached content to website visitors instead. This will reduce the overall load on your local web server and database - because HTML is being served in a local edge location. Apart from this CPU efficiency, users will also get content faster, since the latency has improved.

### eCommerce stores

For eCommerce stores with lots of photos and static assets, rendering product pages can involve paying for a lot of outgoing bandwidth. If your eCommerce platform renders images on the fly (for custom dimensions, for example), this gets even more expensive. Rackspace CDN allows you to selectively cache certain sub-domains or URL patterns to edge locations - allowing assets.mydomain.com, for example, to be fully cacheable. Users will now hit the edge location, rather than your web servers.

### Video streaming

If your site broadcasts live feeds or video uploads, having to cope with spikes in traffic can be stressful and costly. If you implement a cache, however, you are in a much better position: your content is now distributed across the globe and there are no singular points of failure.

### Static Site hosting?

Like Cloud Files CDN, you can upload a static HTML website to Cloud Files and put a CDN in front of it. This is a very simple and scalable way of rendering simple content without having to pay for and maintain web servers and associated software. 
