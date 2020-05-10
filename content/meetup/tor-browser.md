Title: Tor Browser
Date: 2019-12-01 12:20
Author: amolkahat
Category: Meetups/conferences
Tags: tor
Slug: tor-browser
Status: published

**Date:** 2019-12-30  
**Venue:** Red Hat India Pvt. Ltd. Pune, MH, India

**Meetup Name:** [WoSec and  InfoSecGirls workshop by Kushal Das](https://www.meetup.com/WoSEC-India-Women-of-Security/events/266136146/)

Hi, After long time.. I'm writing blog. Today I went to WoSec amd InfoSecGirls meetup,  
and meetup was focused on Tor. Kushal was speaker he talked about  
Tor Browser and it's services. Here are few things which he covered:

1.  Tor is used for anonymity, when you are using Tor no one can track you.  
   They can see you are connected to some server but they do not see what you are  
   doing there.
2.  Tor network is part of Dark Network, lot's of .onion sites are hosted using the Tor services.
3.  You can setup .onion website very easy. You just need to have tor browser installed in your system.
    1.  Let's set it up with Django
    2.  Create Simple django project and run it on 80 port.
    3.  Edit **/etc/tor/torrc** file and uncomment following lines.  

        > HiddenServiceDir /var/lib/tor/hidden\_service/  
       > HiddenServicePort 80 127.0.0.1:80

    4.  Restart Tor service
    5.  You will see there will be one directory in **/var/lib/tor/hidden\_services/**,it will contain one file known as hostname, it will be your .onion link.
    6.  Tor Browser version: 0.4.x support version 3 addressing. You cold see that your URL will be **siidrba5vbfitbudvyvrm5gg7exiq2sw4y3cy5v4ims26rz24zribeyd.onion** long. (Note: Version 2 addressing use 16 bit addressing)
    7.  Put that tor URL link in Tor Browser.. and... here you go.. your website is running in Tor network.

4.  Setup 16 bit address for our website.
    1.  Edit **/etc/tor/torrc** file
    2.  Add these lines below the **HiddenServicePort** line
    3.  HiddenServiceDir /var/lib/tor/service2/  
       > HiddenServiceVersion 2  
       > HiddenServicePort 80 127.0.0.1:80

    4.  Well, in above code we are creating one more service to the same website but it will be 16 bit.
    5.  Restart Tor service
    6.  You could see that now in **/var/lib/tor/service2/** you could see one more hostname file and it will contain 16 bit **.onion** url link.

5.  Now let's see how to setup tor URL link only for specific people.
    1.  To setup tor service we uncomment few lins in **/etc/tor/torrc** file. Now let's go and add one more line below our service2.  

        > HiddenServiceDir /var/lib/tor/service2/  
       > HiddenServiceVersion 2  
       > HiddenServicePort 80 127.0.0.1:80  
       > HiddenServiceAuthorizeClient stealth service2

    2.  It will setup this service for those users whom has the key.  
       (Well, key...?, which key...? will see it)
    3.  Restart Tor service.
    4.  cat /var/lib/tor/service2/hostname  
       > \<.onion url\> \<secret\>

    5.  Add that secret to tor Browser's torrc file.  
       Location: **\~/Tor\_Browser/Browser/TorBrowser/Data/Tor/torrc**
    6.  HidServAuth nnaiiplq6zzyrfwj.onion d60/MWahqH2TUEIZLJ+HXB

    7.  And you are set. Restart Tor Browser. You are able to hit the URL.

I found Tor very interesting. I love to dig more arount it.

1.  
