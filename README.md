# OutfitHash
__________________________________________
A Node.JS Application That Leverages The AWS Product Advertising API To Automatically Generate Full, Relevant, Outfits Given Any Amazon URL </br>
#### Note: The Real GitHub Repo Is Private But This Logs The Site's Journey Up To Launch.
#### Site Is Built From Scratch. I had this idea while walking home from class and didn't think I could build it so I decided to try. This is what I came up with in about 2-3 weeks over winter break.</br>

__________________________________________

**School Year:** Freshman @ University of Maryland (class of 2021) </br>

~~## Site Is Live At : https://www.outfithash.com/~~ (The site broke since node changed a major version and I've been too busy to come back to fix it. Will be back hopefully?)

**Project Start Date:** 12/7/17 </br>
**v1.0.0 (Beta) Published:** 12/23/17 </br>
**v1.1.0 (Beta) Published - Individual Modules Implemented:** 12/24/17 </br>
**SSL Certificate Installation Completed:** 12/25/17 </br>
**v1.2.0 (Stable) Published - BrowserNode Adjustments, UX Refinements, & much more:** 1/1/18 </br>
**v1.3.0: TBD...been busy so don't know when I'll get back on this site to expand it

#### The Problem:
Wouldn't it be nice if you could just generate a whole outfit based on one clothing item you *love*. Imagine...with the click of a button getting stylish recommendations based on what article of clothing you enter into the search field (as a URL). Sometimes I just don't have time to look for new clothes or I've worn the same shoes for years and am looking for new ones. *The search is a pain and most of what I get I don't like.* Imagine being able to rapidly randomize outfits so you get exposed to more choices and hence make smarter buying decisions.

### The Solution:
Create an application that can find the types of clothes that you are looking for and allows a user to quickly randomize pinning what they like and continuing to randomize until they have a whole outfit they love. If someone just wants only one article of clothing then they can just keep randomizing until that one piece looks intersting. The user can save that outfit for later reference or immediately just visit the commerce site to purchase that outfit that they found/saved.

### The Initial Idea:
This is a huge idea so it needs to be narrowed down. Let's narrow it now to this: </br>
 </br>
Create an simple, 1 page, application that allows a user to enter the URL of a clothing product from Amazon that they like and the application will populate a grid of similar clothing for these clothing items:

- Jacket (Over-Wear)
- Shirt
- An Accessory (Watch, etc.)
- Belt
- Pants
- Shoes

The application will intially target only modern men's street style and eventually branch out to cover both genders as well as other types of style as rules are built for product selection.

The initial idea is a success to me if all of the features above in "The Solution" and "The Initial Idea" are implemented and run smoothly in a production environment without throwing fatal exceptions.

### The Overarching Steps That Will Be Taken To Solve This Problem:
This is the most crucial part of *any* project. I will not write a single line of code until I can define *exactly* what I want from the MVP (minimum viable product) and what steps are needed to be taken to get there in plain words. </br>
</br>
General Steps: </br>

1.) Scaffold frontend grid with image, title, and link placeholders. Also have input box. </br>
2.) Take URL input from the user </br>
3.) Strip the URL and get only the information needed like the item's category, color, and clothing type </br>
4.) Amazon's Associate API offers 3 operations that may be useful for this: ItemSearch, ItemLookup, and SimilarityLookup. What we need to do is specify the correct BrowserNodeId to search a correct category but the *most* difficult thing here is to find what keywords to run through the ItemSearch service based on what was in the URL...this will take further thinking. </br>
5.) Take the response and page of results and randomly pick an item (it's already in our criteria now) </br>
6.) Grab the attributes for that item we want (image, title, and link). To do this we will have to append specific modifying parameters on each service's request string (like if we want images we must say 'ResponseGroup=Images' to get images back singe they aren't sent with a normal ItemSearch request.</br>
*Note: Step 5 and 6 will both be done for each individual grid cell from a modular function* </br>
7.) Push all of the data collected up to the view layer. </br>
8.) Offer the user the ability to keep randomly choosing and the ability to pin items they like to keep them from changing. Eventually when all grids are pinned the outfit is complete. (also offering the user to save items in general and not just in an outfit context would be nice.) </br>
9.) At any point allow the user to enter a new url and restart the whole process back to step 2. </br>
 </br>
*Note: There are thousands of types of clothing so this application can't be perfect. But we can try our best to keep relevance at a maximum.* </br>
</br>
Finally.) Deploy the application once url entry, randomizing, pinning, and restart are operational. Add user profiles, saving items, saving outfits, and algorithim refinements as later features.</br>
</br>
*Project Backlog/Tasks:* https://trello.com/b/RbSR3loH </br>
</br>

#### What This Project Is For Me
**1.) Node.js Practice:** The first web framework I learned was Spring boot. It was a natural jump from Java (my first programming language) and I love the autoconfiguration it offfers in so many respects (DAO layer interfaces, SpringSecurity, etc.). When I learned Node I found that I sort of love it more since it is so explicit and you have to do everything yourself. I like that. I like seeing everything and having the granular control that Node offers. I also *love* using JavaScript with API's versus using Jackson to parse data into Java POJO's which feels so forced to me. I also really like npm and how simple it is versus Java's Gradle and Maven dependency management system. I also want to learn it better so it will be the framework of choice for this project.
</br>

**2.) Challenge:** [I am a TeamTreehouse student](https://teamtreehouse.com/benyamephrem2) and there I taught myself Java (when I was 16...I'm now 18), Spring Boot (In the last 2 months), JavaScript (In November), Node.js and Express (In November), and Python (In the last 2 weeks) I have run out of courses that I slated to take there. Now that finals approach and winter break approaches I need something to keep me intellectually occupied and my programming skills sharp since I can feel them dulling the every day I'm not solving problems and learning. This project serves as that leisurely project that I'll work on overtime just for fun and to make things.
</br>

### **Day 1: Non-Responsive Webpage I Made To Begin Writing Backend** (I just want user input right now): </br>
</br>
<a href="https://ibb.co/itETNw"><img src="https://preview.ibb.co/hjooNw/Screen_Shot_2017_12_08_at_11_33_07_AM.png" alt="Screen_Shot_2017_12_08_at_11_33_07_AM" border="0"></a><br /><br />
<br />

### **Day 5: Responsive Homepage Made As Site Is Built Out** (The site is starting to take shape): </br>
</br>
<a href="https://ibb.co/jPL4n6"><img src="https://preview.ibb.co/cxoDfR/Screen_Shot_2017_12_14_at_2_04_51_PM.png" alt="Screen_Shot_2017_12_14_at_2_04_51_PM" border="0"></a>
<br />

### **Day 8 This Is What The Responsive Clothing Grid Looks Like** (Grid Dimensions & Arrangement Adjusts To Screen Size): </br>
<a href="https://ibb.co/j7z626"><img src="https://preview.ibb.co/iDyNaR/grid.png" alt="grid" border="0"></a> </br>
</br>
</br>
### **Day 9 Pinning & User Choice After 1st Generate Implemented, Donation Page Completed, and Footer Cleaned Up**: </br>
</br>
<b>Before a URL is entered to generate:</b></br>
<a href="https://ibb.co/eGOvfR"><img src="https://preview.ibb.co/kK2AEm/screencapture_localhost_3000_generator_1513439457062.png" alt="screencapture_localhost_3000_generator_1513439457062" border="0"></a></br>
</br>
</br>
<b>After Generate:</b></br>
<a href="https://ibb.co/f9dd0R"><img src="https://preview.ibb.co/jsOYZm/screencapture_localhost_3000_generate_1513439596680.png" alt="screencapture_localhost_3000_generate_1513439596680" border="0"></a></br>
</br>
<b>Note:</b>
As you can see a placeholder is generated when an image request fails (for whatever reason). There is a promise that after the items info is fetched THEN the image is fetched and sometimes things just don't work (usually an error hashing the request signature...it's an intricate process) so a placeholder is used to resolve the promise so synchronous operation can continue and the final Promise.all() statement can run resolving the fetch as complete.</br>
</br>
</br>

Donation Page Complete (Still Day 9): </br>
<a href="https://ibb.co/jQLNS6"><img src="https://preview.ibb.co/mywwn6/screencapture_localhost_3000_donate_1513476896998.png" alt="screencapture_localhost_3000_donate_1513476896998" border="0"></a></br>
</br>

Footer After Some Tweaks (Still Day 9): </br>
<a href="https://ibb.co/j3PoH6"><img src="https://preview.ibb.co/c7joH6/Screen_Shot_2017_12_16_at_10_53_28_PM.png" alt="Screen_Shot_2017_12_16_at_10_53_28_PM" border="0"></a> </br>
</br>
</br>
### **Day 10: Front page completely finished and copywriting is complete**: </br>
<a href="https://ibb.co/htWB4m"><img src="https://preview.ibb.co/iZqhAR/screencapture_localhost_3000_1513531403895.png" alt="screencapture_localhost_3000_1513531403895" border="0"></a></br>
</br>
<b>Up Next:</b>
Time to go back to the backend to write some more error failsafes and input validation. Also need to make log-in page (authentication), user profile page, implement CRUD operations on any defined models, security, and authorization. A lot of work ahead, time to get it done.</br>
</br>
### **Day 11: Login + Signup Page Complete, User Schema Done, Authorization Middleware Done**: </br>
<a href="https://ibb.co/jvLWpm"><img src="https://preview.ibb.co/gUjD26/logins.png" alt="logins" border="0"></a> </br>
</br>
</br>
<b>Up Next:</b>
All that is left is to write the backend to handle the form post requests, inject the authorization middleware into the appropriate routes, adjust views based on if a user is logged in or not (global middleware I made avaliable allows us access to user attribute in the views to do this), annnnnnnnd implement the CRUD operations on outfits I mentioned before. Hopefully can get it all done today.</br>
### **Day 12: Authentication and Authorization backend finished. Logout works as well.**: </br>
<a href="https://ibb.co/j6Xo4m"><img src="https://preview.ibb.co/kWPPc6/screencapture_localhost_3000_profile_1513693381449.png" alt="screencapture_localhost_3000_profile_1513693381449" border="0"></a><br />
</br>
</br>
### **Day 13: More Scaffolding, Configured SMTP transporter, Added Individual Generator Modules (A future feature)...Site is realllly taking shape but UX is lacking.**: </br>
<a href="https://ibb.co/bYpfZm"><img src="https://preview.ibb.co/dTY7Em/screencapture_localhost_3000_contact_1513758553966.png" alt="screencapture_localhost_3000_contact_1513758553966" border="0"></a> </br>
</br>
<b>Up Next:</b>
Security, security, security. I need to implement server-side and client-side input validation using regex's, I need to implement CSRF (XSRF) protection on forms, and finally I need to improve the UX by making animations upon CRUD operations (like as a user I want to SEE the outfit disappear from the div when I delete) and adding flash messages after operations. It is CRAZY how many ways a web appliaction can be exploited if you aren't careful so I'll be sure to try my best to keep any user as safe as I can.</br>
</br>
</br>
### **Day 14: Clientside AND Serverside validation, Regex's, and DOM purification to prevent XSS (also implemented CSRF protection on all forms that are vectors for attack)**: </br>
<a href="https://ibb.co/cEbgs6"><img src="https://preview.ibb.co/b491s6/client_server_validation.png" alt="client_server_validation" border="0"></a> </br>
</br>
<b>Comments:</b>
Nearing deployment for beta testing. A little more security tweaks and UX adjustments and should be ready (still really rough but still need to keep things moving).
</br>
</br>
### **Day 15: Preaparing for delopyment for Beta Testing. Setting up Gulp build tools, buying domain, and deploying to Heroku.**: </br>
<a href="https://ibb.co/mkKoPm"><img src="https://preview.ibb.co/iKhWc6/beta.jpg" alt="beta" border="0"></a> </br>
</br>
<b>Comments:</b>
Currently setting up build tools and such. Goal is to get this into people's hands as fast as possible to get feedback and hence improve. Should be fully deployed tomorrow or after tomorrow but this is only the 2nd time I've deployed a web application so I may run into trouble.
</br>
</br>
### **Day 18: Individual Modules Done Front to Back TOTALLY, SSL being added to site (really annoying), and fine tuning.**: </br>
</br>
Homepage Dropdown To Individual Generators: </br>
<a href="https://ibb.co/fUNGx6"><img src="https://preview.ibb.co/mX1WVR/Screen_Shot_2017_12_25_at_3_40_43_AM.png" alt="Screen_Shot_2017_12_25_at_3_40_43_AM" border="0"></a> </br>
</br>
</br>
Profile Page Configured To Display Saved Individual Items AS WELL AS Whole Outfits: </br>
<a href="https://ibb.co/jn8TAR"><img src="https://preview.ibb.co/kSSzH6/screencapture_localhost_3000_profile_1514191317903.png" alt="screencapture_localhost_3000_profile_1514191317903" border="0"></a> </br>
</br>
</br>
**UPDATE 12/25/17:** Deployment's SSL endpoint has been fully configured and the connections are now served securely and encrypted end to end.
</br>
</br>

### **Day 25: v1.2.0 Out. Stable. Beginning User Testing and Getting Feedback...Just Getting The Word Out**: </br>
Reconfigured SSL To Use Native Heroku SSL vs using an expensive ($20/mo endpoint that I don't need now). Before the application ran off the free Heroku dyno, now I upgraded to the Hobby dyno which never sleeps (that killed page load time) and has free SSL. So I just reuploaded my certificate and key, destroyed the endpoint, disconnected the endpoint service, repointed the domain's DNS zone, and now we're good to go. Really proud of this site and know I can always make it better (and will make it better). I refined the BrowserNode picks for this stable version and now the generator picks really nice clothing and doesn't pick weird stuff like before (before the nodes were set to ALL mens shirts for example...I had to go in and specify exactly what I wanted in an array of viable nodes and every generate a node is picked randomly to be injected into the query string). Interested to see where this goes, kind of funny because I might even become a user of this soon...after I finish a few things that need to be done
</br>
</br>

#### Challenges Encountered
As I build this I will state what challenges I face besides just figuring my way around Node's native environment. </br>
</br>
**1.) Signing Amazon API Requests**: I thought this would be super easy since I've worked with API's before and even understand how the Oauth lifecycle works for API's that require it. But I soon found that Amazon had a pretty lengthy process for generating an authentication signature on requests (it has to be an RFC 2104-compliant HMAC created with the SHA256 hash algorithm). It consists of about 10 steps where if you are even a single character off then you are just completely wrong and your request will be thrown away. I built it out according to instructions and it just wouldn't work...then I went through debugging step by step logging what each step output.</br>
</br>
Then I found my problem. I wasn't explicitly writing '\n' since in the instructions it doesn't have that in the string but rather just says it in words that a newline should be inserted so it's something I just glazed over. It was such a good feeling to see the request work after all of the intricate steps necessary. I really feel that everyday that I develop and get better...slightly complex problems like this seem more and more routine and unintimidating than before when I started and *everything* (especially technical documentation) was intimidating.</br>
</br>
**2.) JavaScript Promises and Asynchronous Operations**: I knew that Node was a non-blocking framework that handled tasks asynchronously but I never knew how much of a headache that would come to be later when I have to bind requests in promises and really think about when everything will be done and what depends on what to work correctly. Still figuring it out...but it is making more and more sense. This has probably been the most souring thing for me when it comes to Node and is really...unenjoyable to debug...when requests are flying everywhere and coming back at different times or some fail and some don't.</br>
</br>
**3.) Debugging, Error Logging, and Error Handling**: Smarter error logs and logging in general leads to better insights when an application craches. Errors will happen. Requests may just not go through. I'm learning that you always have to be on your toes for when something will go wrong and have a backup plan. For example, if an image request doesn't go through, I load a placeholder instead so that the imageRequest promise can be fulfilled and the promise chain can keep moving along smoothly. Making smart logs and handling errors is the more boring side of coding to me but an important one as well since many of runs will have errors. The faster I can know where things are going wrong and catch them as they happen the cleaner my application will be.</br>
</br>
**Error Logs After Log Clean-Up** </br>
</br>
<a href="https://ibb.co/cjb2s6"><img src="https://preview.ibb.co/h0xWkR/logs.png" alt="logs" border="0"></a> </br>
</br>
**4.) Frontend Development**: My first language was Java and I've never been great at design. Frontend for this site has been a HUGE challenge for me. I had to learn Bootstrap (I already understood HTML and CSS competently) and from there it was much more rapid to develop the frontend. It looks very nice now I think but it took SO MUCH TIME to get it right. In the beginning I wanted to be like "screw it, I'll just have the site be unresponsive but then my friend [Michael Weinberger](https://github.com/mwein99) told me about the concept of developing "mobile first". So really if I want this to be a great site I have to be willing to learn things I don't care as much for and now I actually enjoy frontend...it's kind of like a break for me from intense server-side debugging. I just see it as necessary for me to do but I certainly don't see myself being a frontend developer...but I don't have a choice here. Also, no-one sees the backend code nor ever will. People see a pretty or ugly site and then judge its quality based off of that so frontend is a priority here.</br>
</br>
**5.) Flash Messages**: What I thought would be crazy easy was implementing flash messages on user actions so the user is informed on success and failure of an action. Little did I know it'd be REALLY annoying. I watched 5 tutorials, tried 4 libraries, and after like 5 hours of troubleshooting I finally got it to work. I just had to move things around in my app.js file because ORDER MATTERS when the application is set up and really weird things happen when everything isn't where it's supposed to be. There are still some bugs but it works pretty well now on redirects.</br>
</br>
**6.) Deployment**: Yep, you guessed it. Another issue that took hours of troubleshooting annnnnnnnnnnd...I was missing the word "return". Gotta love software development. Anyway, I had a huge issue deploying because for some reason my application ran PERFECT locallly but didn't even load when deployed remotely on push. I KNEW when I saw a page load for 3+ seconds SOMETHING was wrong with the route file but it took me literally a whole 6 hours day of troubleshooting to return (no pun intended) to my route file and.....yep....there was the problem. I was serving views with 'res.render(...)' but wasn't saying 'return res.render(...)'. This one word literally made all the difference. Now the nightmare is over luckily and funny thing is this EXACT same problem happened when I delpoyed my first web application to Heroku written in Java with the Spring framework. Go figure...anyway, now that that's over it should be smooth sailing. Gulp is fully configured...all I type is 'gulp' and the default task (I made an aggregate of sub-tasks) builds the ready-to-deploy application. Eager to finally get back to ACTUALLY coding and not working on deployment logistics.</br>
</br>
**7.) Scaling, Infrastructure Decisions, & Refactoring**: Naming things (crazy hard as things grow), backend & frontend rigidity, defining flow of data. As I'm developing new features for this application it becomes clearly apparent that every decision matters. The way you build an application will have a huge effect on how you scale and how fast you can scale. Luckily, I had this in mind and made modular functions for the generation of Azon API query strings, the signing of the requests, and finally for generating Promises for fetches to be executed. Had I not kept this in mind the development of the new features (like the individual modules) would have been really painful. Even now I see HUGE inefficiencies I need to address in repeated code and places where a large function can be replaced by smaller functions that are building blocks to that larger task. It has revealed itself to me that software is like an art with so many pieces fitting together to make a whole artwork...work. I have a lot of refactoring to do to keep up this idea of modular building blocks because I can already tell the application is getting bigger and bigger. The bigger challenge for me is refactoring the frontend rather than the backend since I feel like I change the DOM more often than a backend function will be changed. Anyway, it's been added to the backlog and the infrastructure of this application will be addressed thoroughly.
</br>
</br>

## Built With

* [Node.js](https://nodejs.org/en/) - Event-Driver Server-side Platform used
* [Express.js](https://expressjs.com/) - Node.js web application framework used
* [MongoDB](https://www.mongodb.com/) - MongoDB for Database
* [Bootstrap](https://getbootstrap.com/) - Bootstrap for Frontend
* [jQuery](https://jquery.com/) - Client-Side Document Object Model (DOM) Manipulations and Asynchronous JavaScript & XML (AJAX) Requests
* [Gulp](https://gulpjs.com/) - Development Workflow Task Automation
* [npm](https://www.npmjs.com/) - Package Manager
* [Atom](https://atom.io/) - Text Editor

* [This Application Uses The MEAN Stack](http://mean.io/)...almost...have to learn AngularJS

## Credits
* [Flaticon](https://www.flaticon.com/) - Icon assets
* [Michael Weinberger](https://github.com/mwein99) - Helped Me A Lot With Learning Bootstrap and Frontend
