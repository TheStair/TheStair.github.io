---
layout: default
title: "My Experience at DOE Cyberforce 2024"
date: 2024-11-08
categories: [Security, Cyber Competition, AD Security]
tags: [Active Directory, cybersecurity, incident response, group policy]
---
# Department Of Energy's CyberForce; What You Need to Know

I was granted the priviledge to participate in the 2024 Department of Energy's Cyberforce Competition. This competition was very time consuming, but it provided some great experience in day-to-day business interactions of Cybersecurity Engineers. This competition lasted around 4 weeks with various scored tasks prior to the in-person competition in St. Charles Illinois.

## C-Suite Briefing
Around four weeks prior to the in-person event, teams were given a brief overview of the impacts of a recent cybersecurity incident to an energy company's bottom line. With this information, teams were tasked with submitting a video providing suggestions for mitigations. With a specific emphasis on cost and non-technical language. Teams had to explain the cost vs. risk benefits for their proposed security mitigations in a manner a non-technical business administration team could understand.  
This challenge is unique, in that teams have no technical details regarding the attacks, but still have to propose solutions. In this case, my team heavily pushed for Multi-Factor Authentication (MFA) with DUO and Cybersecurity Awareness trainings for Employees. We argued that Phishing, especially without 2FA, are statistically significant threats to modern corperations. Many recent major Cyberattacks are due to either social engineering, a lack of MFA, or both \([See MGM Hack](https://blog.1password.com/mgm-hack/)\). We also proposed the idea of an independant cybersecurity firm to audit the businesses systems, but noted the high-cost of this solution.  
We made it clear that without proper mitigations, this energy company could continue to see degraded output, damage to the company's bottom line, and irreversible damage to the company's reputation with customers. So, depending on the interal specifics of the attack, the high cost solutions may be worth the investment.

## C-Suite Documentation
After Teams Submitted their C-Suite Briefings, we were finally granted access to the competition network. The machines were divided into two groups; "Traditional" and "Assumed Breach". Where traditional machines could be modified, changed, and hardened while the assumed breach machines were not to have security settings tampered with.  
Teams were then tasked to write network documentation for the C-Suite. We had to create a network map, specify the importance and use of each machine, document vulnerabilities and explain mitigations. This forced teams to develop a deep understanding of the network's current functionality, what security vulnerabilities are present, and what machines are more critical than others.  
Competition Organizers heavily emphasized that a failure to actually understand the state of the network, it's functiona, and it's security would be very obviously reflected in these reports.  

## Pre-Competition Flags
Something new introduced this year were pre-competition flags. These flags were found in the competition machines and typically denoted poor security practices. Whether it's a password in a user's note box, PII, or anything else, there were a handful of flags to hunt down.

## Final Competition Prep
Teams were also given specifications for critical services that needed to be brought up prior to competition. This year, this consisted of creating a website from a provided template, but ensuring functionality and bringing it up to specifications. There was also a machine that managed the PLCs for "wind turbines".

## Competition Day
The in-person competition consisted of a few moving parts: Traditional Red-Blue Defense, Incident Response, and CTF Puzzles.

- **Red-Blue Defense:**  We had to ensure our critical services were functional and available while a red-team actively attempted to bring them down.

- **Incident Response:** Throughout the day, the competition organizers ran scripted events on our "Assumed Breach" Machines that we had to respond to. The organizers heavily emphasize proof of incident and the inclusion of the CVE used.

- **CTF Puzzles:** While both the Red-Blue Defense and Incident Response Challenges were occurring, we also had CTF Puzzles to solve. These puzzles included software reverse engineering (including powershell de-obfuscation), Open-Source Intelligence (OSINT), Trivia, Password Cracking, and more.

This was a lot to handle in that action-packed 8 hour window. Something we definitely could have prepared better for were the CTF Challenges. According to my teammates who particpated in the previous year, the puzzles were significantly more difficult. We could have placed a bit higher if we prepared better for the CTF challenges.

# Conclusion
Cyberforce was a lot of fun and I learned a ton. I think the inclusion of non-technical communication soft skills are a vital area in the day to day life of cybersecurity professionals. I mainly focused on Windows Server and CTF Puzzles during the competition. Our hard work paid off and we placed 15th out of the 94 teams competing! That was a 26 place improvement over my university's team the previous year.