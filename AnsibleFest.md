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
