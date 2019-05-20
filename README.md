# Ansible Tower Post Provisioning API Call Example

Any Job Template in Ansible Tower can be called via a Post Provisioning API. This is done so that at build time (end of the build) you can run a first playbook. 

## Getting Started

Visit a Job Template and look for the "Allow Provisioning Callbacks" checkbox. Make note of the Provisioning Callback URL. Use the magic wand to set a Host Config Key (or just make one up.)

## Usage

The Provisioning Callback URL also provides an example. Click on the Question Mark (?) help icon and you should see cut and pasteable text that looks like this:
```bash
curl --data "host_config_key=POST_PROVISION" https://tower.example.org:443/api/v2/job_templates/123456/callback/
```
