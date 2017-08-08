# mynotes

## Add a build matrix

https://saucelabs.com  
example:  
![example build matrix](https://saucelabs.com/browser-matrix/js-cookie.svg "example build matrix saucelabs.com")

## Platform for translation
https://crowdin.com  
[ublock origin example](https://crowdin.com/project/ublock)

### For profiling tips
https://www.paulirish.com/

### Deploy react native mobile apps
https://apphub.io/  
http://microsoft.github.io/code-push/

https://www.youtube.com/watch?v=pVNagJzzaFg  
**Eric Elliott
"You're writing the wrong thing if you're writing the implementation first"  
"Important to write tests first, so they fail"**  
Tools: Behavioral BDD (he hates those) -> tends to make tests too verbose  
best tests are quality checks -> really simple to read and write  
-> **very best tests are just equality tests**    
test code should be very  
uses Tape as a tool  
-> favors test tools which are dead simple  
all he cares about, did my tests pass?  

Why Node js so popular?  
ex: ruby tests 1hour!! in JS 3 min...  
it's asynchronous by default  

Use Promises  
non-blocking default way to make things in Node  
-> guaranteed to have API non-blocking, no problem waiting on disk read  

Express is not the only way -> recommends cause it's minimal and prefers to build on top of it  
Kapi, Sails (ruby on rails like)  

-------------
**Optimization:  
Start with page load, make the page visible as quick as possible, that's the key to success, best thing  
App startup  **

According to Harvard Business School, “Distributed teams tend to develop more modular products.”*

**Lobby for remote work, more remote friendly culture  
remote work culture really important  **

------------

Kraken JS: Paypal Open Source  
http://krakenjs.com/  

Websites to choose software  
http://alternativeto.net  
https://www.g2crowd.com/

Platform to be crowd financed as a service/content/product creator (monthly salary)  
https://www.tipeee.com/  
https://www.patreon.com/

**Assets naming**  
ref: https://medium.com/pixelpoint/handoffs-guide-for-pixel-perfect-design-part-i-8bbd95d8ffcd  
NB: https://pixelpoint.io is a good website for website speed example
- Latin characters only  
- no spaces  
- lowercase only  
- @2x or @3x postfix to prepare images for devices with different pixel densities  
- use same rules for folder names  
ex: ```customer-service@2x.png```

**Picture format guide**  
NB: check out Google image optimization guide  
- .jpg for pictures without transparency, when quality can be sacrifice in favor of size  
- .png for best quality and transparency  
- .gif or video formats for animations (keep in mind GIFs are a very old format, video file will be higher in quality but smaller in size)  
**Compress/Optimize images**  
Tools:  
- Kraken  
- ImageOptim  
- Optimage  
- SVGOMG (optimize SVG)  

**SVG**
On https://www.vectorizer.io, put blur to the maximum possible to reduce file size  

Acceptable compression level for non-static pictures:  
- 1920x600: < 180KB  
- 600x400: < 60KB
- 300x200: < 30KB  

**Responsive web design breakpoints**  
- 320x568  
- 375x667  
- 768x1024  
- 1024x768  
- 1280x768  
- 1366x768  
- 1920x1080  

**Tools for prototyping user journeys**  
- InVision  
- Axure  

**Tools for animations**  
- Principle  
- Framer  
- Adobe After Effects  

**Tools to create UI library**
- Craft  

**Tools to export from Sketch or PSD**
- Invision Inspect  
- Zeplin  
- Sympli  
- Sketch Measure  

## Node version manager
n is easier to use than nvm

## SEO
add schema.org specifications  
add open graph protocol ogp.me specs

## DevOps
Infrastructure as code: Terraform + Ansible  
Platform to micro-services infrastructure : Kubernetes  
CI/ CD : Jenkins | drone | sonarqube | travisCI | circleCI  
Docker  
AWS

## CSS Frameworks
Boostrap CSS has a much bigger community compared to Foundation
Setup CSS cache invalidation system
Setup CSS unused rules cleaning system

## Analytics
Consider Yandex Metrica (provides other insights that GA doesn't provide -> heat maps = visual representation of which areas in your site is popular)  

## UX
Create Personas http://personapp.io/  
try https://www.figma.com/  

## Apps for startup
http://startupstash.com/  
https://www.getharvest.com/ (time-tracking, report, expenses, project etc)

#React Native
run rndebugger-open to Replace `open debugger-ui with Chrome` to `open React Native Debugger`.

#Download on App Store & Google Play badges
App Store: font Myriad Pro for the text "download on the"  
Google Play: font Geneva for the text "GET IT ON"
