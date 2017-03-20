<!--
Creator: Brandon Kerr
For GA WDI 32 
-->

# Building a Portfolio Website
------
According to a recent Forbes article, 56 percent of all hiring managers are more impressed by a candidate’s online portfolio than any other personal branding tool. However, only 7 percent of job seekers have created an online portfolio.

## So Let's Do That
### What You Need:
* Website hosting service
* Front end code (don't bother with Angular that's silly. One page is where it's at.)
* Domain name (optional)

### Hosting
**Recommended:** Github Pages

Github has built in tools that allow you to host your website directly from a repository. This is super useful because any time you push to your repository, the website is automagically updated without any more input from you. The default github link is also pretty solid - username.github.io - though a personal domain is still recommended.

**How to:**

[Official Guide](https://pages.github.com/)

1. Create a new repository, titled `username.github.io` (But replace with your username!)
2. Add your repository as a remote for your front end code: 
<br>
	` git remote add origin https://github.com/username/username.github.io `
<br>
	Or clone the repo onto your local machine if you don't already have code: <br>
	` git clone https://github.com/username/username.github.io`
3. Navigate to your repository on Github, click on `settings` from nav bar at the top of the repository
4. Scroll down to `GitHub Pages` and select which branch holds your website's code. If you have a custom domain, enter it in the textbox and GitHub will add the file required to use a custom domain name automagically.

### Front End Code
**Recommended:** Start with a template, modify it for your needs

Designing a portfolio website could easily take the better part of a week if you started from scratch. I recommend starting with a template and cutting out whatever pieces you don't need, then rebranding it to make it your own (at least change the colors!)

Browse around for a template that has all the features you want in your portfolio - A section highlighting projects or features, contact information, summary or description. I recommend looking for templates marketed at agencies, they tend to have all the sections you'll need. 

**Check Out** <br>
[Wix](http://www.wix.com/website/templates)<br>
[Start BootStrap](https://startbootstrap.com/)

### Domain Name
**Recommended:** GoDaddy - Great customer service and cheap prices

Buying a custom domain adds an extra touch to your portfolio website, and is probably expected since we're working with the web so you might as well throw down the money for it. (It's cheaper than Philz)

Browse around for domains that match either your name, or a common social media handle that you use. Common trends for extensions are `.com`, techy things like `nathan.codes` or `brikky.tech` as well as extensions that finish your name such as `ashe.ly` 

*.tech and .codes are both really cheap*

**Check Out** <br>
[GoDaddy](https://www.godaddy.com/?isc=gofd2001aj&countryview=1)<br>
[Google Domains](https://domains.google/)<br>
[Name Cheap](https://www.namecheap.com/)

### Last Thing!<br>(If Using Custom Domain)

You need to tell the company you used to purchase your domain name from where your site's content is located! There are guides for how to connect GitHub Pages to these domain name suppliers, but the general idea is:

1. Your GitHub repository needs to have a file called `CNAME` (no extension) which contains your URL: `myurl.com`
2. Go to the website where you purchased the domain to manage your URL, you should look for something like "DNS Settings" or "Manage URLs"
3. Add an A record (sometimes called a host record) or change the value of the existing one to be: 
<br> `"host" = @` <br> `"Points to" = 192.30.252.153`
4. Create another A record with the values: 
<br> `"host" = @` <br> `"Points to" = 192.30.252.154`
5. Add a CNAME record (sometimes called an alias record) with the values:
<br> `"host" = www` <br> `"Points to" = username.github.io` (use your username, though!)
6. Changes should happen within 5 minutes, but can take up to 24 hours to go through
7. If you have any issues, Google for a specific guide, `setting up Github Pages with GoDaddy/Google/Namecheap`. If that doesn't resolve your issue try contacting their customer support, they're usually really helpful and used to dealing with non-technical clients so they'll typically set up everything for you.



