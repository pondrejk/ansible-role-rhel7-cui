Unclassified Information in Non-federal Information Systems and Organizations (NIST 800-171)
=========

Ansible remediation role for profile nist-800-171-cui  
Profile Title:  Unclassified Information in Non-federal Information Systems and Organizations (NIST 800-171)  
Profile Description:  
From NIST 800-171, Section 2.2:  
Security requirements for protecting the confidentiality of CUI in nonfederal   
information systems and organizations have a well-defined structure that   
consists of:  
  
(i) a basic security requirements section;  
(ii) a derived security requirements section.  
  
The basic security requirements are obtained from FIPS Publication 200, which  
provides the high-level and fundamental security requirements for federal  
information and information systems. The derived security requirements, which  
supplement the basic security requirements, are taken from the security controls  
in NIST Special Publication 800-53.  
  
This profile configures Red Hat Enterprise Linux 7 to the NIST Special  
Publication 800-53 controls identified for securing Controlled Unclassified  
Information (CUI).  
  
  
Benchmark ID:  RHEL-7  
Benchmark Version:  0.1.38  
  
XCCDF Version:  1.1  
  
This file was generated by OpenSCAP 1.2.17 using:  
	$ oscap xccdf generate fix --profile nist-800-171-cui --template urn:xccdf:fix:script:ansible xccdf-file.xml   
  
This script is generated from an OpenSCAP profile without preliminary evaluation.  
It attempts to fix every selected rule, even if the system is already compliant.  
  
How to apply this remediation role:  
$ ansible-playbook -i "192.168.1.155," playbook.yml  
$ ansible-playbook -i inventory.ini playbook.yml

Requirements
------------

N/A

Role Variables
--------------

To customize the role to your liking, check out the [list of variables](vars/main.yml).

Dependencies
------------

N/A

Example Playbook
----------------

Run `ansible-galaxy install Ansible-Security-Compliance.rhel7-role-nist-800-171-cui` to
download and install the role. Then you can use the following playbook snippet.


    - hosts: all
      roles:
         - { role: Ansible-Security-Compliance.rhel7-role-nist-800-171-cui }


Then first check the playbook using (on the localhost):

    ansible-playbook -i "localhost," -c local --check playbook.yml

To deploy it, use (this may change configuration of your local machine!):

    ansible-playbook -i "localhost," -c local playbook.yml


License
-------

BSD-3-Clause

Author Information
------------------

This Ansible remediation role has been generated from the body of security policies developed by the SCAP Security Guide project. Please see https://github.com/OpenSCAP/scap-security-guide/blob/master/Contributors.md for an updated list of authors and contributors.
