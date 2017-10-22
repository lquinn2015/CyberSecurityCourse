
# CyberSecurity_Week7_Assignment

# Project 7 - WordPress Pentesting

Time spent: 20+ hours spent in total (Majority of time was figuring out workarounds due to bad installing. Note Posting was not an option for me so SQL CSRF and any Posting exploit was very very difficult)

> Objective: Find, analyze, recreate, and document **Three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1\. [x]  (Required) Title: WordPress <= 4.1.1 - Unauthenticated Stored Cross-Site Scripting (XSS)
- [x] Summary: 
	Title: WordPress <= 4.1.1 - Unauthenticated Stored Cross-Site Scripting (XSS)
    Reference: https://wpvulndb.com/vulnerabilities/7929
    Reference: https://wordpress.org/news/2015/04/wordpress-4-1-2/
    Reference: https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/
    Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3438

- Vulnerability types: XSS 
- Tested in version: 4.1.1
- [x] GIF Walkthrough:<img src='https://imgur.com/a/ODlKt' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
- [x] Steps to recreate: Go to the comments section of the page. 
	 -Enter in <script>while(1){alert(document.cookie);}</script> in the comments box.  
	 -When you submit you will have an infinite amount number of cookie posts which will crash the broswer usually
	 -of alert messages.  After you are done with this vulnerability, reinstall the scotch box its easier that way
	- Extra - note although I show the admin doing this other users ie contributors, author type users can as well. 


2\. [x]  (Required) WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
- [x] Summary: 
	Title: WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
    Reference: https://wpvulndb.com/vulnerabilities/8768
    Reference: https://wordpress.org/news/2017/03/wordpress-4-7-3-security-and-maintenance-release/
    Reference: https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8
    Reference: https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html
    Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-6817

- Vulnerability types: XSS 
- Tested in version: 4.1.1
- [x] GIF Walkthrough:<img src='https://imgur.com/a/ODlKt' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
- [x] Steps to recreate: 
- Choose an youtube video that you would like to embed into the post
	- Add "[embed src=‘https://youtube.come/embed/12345\x3csvg onload=while(1){alert(document.cookie};\x3e’][/embed]" with the URL
	- Post the post
	- You will recieve an error message and be redirected to the images source.


3\. [x]  (Required) WordPress 3.3-4.7.4  - Large File Upload Error XSS
- [x] Summary: 
Title: WordPress 3.3-4.7.4 - Large File Upload Error XSS
    Reference: https://wpvulndb.com/vulnerabilities/8819
    Reference: https://wordpress.org/news/2017/05/wordpress-4-7-5/
    Reference: https://github.com/WordPress/WordPress/commit/8c7ea71edbbffca5d9766b7bea7c7f3722ffafa6
    Reference: https://hackerone.com/reports/203515
    Reference: https://hackerone.com/reports/203515
    Reference: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-9061

- Vulnerability types: XSS 
- Tested in version: 4.1.1
- [x] GIF Walkthrough:<img src='https://imgur.com/a/ODlKt' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
- [x] Steps to recreate: 
	- Choose an image that you will change the name of in your computers files.
	- Rename the image to a<img src=a onerror=alert(document.cookie)>.jpg, then upload the image to WordPress
	- Click on the image and then click view attachment page.
	- You will recieve an error message if the file is over 2 MBs

	-Extra: While this is not a major problem alone it would be easy for an admin that just recieve a large amount of files to upload to do
	- To increase danger look at social engineering.
