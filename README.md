# [CheckUpOn.Me](https://checkupon.me)

Part of the [Reach4Help](https://www.reach4help.org) Family

[![CheckUpOn.Me site released under the MIT license.](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE) [![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md) [![! Security!](https://img.shields.io/badge/!-Security-red)](./SECURITY.md)

![CheckUpOn.Me](https://checkupon.me/images/promo/Banner1.png)

[CheckUpOn.Me](https://checkupon.me) provides a text-distribution and outreach tool for creating connections between volunteers and people who would like to be checked in on. During the COVID-19 pandemic our goal is to help where it's needed most by connecting people in need with volunteers who will be ready to take action.

Our outreach platform is built with open source tools such as Nodejs, React, PHP, and Linux. Our platform helps organizations mobilize supporters and members into action and allows us to manage lists of contacts, customize scripts and assign volunteers to communicate with supporters while allowing organizations to manage the process.

**We are an open project! [Learn how to contribute!](./CONTRIBUTING.md)**

We would love to hear from you! 
[Join us on slack!](https://ckup.me/slack) Join channel #team-checkuponme

[View the currently ongoing projects](https://app.zenhub.com/workspaces/checkuponme-5e8e3956beee58232ea519a4/board?repos=252629679,252606726,250885954,249560771)

## Links

* [Please donate so that we can keep operating!](https://opencollective.com/checkuponme)
* [Project Overview and Functional Specification](https://docs.google.com/document/d/13fXcPPEUqrn-WzIEtGMBgIJfCJyRTFELOs2QWT_SmVc)
* [Our User Manual and Demo Screenshots](./SPOKE_GUIDE.md)
* [Our Hackathon DevPost](https://devpost.com/software/checkupon-me)
* [Our Google Drive](https://drive.google.com/drive/u/3/folders/1yI3vNIrw18Ably0OlW2Si0NWnMqZfwWR)
* [Progressive Coders Project Proposal](https://github.com/ProgressiveCoders/projects/issues/160)
* [The Progressive Coders Network](https://www.progcode.org)
* [Helpful Engineering](https://www.helpfulengineering.org)
* [Our URL Shortener - ckup.me](https://ckup.me)

## Our Team

| Name                                              | Role                        | Info                                                         |
| ------------------------------------------------- | --------------------------- | ------------------------------------------------------------ |
| [Alex Vanino](https://www.linkedin.com/in/vanino) | InfoSec, DevOps, Co-Founder | Slack: [@AlexV (CheckUpOn.Me)](https://app.slack.com/team/U010RBE7J2U), The Progressive Coders Network |

### Special thanks to

- [Ben Chrobot](https://www.linkedin.com/in/benjaminchrobot/) of [Politics Rewired](https://politicsrewired.com/) for all of the help he has given us with getting out spoke instance up and running. 
- [Pedro Filipe and Shayan Chowdhury and the rest of the Reach4Help team](https://github.com/reach4help/reach4help/blob/master/docs/TEAMS.md) for their ongoing support and awesomeness.
- [Stephen Scapelliti](https://www.linkedin.com/in/stephen-scapelliti/) of the [Progressive Coders Network](https://www.progcode.org) for helping advise on different legal and organizational processes.
- [Robert Diamond](https://www.linkedin.com/in/rmd6502/) of the [Progressive Coders Network](https://www.progcode.org) for all of his help with spoke.

### Team Standup Meetings

Open Standups: 8:00PM EST every Tuesday and 11:00AM EST every Thursday.

- Agenda: https://ckup.me/standup-agenda
- Video Call: https://ckup.me/standup-video
- Dial-In: https://ckup.me/standup-dialin

### We're looking for help!

While we are certainly open to all forms of help, we are currently looking for people to fill the following high priority roles:

#### Engineering

- Frontend and backend developers with Twilio, NodeJS, React, Graphql and responsive web design experience.
- Site Reliability / DevOps Lead

#### People Operations

- Coordinators with experience managing large groups of volunteers remotely
- Talent Recruiter
- Local coordinators to help manage things on the ground in specific areas. People around major cities are most needed right now
- Outreach Volunteers that will be the core of our platform. These volunteers will communicate with people in need through our SMS messaging platform.

#### Org Operations

- Social media, hackathon presence, marketing and PR specialists
- Funding and Donor coordinator - Network and manage our relationships with donors and funding sources
- Partner organization coordinator - Manage our relationships with other organizations
- Financial Bookkeeper

These are all positions that have the possibility of evolving into part time or full time paid opportunities as more funding becomes available. If you feel that you would excel in any of those roles, feel free to drop by our slack channel: https://ckup.me/slack **#team-checkuponme** and introduce yourself or [apply here](https://forms.gle/ycgn3i5AeJiWk4S58).

## Funding

We are currently incorporating as a corporation within the United States for funding purposes. We’ve already been rewarded with over $10,000 (Thanks to HWC, AWS, GCP, and Twilio) in funding and expect more funding where that came from. We are fully transparent with our donations and funding. 

We are on Open Collective: https://opencollective.com/checkuponme 

[Please donate so that we can keep operating!](https://opencollective.com/checkuponme)

We’re currently exploring opportunities for further funding our project. We’re mainly operating off personal development machines (Hosted on developers personal internet connections) and free Heroku services which I’m afraid won’t be maintainable once we go live. We are also developing all tech solutions in house or using open source solutions. Finally no one, including myself is being paid for any of the work we are putting into this project. It is truly a project of passion.

Because of the work we are putting forward in solving a major issue during this pandemic, we are looking for assistance with obtaining funding via operating grants or outside investors so that we may continue to operate and continue providing valuable services to the community.

## Development Information

### Production Env

* Website: [https://checkupon.me](https://checkupon.me)
* App/Spoke: [https://spoke.checkupon.me](https://spoke.checkupon.me)

### Development Env

* Website: [https://dev.checkupon.me](https://dev.checkupon.me)
* App/Spoke: [https://dev-spoke.checkupon.me](https://dev-spoke.checkupon.me)

### Stack Information

* [Spoke](https://opensource.moveon.org/) - [GitHub](https://github.com/moveonorg/spoke) 
* [Politics Rewired Spoke](https://politicsrewired.com/spoke/) - [Github](https://github.com/politics-rewired/Spoke) 
* #spoke on progcode slack

### CheckUpOnMe Interaction Flow

![CheckUpOnMe Interaction Flow](https://checkupon.me/images/spec/DataFlowDiagram-20200326.png)

### Integration with ReachForHelp MVP

The ReachForHelp (r4h) organization has developed a strong platform for vetting volunteers and Persons In Need (PINs). This lends itself to complementary functionality, where r4h handles the creation of users, volunteers, and campaigns (geographic regions), and spoke handles workflow management and call connection.
This would be handled via service triggers built into r4h. A new user corresponds to a PIN, so will be added to campaign_contacts. As yet unanswered is how to organize campaigns in spoke, since there’s already a zip code function we should leverage that. Volunteers would be added to the users table, and assigned to teams.
