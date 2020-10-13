# 20201013

## Keynote: Collaborating at Scale: Connecting the growing ansible community through innovation and change

Part of Ansible's success being built on a modular architecture which made it easier to get started, use, and contribute. 

Now things have grown. How can they continue to have contributors? They've modularized even more via Collections. (important as any project grows)

In Ansible 2.10 (batteries still included - but optional (via collections))

## Adapting to change with automation

Ansible collections plus OpenShift help make it work better across clouds

## CarMax: Driving Efficiency and Innovation with Ansible

### People

What do you need to do to get buy-in? Are your people trained well? 

Good thing about the way Ansible playbooks are written, it's got a very low learning curve. It's written more like English than bash or Powershell Scripts.

They can help to speed up adoption of automation.

### Processes

How well are your processes documented? 

What processes does your org have in place?

### Technology

How will success be measured?

### DevOps

This allows the devs not to have to worry about the environments being set up correctly.

## Case Study: Defending a Defense Company with Ansible Automation

Presenter has been using ansible for 6months

Practices Ansible in his homelab (!)

### The Problem

Large Defense Contractor

- massive global routing, switching firewall devices
- backup management
- configuration management
- auditing privileged accounts
- quick, secure, and efficient changes

There's also a bunch of "islands of security" that require maintenance, management, and auditing

eg docker, jenkins, aws, azue, Ansible, OpenShift, kubernetes

This means there's LOTS of creds to manage and that can be untenable.

### Networking 101

NIST recommends Zero Trust - always assume you have to verify users

- Switch - connecting everything
- Routers - routing the traffic everywhere throughout the network
- firewalls - in the past relied on this to keep the bad guys out

### Real-World Use Cases

Backup of Configs - why?
- hardware goes bad
- disaster recovery/business continuity

Standardization and Compliance
- Automate Firemware Upgrades - need to make sure the firmware on all network devices up to date because of attacks
- Leverage NAC (network access control) - make sure automated and using ZeroTrust 
- Device agnostic! - Can be utilized with over 24 platforms!

### Solution - use what you already own

They had a Central Redential Provider, Cisco Identity Serivces Engine, and Red Hat Ansible Tower

(see Slide of how it Works)

CyberArk provides Creds to Ansible. 

### Business Benefits

- He was able to reach and update all the devices without having to do it manually
- security happy because creds aren't in any scripbs
- ops happy because it didn't affect OpenShift


## Live Q&A: Efficiently scaling automation across your organization

Q: Best size team for a POC to show how automation will help the larger office?
A: It depends. Start small and break things into small chunks. Show successes often. Smaller allows you to focus so you don't have to focus on external dependencies as much. 

Q: As a small IT organization how can we overcome an engr department that has 0 trust in ops team?
A: Start small to build the trust. Maybe use a side project to show them the value of what you're doing - maybe show a quick automation.

Q: Now that Ansible includes collections - what's the best way to build a centralized repo for it?
A: Git

Q: How to include Windows in Ansible Automation
A: It works well with Windows already!

Missed question, but answer - need to make sure you use source control for your playbooks. It really is part of the core of the way Ansible operates.

Q: Ansible is popular in my place. Everyone wants to be on Tower. How do help spread this throughout the whole organization?
A: Tower has organization and RBAC. Give each group control over their own "destiny" rather than trying to control it. If they don't need approvals, they will get a lot mroe out of Ansible.

Q: A bunch of orgs did it independently. How do you bring it all together?
A: Part is the answer to the previous question. And part of it is having community standards/governance.Eg: syntax, how to group playbooks, etc
