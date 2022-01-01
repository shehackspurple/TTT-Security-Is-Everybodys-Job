# TTT-Security-Is-Everybodys-Job
This repository will teach you got to present my talk "Security is everybody's job", a talk about DevSecOps.


# Security is Everybody's Job!

This is a “Train the Trainer” document, to be used by someone who wants to present this talk for an audience.  If you were hoping to learn more about this topic, and not to learn how to present this talk, stop reading this document and do this instead: 1) watch the [video of this talk](https://www.youtube.com/watch?v=zQJ5dxCvniU), 2) read the [blog series](https://wehackpurple.com/security-is-everybodys-job-part-1-devsecops/) based on this talk and 3) follow the author of this talk to continue learning about this topic, [Tanya Janca](https://twitter.com/shehackspurple).  Thanks!

## How To Use

Welcome, Presenter! Thank you so much for wanting to spread the word and help make the world a more secure place!  This document will attempt to help you do a great job of presenting this talk, so that you look awesome and the audience learns and enjoys themselves.

Along with the video of the presentation, this document will link to all the stories, jokes and concepts you need to successfully present including PowerPoint slides.

Let’s get started, shall we?  

1.  Read this document in its entirety.

2.  Watch the [video of this talk](https://www.youtube.com/watch?v=zQJ5dxCvniU) 

3.  Watch the [“Train the Trainer”](https://www.youtube.com/watch?v=bWjPl-cKzFs) video, a slide by slide breakdown of possible stories, concepts or ideas that you should ideally try to explain.

This presentation is just talking, no demos.  You only need the slide deck and a screen. 

## Assets in Train-The-Trainer kit

- This guide
- PowerPoint presentation including notes for each slide (in this folder)
- Full-length recording of presentation [here](https://www.youtube.com/watch?v=zQJ5dxCvniU)
- Recorded “Train the Trainer” session [here](https://www.youtube.com/watch?v=bWjPl-cKzFs)


# Session Abstract (Use this to apply to speak somewhere)

In DevOps everyone performs security work, whether they like it or not.  With a ratio of 100/10/1 for Development, Operations, and Security, it’s impossible for the security team alone to get it all done. We must build security into each of “the three ways”; automating and/or improving efficiency of all security activities, speeding up feedback loops for security related activities, and providing continuous learning opportunities in relation to security. While it may sound like the security team needs to learn to sprint, give feedback, and teach at the same time, the real challenge is creating a culture that embodies the mindset that security is everybody's job.

# Session Story Summary

This presentation is an introduction to the topic of DevSecOpps and DevOps.  The focus should be ensuring the audience understands that DevOps is, then what DevSecOps is. We want them to walk away knowing what "The 3 Ways of DevOps" are, and a few things they can do to add security to those processes. We want the audience to feel confident they can make a positive difference in their workplace, and not at all intimidated about DevOps. The hope is that they are ON the DevOps team or willing to work with them, to ensure the systems they are creating and maintaining are secure.

This talk is beginner level for people who *already* work in technology, and hopefully have a grasp of what software development is. This talk would be great to present at any InfoSec, AppSec or DevOps meetups, or in an office to your team.


Session Outline (When applying to speak at places they often ask for this)
===============

This talk can be anywhere from 40 minutes to 60 minutes, depending upon how many stories you decide to tell for each slide.

I’m here to argue that DevOps is the best thing to happen to application security since OWASP.  And by the end I hope that you will agree that security is truly everybody’s job.  Let’s start!

My key take away is that I want developers and ops to realize that security is ALSO their responsibility, and that if they want to do DevOps (instead of traditional SDLC/dev) they have to adjust for security as well.


AppSec is a Thing, and it needs to be taken seriously:
Current status: causes around 1/4 of incidents (you know, those scary things you read about on the news)
Usual ratio  for Dev/Ops/AppSec is 100 > 10 > 1
Security is not taught thoroughly in schools
Waterfall never really worked, and the security model around it “stop while we do this” is slow and untenable, and certainly not possible in DevOps (Dinosaurs in a waterfall)

Now let’s talk about DevOps, and how I feel it’s main goals mesh nicely with security goals.

DevOps Main Goals:
* Improved deployment frequency; Awesome!  This means if a security bug is found it can be fixed extremely quickly. <check mark> (tell 8 months for emergency release story)
* Lower failure rate of new releases and faster recovery time; Meaning better availability, which is a key
security concern with any application (CIA).
* Shortened lead time between fixes; Fixing all bugs, including security bugs, faster.
* Faster time to market; meaning the business gets what they want. Sometimes we forget that the entire purpose
of every security team is to enable the business to get the job done securely.  And if we are doing DevSecOps,
getting them products that are more secure, faster, is a win for everyone. Again, check mark for security.

Let’s talk more in detail about The 3 ways (and how security fits in perfectly)
Summarize three ways
Emphasize the efficiency of the entire system, not just one part.
Fast feedback loops.
Continuous learning, risk taking and experimentation (failing fast)

Let’s dig in, shall we?

5 mins

1. (left -> right speed) (show SDLC)
Emphasize the efficiency of the entire system, not just one part.
	▪	This means that Security CANNOT slow down or stop the entire pipeline (pulling the Andon Cord), unless it's a true emergency. 
	▪	This means Security learning to sprint, just like Ops and Dev.
	▪	Focus on improving ALL value streams, and how securing the final product and network offer value to all other steams.  

What does this mean for developers? 
Efficiency and automation (of security activities)
	▪	Helping AppSec team tune web proxy scanners such as Zap, Burp and SonarCube - addressing issues it finds
	▪	Helping the AppSec team tune static code analysis tools (brakeman, Fortify, name more)
	▪	Add the bugs to the defect tracker, and don’t mark them as “fixed” when the appsec team isn’t looking 
	▪	Using templates and code samples that a known-secure (sec code library), reused code that has already had security testing performed on them
	▪	Using rescanned images that are up to date/fully patched
	▪	Repo Kid and other permission-reducing activities, for least priv from Netflix, be ready for changes
	▪	Add negative use cases as unit tests, not just positive use cases
	▪	If the AppSec team creates a security pipeline for testing for you, use it!
	▪	OWASP Dependency check, Retire.js, and tools to remove known vulnerable code/libraries/components
 

2. (left <- right - feedback)
Fast feedback loops meanings "Pushing Left" in application security.  (house analogy) The goal of security
activities must be to shorten and amplify feedback loops so security flaws (design issues) and bugs (code
issues) are fixed as early as possible, when it's faster, cheaper and easier to do a better job.
Ways to do this:

What does this mean for developers? 
Faster feedback loops (of security related events and activities)
	▪	Check all apps for things found in each pentest result, add these tests to unit tests
	▪	Rename insecure functions or libraries as “insecure” with a wrapper, so programmers see immediately that there is an issue.
	▪	Performing security sprints
	▪	Participating in Threat modelling activities if the AppSec team asks you for help
	▪	Participating in security incidents and investigations if need be
	▪	Informing the security team what Dev and Ops are concerned about, so they can ensure they don’t negatively affect those things, feedback 
	▪	 if security tests fail, the continuous integration server must break the build.  Just like quality tests.
	▪	Learning to use security tools, and how to use their feedback immediately to improve code quality
	▪	Use the security pipeline to test your code


3 (full circle - continuous learning) 
Culture change!  My favourite thing.  InfoSec needs some culture change.  In fact, all of IT does (including
Dev and Ops) if we want to make security everybody's job. 
•Allocating time for the improvement of daily work
•Creating rituals that reward the team for taking risks: celebrate successes
•Introducing faults into the system to increase resilience: red team exercises

Enabling and encouraging Continual experimentation, risk taking and learning from failure (failing fast):
*pushing to improve security
*innovations in testing, can't be locked down into one process
*
Fostering the understanding repetition and practice is the prerequisite to mastery: 
* Incident simulations: practice makes perfect
* Repeat secure coding training
	▪	If the metrics from the AppSec team show there are repetitive issues, create workshops, ensure everyone learns



What is the security team's job then?
To enable Dev and Ops to get their jobs done, securely.  It doesn't mean doing all the security work
themselves.  With a normal ratio for Dev/Ops/Sec of 100/10/1
* This means providing tools, processes and information in a timely and consumable manner.
* This does not mean doing all the security work within the security team, it means making it possible for Dev
and Ops to perform security, as part of their daily work. 
- Ensuring their processes match your pace
- Automating tools to test and give you feedback
- creating learning opportunities, providing formal lessons
- Feeding your knowledge base with mitigation advice that works
- providing resources, including creating or purchasing tools for developers
- using feedback and metrics to adapt to developer’s needs
- Provide security training
* This means giving dev and ops access to sec tools, showing them how to use them
* Building sec tools into all levels of the pipeline, both static code analysis and dynamic testing
* teaching developers and ops what the security tool output means and how to address it, don't let the AppSec
person be the bottleneck
* ensure the security team understands what the developers, Ops and customers are concerned about, and what
they need (CIA - Confidentiality/Privacy, Integrity/Data Accuracy, Availability/Resilience) 
The outcomes of the Second Way include understanding and responding to all customers, internal and external,
shortening and amplifying all feedback loops, and embedding knowledge where we need it.
*teaching everyone when there's a security issue what happened
& Learning from mistakes - analyze metrics and trends and teach lessons on anything that repeats itself
(Defect Dojo is so great for this!)
* if security tests fail, the continuous integration server must break the build.  Just like quality tests.


Reinforce the new culture that security is everybody’s job
	▪	Celebrate when you pass a pentest or pass through the security pipeline for the first time with no highs or mediums
	▪	steal slides from insecurity in information technology

What does this mean for culture change? 
Developers will need to perform some security activities, and will receive different types of support, as we build security into each of “the three ways”.
The security team is going to need to learn to sprint, give feedback, and teach at the same time.
Everyone in IT needs to have a culture shift, not only speed, agility, quality, learning and resilience, but also security.
The definition of quality includes “secure” from now on.  Resilience means security.  Learning will include security. Speed in responding to security issues, not just operational issues.  All of this means weaving security into every aspect of developing software, start to finish.

Resources: lots of resources to help the audience learn more.

Q & A - this can take up to 20 minutes, budget an hour for this talk + Q&A, if possible.


Train the Trainer Video
=======================

Recorded Train-The-Trainer session [here](https://www.youtube.com/watch?v=bWjPl-cKzFs)


## Resources for Audience 

* [https://shehackspurple.ca](https://shehackspurple.ca)
* [Security is Everybody's Job Blog Series](https://wehackpurple.com/security-is-everybodys-job-part-1-devsecops/)
* [https://twitter.com/shehackspurple](https://twitter.com/shehackspurple)
* [We Hack Purple Community](https://community.wehackpurple.com)
* [We Hack Purple Blog](https://wehackpurple.com/blogs)
* [https://youtube.com/SheHacksPurple ](https://youtube.com/SheHacksPurple )


## Document Information

**Content Developer & Author**
[Tanya Janca](https://shehackspurple.ca)


# Change Log
Published: (Janualy 1, 2022)
