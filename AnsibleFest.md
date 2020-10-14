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

## Continuous Testing with Molecule, Ansible, and Github Actions

The earlier you catch defects, the cheaper they are to fix!

Uses a container for testing

Molecule originally built to test Ansible roles, but you can use it to test playbooks.

You can also use it to verify the yaml.

Molecule can also make sure the playbook maintains idempotency

To use as part of Github actions as easy as setting up Python to pip install molecule, yamllint, and ansible-lint.

## Blue Cross Blue Shield of North Carolina: Deliver and Deploy Infrastructure Fast with Automation

Thanks to automation - finished 9 weeks ahead of schedule, saving $850k

Important to communicate value of automation to teams.

## Red Hat Ansible Automatino Platform "NOW"

Automation is no longer a "nice to have" - it's now the industry standard.

(a big demo)

# 20201014

## The future of Red Hat Ansible Automation Platform

Ansible Automation Hub -> want to use your private roles and automation and combine it with Galaxy (community contributions). Want to give you the ability to curate it.

Portable execution environments: You use virtual environments to manage Ansible execution. They aren't very portable, though. Can cause issues. So now there are execution environments. They are container-based. 

## T-Mobile: Using automation to build and optimize networks

Important to build relationships to discuss the designs and how the playbooks should be designed

## Free Their minds: Driving culture change and workforce transformation

Sandia National Labs

They had the goals of 
- reducing heterogeneity - have all workstations configured the same
- promote security - thanks to above, easy to deal with security updates
- streamline delivery
- licecycle managment - had been missing before
- reduce low value work - get rid of the drudgery of sysadmin work

Challenges:
- Infrastructure diversity
- service diversity
- culture 
- team independence - teams are very independent. 
- duplication of work - Because of above, a lot of wasted time duplicating work
- training

Why Ansible and Tower?

At Sandia they tested Ansible, saltstack, chef, and puppet - Ansible won

### Approach

- Build a great toolbox so that people can see the benefits of Ansible
- Market a great product - get people aware that this is available; we will take care of vulnerabilities for you as they arrive.
- Target infrastructure with real impact - wanted to help the teams that needed it more. This also helps with marketing.
- Build for future needs
- Be the easy button - it has to be easy to use, well-writte, well-documented - it has to be easier than someone creating their own scripts

### Obstacles

- Don't touch my box - didn't force them. Showed the sysadmins the links to the repos. Once they saw it, they knew it would be better.
- MY CM tool is better than Ansible - we didn't insiste that Ansible replace existing CM. There were some very established Chef and Puppet CM teams. We just said - maybe you can use Ansible where it fills in the cracks.
- Policy - 
- Mavericks - just don't target these guys. Go for 80% 
- Dev groups and application owners

### Culture Change
- find a champion - what's below is the champion's duty
- communication
- relationships
- commmunity
- consensus

### Workforce Transformation
- brown bags
- demos - Cool ones! Don't do simple basics like adding a user.
- Hands on workshops
- professional training
- bounties - a team has something they need solved with ansible
- Ansible challenges

### Considerations
- Buid a comprehensive toolbox
- TEST TEST TEST TEST
- Find a champion
- Build trust
- Plan for environments with real impact - not necessarily low hanging fruit
- Middle out approach
- Lots of carrots - policy comes later
- Culture is tough to change - be patient, be a regular voice, and build a community

## Building the Next-Gen Applications for multi-cloud environments

Problem nowadays is that people want mutiple K8s clusters, including in more than once type of cloud environment.

Hybrid cloud is really hard
- error prone
- inconsisten sucurity across envs
- overwhelming to verify components, configs, policies, and compliance

k8s is initially chosen in order to have an ease of management and provisioning

Take k8s and run the OpenShift distro. Then add on the Red hat Ansible Automation Platform

Openshift is missing a bit for making it easy to be on multiple clouds, but if you add Ansible - it fills in that gap.

On OpenShift the operator Red Hat ACM calls to the Ansible Automation platform to use templates  to execute jobs. Then Red Hat ACM can see all teh Ansible stuff plus all the other stuff it normally sees.

## Live Q&A: Open Forum about the future of automation with Ansible Engineers Jason McKerr, Aaron Withrow, Adam Miller, and Richard Henshall

