**Rackspace CDN User Guide Outline**

Created: April 22, 2015 - Revisions received from Megan Meza and Brian Metzler and applied.

For use to create Knowledge Center User Guide/Articles for using Rackspace CDN through the control panel

I.	**Overview**

    A.	Uses of Rackspace CDN

    B.	Access to Rackspace CDN
    
    C.	Limits of Rackspace CDN
    
    D.	Rackspace CDN terminology
    
    E.	User Guide table of contents       

II.	**Create a service**

   A. Create a service 

    Fields include:
    
    - Service Name
            
    - Domain Name
            
    - Origin – May be a URL or an IP Address

   B.	Origin Rules
    
    Origin rules should be used if you have multiple infrastructions setup to serve a single domain. Adding an additional origin will always require that you add a rule for which traffic should pull from that origin. 

    Fields include: 

    - Name – Default Origin

    - Applied Path

    - Origin

    Buttons:

    - Edit Rule: To provide Name and Path. Path may be a complete path or a wildcard.

    - Delete Rule: To delete the selected rule.

   C.	Caching Rules

    Caching rules are designed to determine how long your content should live on the edge before checking the origin for an update. If your content changes frequently, you may want to set up a TTL (Time to Live) rule that pulls every few minutes. If your content does not change frequently, we suggest you set a longer TTL of 12-24 hours.
 
    Fields include:

    - Name 

    - Applied Path

    - Detail

    Button:

    - Add Rule

   D.	Restrictions 

    Restriction rules limit who can see your content. All rules below are designed to show a list of traffic you allow. For example, a referrer value of "website.com" would ALLOW traffic being requested from website.com, NOT deny traffic from website.com.

    Fields include:

    - Name

    - Type

    - Applied Path

    - Detail

    Button:

    - Add Rule with the following fields:

        - Name
        
        - Type
        
        - Referrer (Referrer may be a path or a wildcard)

   E.	Update your Domain Name System (DNS) Access your website (Idea for this is from API GSG. Do we need a section like this in the KC UG?)

   F.	Access your website (Idea for this is from API GSG. Do we need a section like this in the KC UG?)
    
    


III.	**Manage CDN Service**

  A.	Service Details

    Describe all the details at the top of the page and what they mean

	Enable Logs

	Add Domains/Origins 

  B.	Actions cog (see next high-level sections)

    1.	REFRESH CONTENT – Purge

    2.	MANAGE – Rename

    3.	MANAGE - Delete

  C.	Purge files (Actions – REFRESH CONTENT - Purge)

    Dialog includes the following radio buttons:

    - Purge All Files
    
    - Purge Some Files – Specify File Path in field

  D.	Rename service (Actions – MANAGE – Rename)

    - Service Name

  E.	Delete service (Actions – MANAGE – Delete)

    Permanently delete this service?
    
    Warning: You will not be able to access content for this website until you reconfigure your CNAME entry.