<!--
Creator: Brandon Kerr
For GA WDI 32 
-->

# Building a Portfolio Website
------
According to [Forbes](https://www.forbes.com/sites/jacquelynsmith/2013/04/26/why-every-job-seeker-should-have-a-personal-website-and-what-it-should-include/#3ce890c2119e), 56% of all hiring managers are more impressed by a candidate’s online portfolio than any other personal branding tool. However, only 7% of job seekers have created an online portfolio - which means having one gives you a huge advantage in the job market.

## So Let's Make One
### What You Need:
* Website Hosting
* Code for Your Site
* A Purchased Domain Name (optional)

### Hosting
**Recommended:** Github Pages

Github has built in tools that allow you to host your website directly from a repository, which makes updating a breeze. Any time you push to your repository, the website is automatically updated without any extra work. The default URL for Github Pages - username.github.io - is much better than using Wix or Squarespace, though a personal domain is still the most professional option.

**How to:**

[Official Guide for Github Pages](https://pages.github.com/)

1. Create a new repository called `USERNAME.github.io` (using your username)
2. cd into the local directory with your website's code, and add the new repository as a remote: 
<br>`git remote add origin https://github.com/USERNAME/USERNAME.github.io`
<br>Or clone the repo onto your local machine if you haven't build the website yet: <br>
`git clone https://github.com/username/username.github.io`
3. Navigate to your repository on Github (`https://github.com/USERNAME/USERNAME.github.io`), click on `settings` from nav bar at the top of the repository
4. Scroll down to `GitHub Pages` and select which branch holds your website's code - most likely master. If you have a custom domain, enter it in the textbox and GitHub will add the file required to use a custom domain name automatically.

### Front End Code
**Recommended:** Start with a template and modify it for your needs.

Designing a portfolio website could easily take the better part of a week if you start from scratch. I recommend using a template and cutting out whatever pieces you don't need, then rebranding it to make it your own - at least change the colors!

Browse around for a template that has all the features you want in your portfolio - a section highlighting projects or features, contact information, and a summary or description. Look for templates for agencies and other service businesses, they tend to have all the sections you'll need. 

**Search for Templates Here:** <br>
[Wix](http://www.wix.com/website/templates)<br>
[Start BootStrap](https://startbootstrap.com/)

### Domain Name
**Recommended:** GoDaddy - Great customer service and cheap prices 

Buying a custom domain adds an extra touch to your portfolio website, and is often expected of technical candidates because it shows at least a baseline understanding of how the internet works.

Browse around for domains that match either your name, or a common social media handle that you use. Common trends for extensions are of course `.com`, tech-oriented things like `nathan.codes` or `brikky.tech` as well as extensions that finish your name such as `ashe.ly` 

*.tech and .codes are cheaper than standard domains like .net or .com*

**Purchase Your Domain at:** <br>
[GoDaddy](https://www.godaddy.com/?isc=gofd2001aj&countryview=1)<br>
[Google Domains](https://domains.google/)<br>
[Name Cheap](https://www.namecheap.com/)

### Set Up DNS Records - If Using a Custom Domain

If you purchase a domain, you'll need to tell the company you used to purchase your domain name from where your site's content is located. There are guides for how to connect GitHub Pages to the domain name registrars linked above, but the general idea is:

1. Your GitHub repository needs to have a file called `CNAME` (no extension) which contains only the URL you purchased: `myurl.com`
2. Go to the website where you purchased the domain to manage your URL, you should look for something like "DNS Settings" or "Manage URLs"
3. Add an A record (sometimes called a host record) or change the value of the existing one to be: 
<br> `"host" = @` <br> `"Points to" = 192.30.252.153`
4. Create another A record with the values: 
<br> `"host" = @` <br> `"Points to" = 192.30.252.154`
<br>These IP addresses point to Github Pages
5. Add a CNAME record (sometimes called an alias record) with the values:
<br> `"host" = www` <br> `"Points to" = USERNAME.github.io` 
6. Changes should happen within 5 minutes, but *can* take up to 24 hours to go through
7. If you have any issues, Google for a specific guide, `setting up Github Pages with GoDaddy/Google/Namecheap`. If that doesn't resolve your issue try contacting their customer support - they can often set up all of the files for you.



