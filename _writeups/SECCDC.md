---
layout: post
title: "Securing the Domain: Lessons from a Cyber Competition"
date: 2025-02-08
categories: [Security, Cyber Competition, AD Security]
tags: [Active Directory, cybersecurity, incident response, group policy]
---

# Securing the Domain: Lessons from a Cyber Competition

During a recent blue team defense competition against a professional red team, I was tasked with securing an Active Directory (AD) environment spanning eight devices. Remarkably, we only gained access to the machines the minute the competition started, which meant diving straight into the deep end. The experience was a rollercoaster of challenges, unexpected setbacks, and valuable lessons. I would like to share some of my experience with you.


## Getting Started with Account Management

The first step was to tighten up user access:

- **New User Creation:** I began by creating an additional user account for our teammates, ensuring we had a dedicated account for administrative work.
- **Locking Down Default Accounts:** I then renamed and disabled the default administrator and guest accounts to reduce potential entry points.
- **Removing Unauthorized Accounts:** I identified and deleted two unauthorized accounts that were glaringly out of place.

## Tackling Group Policy Challenges

Next, I turned my attention to Group Policy management. I attempted to edit the Group Policy Object (GPO) to apply best-practice security settings. However, I quickly encountered permission issues—something that had been predicted in our pre-competition documentation. In response, I:

- **Escalated Privileges:** Added my user to all domain management groups and updated my password.
- **Server Restart:** Despite the extra permissions, I couldn’t modify the GPO until I restarted the server, which finally allowed me to make the changes.
- **Fine-Tuning Settings:** I applied several recommended settings. One configuration—requiring LDAP signing—initially interfered with our scoring parameters, forcing me to revert that change.

## Dealing with Malicious Activities

Not all challenges were configuration-related. During the competition, I uncovered a few concerning issues:

- **Malicious Scheduled Task:** I discovered a scheduled task that ran a file named “google-updater.exe” every five minutes—remarkably, even before Chrome was installed.
- **Account Lockouts:** Our lockout policy effectively stopped brute force attempts by the red team but also led to intermittent service disruptions. For example, after a server restart, our blueteam account was locked out until the 10-minute timeout expired.
- **Rapid Response with Tools:** Quick Malwarebytes scans helped identify and remove malware, while “Everything Search” allowed me to hunt down and delete an out-of-place “goose” program that could have complicated later stages of the competition.
- **Live Process Monitoring:** Towards the end, I used Taskexp.exe to monitor live processes and terminate remote shells as they appeared.

## Unforeseen Technical Intricacies

One of the more unexpected challenges was handling injection attacks. This year’s injects were notably more technical:

- **DNS Zone Transfer Verification:** A question about zone transfer attacks on DNS prompted me to verify our deployment. Since our single-point DNS server did not allow zone transfers—and such transfers weren’t necessary—our system remained secure. I confirmed this by checking the Event Viewer for DNS event IDs (6001-6004, 6527) and found no anomalies.

## Lessons Learned and Future Directions

Reflecting on the competition, I believe we did a solid job securing the AD system, despite a few hiccups. However, there are key areas for improvement:

- **Remote Management:** Our other Windows machines got locked out during the process. Learning how to manage these machines remotely via the domain controller could be a game changer.
- **Eliminating Persistence:** Although I removed multiple forms of malicious persistence, the red team managed to reintroduce a previously deleted “google-updater.exe.” This underscores the need for deeper research into Windows persistence techniques—like the use of malicious DLLs and disguised scheduled jobs.
- **Firewall Enhancements:** While I added firewall rules to block unnecessary traffic (for example, shutting down ports 22 and 23 and disabling IPv6 traffic), I recognize that there’s more to explore, especially as IPv6 becomes more prevalent.

These three areas—remote management, persistence elimination, and firewall control—will be my major focus for future competitions

## Final Thoughts

This competition was both challenging and incredibly instructive. Every hurdle, from permission issues to unexpected malicious activity, reinforced the importance of continuous learning and proactive security measures. As I work toward refining these skills, I look forward to applying these insights in future challenges and beyond. Despite not making it to regionals, the lessons learned were significant, and our 11th place finish out of 38 teams was impressive.

