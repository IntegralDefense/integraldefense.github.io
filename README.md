### Learn from attacks that bypass your preventions ###

I know, no kidding, right? Thanks, Captain Obvious! 

I find that we are trusting our commercial tools too much. If you take the "trust but verify" approach to attack detection, you will learn so much. If you apply what you learn, you will detect future attacks that bypass your preventions. 

There are several ways to get started. Starting with antivirus alerts is one simple way, since the attack made it to the endpoint. Regardless of how you start, the important aspect is being able to answer the question, "how was it delivered?" By attempting to answer that question, you will learn where you have visibility gaps and where your attacks are originating from. In addition to understanding the delivery vector of an attack, it is also important to classify the threat by risk level for your business. This information will allow you to make a data driven decision on where to focus your efforts. 

For us, email was the highest volume and highest risk delivery vector. While we had IDS in addition to IPS, as well as EDR along with antivirus, we only had an email prevention system, without a detection system. We decided to build our own. 

By implementing, and continually improving the Intel, Detect, Response process, we have not only become knowledgeable, but we now detect over 480 email attacks that bypass our email filter monthly. This represents a total population of 12,000 employees. Additionally, we are alerted when an employee clicks a link or opens an attachment related to the phish. This data provides us actual click rates, not just data from a phishing simulation. 

We continued to automate our manual processes, improving our ability to work more alerts with the same number of employees. We created detection systems and managed attack related data which fed our detection. 

 <img src="AlertIntelSources.png" alt="Alerts and Intelligence over time" width="600"/>

To kick-start our program, we initially focused on externally sourced intelligence in addition to answering the delivery vector question. While we continue to collect external intelligence, we prioritize those sources by focusing on high risk threats. As we have matured, we focus most of our efforts on internally sourced intelligence. It is the most relevant, contextual, reliable, and credible source of intelligence available. Managing and applying that data is the key to a highly capable program. 

As we streamlined the process of detection -> response -> intelligence -> detection for attacks bypassing our preventions, we started to detect more threats quarter over quarter. The system began feeding itself. 

There is no silver bullet and taking the time to learn all of the systems, data, and priorities was a journey, but it has been a journey that has made us very knowledgeable and improved our capability.  

The great news is that this approach is reproducible. 
_________________________________________________________________________________________________

### Previous Posts
**[Learn from attacks that bypass your preventions](#learn-from-attacks-that-bypass-your-preventions)**<br>
**[Treat every alert like a dollar in your budget](#treat-every-alert-like-a-dollar-in-your-budget)**<br>
**[I love not doing things](#i-love-not-doing-things)**<br>
**[Are You Winning?](#are-you-winning)**<br>
**[Custom Phish Detection For The Win](#custom-phish-detection-for-the-win)**<br>
**[Move to a Free First strategy](#move-to-free-first)**<br>
**[Opensource is well positioned for security automation](#opensource-is-well-positioned-for-security-automation)**<br>
**[The Process](#the-process)**<br>
**[Hello](#hello)**<br>

_________________________________________________________________________________________________

### Treat every alert like a dollar in your budget ###

Security 101:
 
	1) Buy a security platform (SIEM or similar)
	2) Pump data into the system
	3) Create a SOC (make sure to have many large screens, 24x7, follow-the-sun setup)
	4) Thousands of alerts daily, with no context.
	5) SOC submits ticket to IT team
	6) IT team closes ticket
	7) Go to step 4, repeat until breach.
	8) Buy new wizbang security technology
	9) Go to step 4. repeat until breach.
	10) Fire CISO
	11) Hire a service which does 1-9

Dave Ramsey says that when budgeting, every dollar should have a job and a purpose. This means that each dollar has an understood opportunity cost. 

Alerts have an opportunity cost too. If it isn't valuable, tune it or get rid of it. If it is valuable, it should be highlighted. Alerts should be easy to tune and even easier to turn off (if bad).

False positives are a way of life. False positives that add no value or take too long to analyze are like incurring high interest debt. 

> "You must gain control over your money (alerts) or the lack of it will forever control you.”

**Find Alert Peace.**

**_tldr:_**

Alert triage is similar to troubleshooting an IT problem. The more information collected up-front, the easier it is to find answers, the quicker the problem gets resolved. Security alerts are similar, the more understanding of why the alert fired, what it might represent, and the ability to find additional information drive quicker analysis. 

The goal is for every alert to have all the information required by a human to disposition the alert with confidence quickly, thereby reducing manual effort and time. Additionally, a tuning sub-process should be implemented within the normal flow of alert triage. This will not only help with alert fatigue, but improve coverage, and get your team thinking the right way.

If you can answer these questions, your alerts, and SOC, are working for you.
  - Why did this alert fire? 
  - What was the system looking for that created this alert? 
  - How often does this alert fire? 
  - How often is it a false positive vs malicious? Is this a new alert?
  - What is the impact if this alert is associated with evil?
  - How far in the attack cycle did the threat get?
  - Does the alert contain the information needed for an analyst to make a high confidence disposition? 
  - What data is needed to accomplish a high confidence disposition?
  - With the data required to make a high confidence disposition, does the analyst make the right decision? 
  - How long does it take the analyst to make the right decision?
  
_________________________________________________________________________________________________

### I love not doing things

### and I love that by not doing things we can do more things ###
 
- I love that we no longer need to manually pull pcaps for an IDS alert, it's just part of the alert in ACE. No more worries about pcaps rolling off before manually grabbing them. No more command line craziness to find and extract the pcaps related to the alert. No more scp'ing pcaps all over the place before we can analyze them.
- I love not having to manually lookup who a user is, where they are located, or what employee a computer belongs to, it's just part of the alert.
- I love that we no longer need to manually submit files to our sandboxes or manually lookup results on VT, it's just part of the alert.
- I love, upon a customized phish detection that bypasses our email preventions, we don't have to login to exchange, find the email and remove it. I love that we don't have to put in a ticket for removal. I love that ACE has a button to remediate it.
- I love how easily & quickly we detect credential harvester phish, remediate them, and know if any of our employees visited or supplied credentials.
- I love that we no longer need to manually combine and keep track of important alerts that relate to an attack, I can just combine them into ACE events.
- I love that as we have gotten better at detecting and remediating phish, the number of attacks that reach installation has almost vanished. (Actually, if I'm honest, I wish we had installation events more often to maintain our response skills.)
- I love, appreciate, and take for granted so many of the things we have created to improve our program.
 
Things that use to be hard, or tedious, no longer are. This provides us the opportunity to work on the next hard thing.
 
Why not have ACE do things, so your team can do more things?
 
Let's join forces and ***automate the ordinary!***
 
***(Ok and maybe the extraordinary too)***


_________________________________________________________________________________________________

### Are You Winning?

What does winning look like in cybersecurity? 
	
	- No business operations disruption? 
	- No financial loss? 
	- No loss of important data? 
	- No brand negativity? 

If you are winning, how well are you winning? 

What if you measured every attack that gets around at least one of your preventions? What if, for every one of these attacks you measured how far the attack made it in the attack cycle?
 
Dispositioning your security alerts by attack cycle provides this insight.

ACE not only provides you the ability to automate the ordinary, it also collects the data you need to understand your threats and risk, as part of the normal security operations process. 


##### Do you understand your security operations? #####

<img src="SecurityOperationsMetrics.png" alt="Security Operations Metrics" width="600"/>


##### Can you show you are winning? #####

<img src="Attack_Penetration.png" alt="Attack Penetration" width="600"/>


##### Do you know what threats are getting past your defenses? How well do you detect and prevent these threats? #####

<img src="Threats.png" alt="Your Threats" width="400"/>

________________________________________________________________________________________________

### Custom Phish Detection For The Win
#### Catch phish, clean'em, and use'em as bait ####

Ok, so phishing is not new, but waves of relentless phishing continue and bypass email prevention systems daily. It is odd that year over year the number of phishing attacks getting past prevention systems continues to increase.

From Business Email Compromise, to credential harvesters, to malicious attachments, and links to all sorts of malicious files; phishing is still the easiest, lowest cost delivery vector for attackers. Good thing for us it is also the easiest to detect (__believe it!__). 

In my experience if you have a good phishing prevention system and a good phishing awareness program, you are still missing attacks…a lot of attacks. While prevention is the ultimate goal, there is so much additional value gained by detecting and learning from the phish that bypass your preventions! 

   - **The best Intel source.** Those indicator feeds are nice, but way less valuable than the intel you gain when analyzing the phishing attacks that get past your preventions. This is the source of the most relevant, high quality, kill chain diverse intel you can find. Instead of investing in intel feeds, maybe you should invest in detection. 
   - **Practice.** Learning is all about iteration. Being able to iterate the detect, respond, intel cycle often and quickly will train your team intrinsically. They will better understand their data, visibility, and how it all fits together. They will then be prepared to work more stressful incidents, understand what is high priority vs what can wait, and more quickly focus on the right items. 
   - **Credibility.** When you get to the point of calling an employee minutes after they click a link to provide real-time training, the word gets around, and the company knows your team can be trusted. This drives the ability to influence and increases your chance of budget to improve on gaps.
   - **Winning.** Stop the attack early in the attack cycle instead of the resource intensive work of cleaning things up when the attacks reach further into the attack cycle. Know about the attack early in the cycle and feed that information into your detection systems quickly, so you are warned if later stages of the attack cycle are reached.
   - **Metrics & Risk identification.** Having data to show how far attacks are getting before they are prevented, the cycle times involved with alert triage, and the data to show what types of attacks you are facing all lead to an understanding of risk. Having this data builds credibility and trust, which helps when you need money to fill gaps and grow your program.
   - **Ease of disposition.** Alerts for email, if done correctly, have the most context of any type of alert and are amongst the easiest to triage. Very quick to disposition and respond to. 
   - **Combat Alert Fatigue.** When you are detecting attacks, learning from them, tuning detection, and remediating them quickly, alert fatigue issues are dramatically reduced. Alert fatigue is more of an issue when only false positives are witnessed, or the same non-value, long cycle-time, zero context alert comes in. Not the case with email alerts done correctly.
	
**"Give a Man a Phish, and You Feed Him for a Day. Teach a Man To Phish, and You Feed Him for a Lifetime."**

The barrier to entry is low. This is what you get for free. We hope you join us to build on the existing capabilities.

   - **Out of band and extremely easy to implement.** This means you can be bleeding edge with your detection, no worries of causing email disruption, the business continues as usual. Let your prevention systems do the preventions.
   - **Log rich email metadata.** JSON log format includes all aspects of the email, including attachment details, links found within the email, and all header metadata. Easily ingest into your log aggregation system.
   - **Recursive file analysis.** Supports common delivery vector file types (like doc, pdf, archive formats), easily exteded.
   - **Metrics.** Track cycle-time, events, and incidents out of the box. By dispositioning alerts based on attack phase you automatically have data on the stage of the attack reached.
   - **Custom yara rules for detection!**
   - **Alert management.** The alert, with all the analysis completed, presented to an analyst for easy disposition.
   - **Email Remediation Integration.** Integrate click button remediation of emails with O365 (PhishRemediation project).
   - **Dynamic file analysis integration.** Integrates with Cuckoo, VXStream, and Wildfire sandboxes.
   - **Link inspection integration.** Automatically analyze content of links with ACE's cloudphish (free) configuration.
   - **Integrates** with Integral's **Event Sentry** and **CRITS** for event processing and intel collection/distribution automation.
   - **Integrates with standard ACE** analysis/correlation modules which means you can **automate the ordinary**.

________________________________________________________________________________________________

### Move to Free First
#### Moving to a "Free First" approach for cybersecurity ####
Step 1: call salesperson, Step 2: get quotes, Step 3: compare functionality.

Remember the days when the strategy was to look for a commercial tool first? That strategy has led to quite a few purchases, some that we are now stuck with, some that we still get value from.

But, as I look at the opensource security system landscape, I'm thinking we need to move to a "Free First" mindset. Getting involved with opensource, seeing projects grow into extremely capable systems, and seeing how quickly they are becoming mainstream…why not take a little time to research opensource before you buy? What's the downside? For good opensource projects the time investment is relatively small. Setup a proof of concept to understand the functionality and learn how it fits into your security program (without the marketing FUD). Worst case, you become more educated and better prepared for determining the value of the commerical tools.

Maybe you are looking to buy automation tools. Maybe you are thinking about a SIEM.  

Maybe you should go "Free First".

________________________________________________________________________________________________


### Opensource is well positioned for security automation ###
Some interesting quotes about SOAR related to the opportunities, limitations for integrations, unrealized out-of-the-box value, and adoption predictions [here](https://blogs.gartner.com/anton-chuvakin/2018/02/22/our-security-orchestration-and-automation-soar-paper-publishes/)

SOAR is all about connecting systems into a cohesive process. Who is in the position to accomplish this the best? Every company has different systems they use and rely on. Who is best positioned to create the integrations & systems necessary to connect them?

I believe the teams that rely on those technologies and use them every day to accomplish a mission are in the best position to continually improve & maintain those technologies. Unfortunately, I don't believe a commercial solution is best suited to provide this. How many integrations can a commercial solution actually support, test, and maintain as systems change? How do they prioritize the integrations? How quickly can one company do this? Does it align with your needs? In my experience, this is a bottleneck to success. Conversely, this is the value of opensource; connecting not only disparate systems, but teams, your specific priorities, and processes into a cohesive solution.

We have a great foundation that supports a mature process. We've learned from and implemented systems based on both our every day experience, as well as collaboration with best in class companies. Take security collaboration to a new, meaningful level. Join us!

#opensourceftw #collaboration #improvecybersecurity #forthemasses #worktogether #flexible #ownyourprocess

________________________________________________________________________________________________

### The Process
#### The Why, and how it fits together ####
Our goal is not the creation of code, it is the streamlining of this process. With that said, to enable the capability & effectiveness of this process we have created and integrated systems. Creating smart systems to improve this process has been our key to success. 

All of the tools required to accomplish this process are now available from Integral Defense for free. Join us!

The short and skinny...

![The Process](the_process.png)

Additional details...

![More Words](details_words.png)

Where the tools fit into the process...
![Free systems and tools to accomplish the process](current_state.png)

________________________________________________________________________________________________

## Hello
#### integral systems for cyber defense ####

There are many good security tools across the computing landscape, from email, network, and endpoint, to log aggregation, machine learning, case management, vulnerability management, and many more. Connecting these systems together in an efficient and meaningful way is still a major challenge within a security ecosystem. This github site contains a variety of code, including productivity tools, integration scripts, sophisticated detection capabilities, alert management, and an analysis correlation engine (**ACE**).

Every company is different. The combination of technology stacks, attack surfaces, and threat actors are not consistent across companies. Much of the code within this repo can be easily enhanced to accommodate specific technologies and allow you to make strides towards lean, efficient processes for your security program...not to mention the killer out of the open-box capabilities!

Your friends,<br>
***Integral Defense***

_Code long and prosper_<br>
_Take a penny, leave a penny_<br>
_"For a bunch of hairless apes, we've actually managed to invent some pretty incredible things"_<br>
_"I know that the future is scary at times. But there's just no escaping it"_
