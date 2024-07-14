+++
title = 'Quick thoughts on QA'
date = 2024-03-02T13:25:55-05:00
draft = false
+++


A friend of mine wanted to chat about a role as a software QA.  
Like anything in the tech field one term or role can mean many things.  

Wanted to get a couple notes down in draft, and expand on them when we meet to discuss the role in depth.  I'll start with somebackground for fun, then get into the notes.  

Background:  

It's been about a year since I've been in the software engineering field and probably about 7 years since I was in a QA role. So, going off memory but going to hit the big picture and drill in from there.  

I took on the role after having an internship as a software engineer. The internship involved a little more complexity than a traditional internship at the company, guess they wanted to challenge me. Instead of doing some simple C# projects, or getting involded in the companies main code bases in C#, like the other engineering interns did, they paired me with "the guy".  
This "the guy" was basically running an API platform for the company. The platform allowed inside and outside developers access to all the API's the companies created and subscribed to. All this to say that I didn't get to test so much as learn how to get the specific version of linux up and running and then get the software platform up and running, this was a lot, trust me.  

So when it came time to graduate and step over to the C# products role, they threw me at QA for 6 months to get my bearings.

Notes:  

What are we testing? Website, TV OS, Phone, Phone APP, Desktop App, Backend System, maybe even another system used by our product.

What is the goal of the testing? Are we six sigma? Are we sending this to the moon? Is it consumer, business, government or military used? Are we a start up compnay or a bank. What's at risk?

Where is testing currently and where does it need to be? Am I just maintaining the current testing and adding for any new features? Do we have blind spots? Do you know for sure? Do you a coverage percent?

From here depending on skill level, a potential QA may have all known knowledge of testing in the universe and may be able to 10x the whole company and also 100x their tests and software and lead the world into Utopia. For the rest of us, lets get some follow up questions going.

Lets say I'm new to testing, have the practical side of it, but feel I will do much better starting out with a close mentor/trainer, will that be available to me?

I can elaborate on role/career stuff but let's get to technical:  

Testing:

Unit, Component: Engineers should be writing unit tests, but may not be fully covered on how the units interact.  
Example, a calulator app, the engineer has confirmed all unit tests are passing for every calculation, but these tests never hit the clear but, just reset the test scenario. As a QA you see a real world issue, users hit clear after they do a calcualtion to do the next calculation. 
May not be the best term but to me this makes up more of a component or intergration test. How pieces make up a part or whole and/or how pieces interact. 

Also note that engineers may be running unit tests on the pieces of code that specifically do the calculation. Thinking about this further, the calculator app is a UI and many things can take place between hitting the individual keys and the creating the calculation. Some companies may have this type of distinction(front end / back end) the QA and Engineers need to focus on. In the end, it's best to have a close working team that can openly discuss where each should be focused. 

Local, Cloud
In the example of the calculator before, was it running in a browser(which? tested on each), on a phone(which? tested on each), desktop application?
Not going in depth on this but there should be a code base that you can run and test that it correctly build and starts locally. By locally either on your machine or a Virtual machine. 
From here think about how you package and deliver the product. If it is published as or to a website it may be a good idea to mirror the "production" version of the final product in a "staging" environment and this may be where you do the majority of your testing.  

Example: you are testing an amazon like website and they have created a new part of the website where you can Praise Bezos by rubbing an animated bald head similar to Jeff Bezos. Before pushing the feature/enhancement to production for the world to see, you have pulled the code to your local machine, got it up and running and added testing for this. The tests pass locally, but the local version is only using test data and doesn't actually connect to external api, basically is a limited version of the real thing.  
Going to the staging environment may be less limited and actually incorporate other systems api in their respective staging environment allowing you to get a more real world test.  
Generally, you now know that the feature is working, or haven't uncovered an issue yet. Following the example for an amazon like site, once in production it may be a good idea to have a "dummy" account and goes high level test the new feature.

**Note** you can be as in depth as you want, but depending on the product or company it may be the norm to only be testing on windows and android, or only chrome and mac OS. Knowing that things can run any and everywhere is great but IMO the best thing is to know the customer or product user and focus on the majority then work towards the edge case. 

Regression, Outage, Notification, CI/CD, Metrics, Error logs  