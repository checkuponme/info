
# CheckUpOn.Me

Part of the [Reach4Help](https://www.reach4help.org) Family

[![CheckUpOn.Me site released under the MIT license.](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE) [![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md) [![! Security!](https://img.shields.io/badge/!-Security-red)](./SECURITY.md)

CheckUpOn.Me provides a text-distribution and outreach tool for creating connections between volunteers and people who would like to be checked in on. During the COVID-19 pandemic our goal is to help where it's needed most by connecting people who might not have others to rely on with volunteers who will have their backs.

CheckUpOn.Me provides a text-distribution and outreach tool built on top of the Open Source NodeJS project called Spoke, which is currently maintained by MoveOn.org. Spoke is a text-distribution tool for organizations to mobilize supporters and members into action. Spoke allows you to upload phone numbers, customize scripts and assign volunteers to communicate with supporters while allowing organizations to manage the process.

**We are an open project! [Learn how to contribute!](./CONTRIBUTING.md)**
[View the currently ongoing projects](https://github.com/orgs/checkuponme/projects)

* [Our Hackathon DevPost](https://devpost.com/software/checkupon-me)
* [Our Google Drive](https://drive.google.com/drive/u/3/folders/1yI3vNIrw18Ably0OlW2Si0NWnMqZfwWR)
* [Progressive Coders Project Proposal](https://github.com/ProgressiveCoders/projects/issues/160)
* [The Progressive Coders Network](https://www.progcode.org)
* [Helpful Engineering](https://www.helpfulengineering.org)
* [Functional Specification](https://docs.google.com/document/d/13fXcPPEUqrn-WzIEtGMBgIJfCJyRTFELOs2QWT_SmVc/edit#heading=h.671dnefa917m)
* [Donate!](https://opencollective.com/checkuponme)
* [Our URL Shortener - ckup.me](https://ckup.me)

## Team

|Name|Role|Info|
|-|-|-|
| [Alex Vanino](https://www.linkedin.com/in/vanino) | InfoSec, DevOps, Co-Founder | Slack: [@AlexV (CheckUpOn.Me)](https://app.slack.com/team/U010RBE7J2U), The Progressive Coders Network |
| Robert Diamond | Lead Developer, Co-Founder | The Progressive Coders Network |
| Paul Ayre | Community Outreach | |

**Special Thanks**

Stephen Scapelliti - The Progressive Coders Network

## Production Env

* Website: [https://checkupon.me](https://checkupon.me)
* App/Spoke: [https://spoke.checkupon.me](https://spoke.checkupon.me)

## Development Env

* Website: [https://dev.checkupon.me](https://dev.checkupon.me)
* App/Spoke: [https://dev-spoke.checkupon.me](https://dev-spoke.checkupon.me)

## Stack Information

* [Spoke](https://opensource.moveon.org/) - [GitHub](https://github.com/moveonorg/spoke) 
* [Politics Rewired Spoke](https://politicsrewired.com/spoke/) - [Github](https://github.com/politics-rewired/Spoke) 
* #spoke on progcode slack

## Team Standup Meetings

Agenda: [https://ckup.me/agenda](https://ckup.me/agenda)

* NA-Timezone Meeting [https://zoom.us/j/455777814](https://zoom.us/j/455777814) at 8:00PM EST every Friday and Monday
* EU-Timezone Meeting [https://zoom.us/j/225526065](https://zoom.us/j/225526065) at 11:00AM EST every Wednesday

## CheckUpOnMe Interaction Flow

![CheckUpOnMe Interaction Flow](https://checkupon.me/images/spec/DataFlowDiagram-20200326.png)

## Integration with ReachForHelp MVP

The ReachForHelp (r4h) organization has developed a strong platform for vetting volunteers and Persons In Need (PINs). This lends itself to complementary functionality, where r4h handles the creation of users, volunteers, and campaigns (geographic regions), and spoke handles workflow management and call connection.
This would be handled via service triggers built into r4h. A new user corresponds to a PIN, so will be added to campaign_contacts. As yet unanswered is how to organize campaigns in spoke, since there’s already a zip code function we should leverage that. Volunteers would be added to the users table, and assigned to teams.