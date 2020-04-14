# [CheckUpOn.Me](https://checkupon.me)

Part of the [Reach4Help](https://www.reach4help.org) Family

[![CheckUpOn.Me site released under the MIT license.](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE) [![PRs welcome!](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md) [![! Security!](https://img.shields.io/badge/!-Security-red)](./SECURITY.md)

[CheckUpOn.Me](https://checkupon.me) provides a text-distribution and outreach tool called Spoke for creating connections between volunteers and people who would like to be checked in on. During the COVID-19 pandemic our goal is to help where it's needed most by connecting people in need with volunteers who will be ready to take action. This user manual will go over the basic operating details for Spoke. This documentation and the Fork of spoke we are using was **heavily** influenced by our [upstream](https://politicsrewired.com/spoke/).

![Spoke](https://checkupon.me/docs/images/spoke.png)

# Table of Contents

* [Getting Started with Spoke](#getting-started-with-spoke)
   * [Using this documentation](#using-this-documentation)
      * [Administrators](#administrators)
      * [Texters / Volunteers](#texters--volunteers)
   * [Dashboards](#dashboards)
      * [Administration dashboard](#administration-dashboard)
      * [Texter dashboard](#texter-dashboard)
* [Administering Spoke](#administering-spoke)
   * [Invite texters to Spoke](#invite-texters-to-spoke)
   * [Assign user roles](#assign-user-roles)
   * [Create a team](#create-a-team)
   * [Organizations](#organizations)
* [Concepts](#concepts)
   * [Campaigns](#campaigns)
   * [Interaction scripts](#interaction-scripts)
   * [Assignments](#assignments)
   * [Teams](#teams)
   * [Contact overlap management](#contact-overlap-management)
   * [Canned responses](#canned-responses)
   * [Texting hours](#texting-hours)
   * [Due dates](#due-dates)
   * [Contact lists](#contact-lists)
   * [CSV Format](#csv-format)
   * [Uploading contact lists](#uploading-contact-lists)
   * [Filtering existing campaigns](#filtering-existing-campaigns)
   * [Conversation tags](#conversation-tags)
   * [Bulk script editor](#bulk-script-editor)
   * [Short-link domains](#short-link-domains)
   * [Settings](#settings)
   * [Opt-out message](#opt-out-message)
   * [Texting hours](#texting-hours-1)
   * [Assemble Numbers API key](#assemble-numbers-api-key)
   * [Sending locations](#sending-locations)
   * [Send Status](#send-status)
   * [User Roles](#user-roles)
* [Managing campaigns](#managing-campaigns)
   * [Create a new campaign](#create-a-new-campaign)
   * [Create an interaction script](#create-an-interaction-script)
   * [Colors and tags for active campaigns](#colors-and-tags-for-active-campaigns)
   * [Color coding](#color-coding)
   * [Tags](#tags)
   * [Reassign conversations to texters](#reassign-conversations-to-texters)
   * [From the message review page](#from-the-message-review-page)
   * [From the escalated conversations page](#from-the-escalated-conversations-page)
   * [From the campaign list](#from-the-campaign-list)
   * [Export data from a campaign](#export-data-from-a-campaign)
   * [Campaign actions](#campaign-actions)
* [Spoke Contact Tool Guide](#spoke-contact-tool-guide)
* [Text a contact](#text-a-contact)
   * [Send initial messages](#send-initial-messages)
   * [Send replies](#send-replies)
   * [Request texts for assignment](#request-texts-for-assignment)
   * [Add tags to a conversation](#add-tags-to-a-conversation)
   * [Opt out a contact](#opt-out-a-contact)
   * [Use a canned response](#use-a-canned-response)
   * [Skip a reply](#skip-a-reply)
   * [Escalate a conversation](#escalate-a-conversation)
   * [Include an image in a message](#include-an-image-in-a-message)
* [Appendix](#appendix)
   * [Timezone Reference](#timezone-reference)

# Getting Started with Spoke

To get started with this guide you will need access to a spoke instance. You can either set one up yourself with the directions in the spoke repo or you can drop in on [slack](https://ckup.me/slack) and request access to one of our instances.

Through Spoke, you can organize texting [campaigns](#campaigns), which provide the structure and tools needed to connect [texters](#spoke-contact-tool-guide) in your organization with your contacts. Spoke is meant to be used in combination with a CRM. Spoke is not a CRM and should not be used as one.

Spoke's key features include:

- Messaging platform with script and survey integration
- Interaction script and survey editing
- Auto, dynamic, and manual conversation assignment
- Automatic handling and processing of your contact lists
- Opt-out handling

## Using this documentation

The documentation that you find on this website is intended for both Spoke administrators and texters. We recommend that you browse the collections of articles listed below or that you visit [Dashboards](#dashboards).

#### Administrators

If you are an administrator, we recommend looking through the following categories:

- [Getting started with Spoke](#getting-started-with-spoke) -- Introductory articles about first steps with Spoke
- [Administering Spoke](#administering-spoke) -- Guides for administrators to set up user accounts and other {administrator things}
- [Managing campaigns](#managing-campaigns) -- Guides for administrators to create and manage texting campaigns
- [Concepts](#concepts) -- Articles describing the different components you'll find Spoke

#### Texters / Volunteers

If you are a texter, we recommend looking through the following categories:

- [Getting started with Spoke](#getting-started-with-spoke) -- Introductory articles about first steps with Spoke
- [Texting contacts](#spoke-contact-tool-guide) -- Guides for texters to use the Spoke messaging application
- [Concepts](#concepts) -- Articles describing the different components you'll find in Spoke

## Dashboards

### Administration dashboard

The administration dashboard lets you manage your Spoke [organization](#organizations). From the administration dashboard, you can access the following:

- [Campaigns](#campaigns)
- [User roles](#user-roles)
- [Teams](#teams)
- [Assignments](#assignments)
- [Interaction scripts](#interaction-scripts)
- [Short-link domains](#short-link-domains)
- [Settings](#settings)

You must be an [administrator or owner](#user-roles) for your Spoke organization to use the administration dashboard. To access the administration dashboard, use the following URL: 

https://spoke.checkupon.me/admin/organization-number

Where *organization-number* is the number assigned to your Spoke organization.

![Admin Dash](https://checkupon.me/docs/images/admin.png)

### Texter dashboard

The texter dashboard lets you request texts and send messages to any conversations assigned to you. You must have a user account with your Spoke organization to use the texter dashboard.

To access the texter dashboard, use the following URL:

https://spoke.checkupon.me/app/organization-number

Where *organization-number* is the number assigned to your Spoke organization.

# Administering Spoke

## Invite texters to Spoke

You invite texters to Spoke by sending them a invitation link. When someone clicks on the link, they can create a texter account. After texters create their accounts, you can assign user roles to them.

To invite texters to join your organization on Spoke:

1. From the administration dashboard, navigate to the **People** page.
2. Click the **Add** button.
3. Copy the URL.
4. Share the URL with the texters you want to invite.

When someone clicks on the link, they will be able to create an account.

![Invite](https://checkupon.me/docs/images/invite.png)

## Assign user roles

[User roles](#user-roles) can be assigned from the "People" page of the [administration dashboard](#dashboards). After you [invite texters](#invite-texters-to-spoke) to your Spoke organization, users are automatically listed with the default **Texter** role.

To change a user's role:

1. From the "People" page, click the arrow next to the role name.
2. Select a new role. For more information about the different user roles, see [User roles](#user-roles).

![People](https://checkupon.me/docs/images/people.png)

## Create a team

Teams let you group the texters in your organization based on some factor, such as specialization, skillset, or location.

To create a team:

1. From the [administration dashboard](#dashboards), navigate to the "Teams" page.
2. Click **Add**.
3. Enter a team name.
4. Enter a description for the team.
5. Enter an assignment priority value for the team. The lower the number, the higher the priority.
6. Click **Create**.

![Create Team](https://checkupon.me/docs/images/createteam.png)

To add texters to a team:

1. Select the team from the team list.
2. Enter a texter's name in the **Add Texter** field.
3. Select the name from the list.

![Add Team Members](https://checkupon.me/docs/images/addteam.png)

## Organizations

Each instance of Spoke can have multiple organizations. An organization is a distinct sending identity within your Spoke instance.

Organizations are useful when your texting goals are different enough to split up.

Each organization has a separate:

- Pool of phone numbers for sending messages (for example, when different lists would be sent by two separate numbers)
- Opt-out list (for example, this would allow a contact to opt-out of specific lists).

The organization is defined by a number, which is visible in the URL of both [dashboards](#dashboards).

# Concepts

## Campaigns

Campaigns are the central feature of Spoke. They provide the structure and tools for [texters](#user-roles) to engage in conversations with your contacts.

Each campaign has a contact list and an [interaction script](#interaction-scripts). When you start a campaign, contacts are assigned to texters, who can then initiate a conversation using the interaction script. 

A campaign should have a single purpose -- for example, to inform your contacts of an event or to ask about issue priority -- so that you can tailor your interaction script to properly convey that information. You can run multiple campaigns simultaneously to reach your contacts about different things.

If you are a Spoke administrator, you can manage campaigns from the [administration dashboard](#dashboards).

![Campaign](https://checkupon.me/docs/images/campscreen.png)

## Interaction scripts

Interaction scripts define conversation flow and survey questions. They are used by [texters](#user-roles) to send prepared messages to contacts and to record answers to the survey questions. Each campaign has an interaction script that can be written and edited on the campaign settings page. Only administrators can edit the script.

An interaction script has three parts:

- An initial message that a texter sends out to kick off a conversation
- A set of follow-up messages that can vary depending on how a contact replies
- A set of survey questions and answers that texters use to record information about the contact

To minimize the chance that your messages are flagged as spam by a carrier as spam, you can write multiple versions of the message that are randomly distributed across the conversations.

In case the conversation departs from the interaction script, you can provide [canned responses](#canned-responses) that texters use to handle the situation on a case-by-case basis.

![Interaction Scripts](https://checkupon.me/docs/images/question-script.png)

### Images

You can include images in the interaction script by surrounding an image URL with square brackets, [ ]. For example: `[https://image-url.com/image-is-here]`.

Any text before and after the bracketed URL is combined into a single message with the bracketed URL removed.

## Assignments

There are three ways to assign conversations to texters. All three are available in the campaign settings page. For more information about assigning conversations to texters, see [Create a new campaign](#create-a-new-campaign).

### Manual assignment

Administrators can manually assign texts to individual texters from the "Texters" window of the campaign settings page. Depending on how many texters you use with manual assignment, this can be a time-intensive process. We recommend using dynamic assignment or auto-assignment, unless you have a special case that requires manual assignment.

### Dynamic assignment

Dynamic assignment provides an assignment link that administrators can share with texters. This method of assignment is useful for assigning conversations to a certain group, as you can share the link on a mailing list or in a Slack channel.

### Auto-assignment

Auto-assignment allows texters to request a number of conversations from the texter [dashboard](#dashboards). This is the most hands-off version of assignment.

After texters make their requests, administrators must approve the requests from the "Assignment Requests" page of the administration dashboard.

![Assignment](https://checkupon.me/docs/images/Assignment.png)

## Teams

Teams are groups of texters in your organization. Teams provide a method of designating texters for special cases or with different skillsets. For example, you can assign a team of Spanish-speaking texters to a campaign that reaches out to Spanish-speakers.

Each team is defined by the following:

- **Name** -- The name of the team. When you assign a team to a campaign, you use the team name.
- **Description** -- A description of the team. Use this to keep track of your teams.
- **Priority number** -- The priority number used to determine conversation assignment for team members. The lower the number, the higher the priority.

![Teams](https://checkupon.me/docs/images/teams.png)

## Contact overlap management

Contact overlap management is a step in [creating a campaign](#create-a-new-campaign). This window in the campaign settings page displays the number of contacts that overlap with other campaigns. From the window, you can removing overlapping contacts from this campaign to avoid having simultaneous conversations with your contacts. 

When you upload a contact list to a campaign, Spoke automatically detects overlapping contacts. It's best to remove overlapping contacts, except in the unusual case that you want to bother them about multiple things at once. You can do this by clicking the trash icon. 

> Note: Different campaigns text contacts from the same number, which can lead to confusion if you have simultaneous conversations.

## Canned responses

Canned responses are an additional set of prepared messages that texters can use if a conversation deviates from the interaction script. Spoke administrators can create canned responses to handle a variety of situations. They can do this from the campaign settings page while creating or editing a campaign. 

Texters can access canned responses while in a conversation, as shown in the following image:

![Canned Responses](https://checkupon.me/docs/images/cannedres.jpg)

## Texting hours

Texting hours restrict when [texters](#user-roles) can send messages to contacts. Using texting hours minimizes the chance of disturbing someone at inappropriate hours of the day. Spoke's default texting hours have been chosen to comply with regulation regarding consumer telephone contact. **We do not recommend extending these hours** and you do so at your own risk.

Texting hours are defined in the [campaign settings page](#settings) by a start time, an end time, and a default time zone. The time zone for a contact is determined by their zip code. If a contact does not have a zip code, the default time zone is used.

Outside of texting hours, Spoke disables the **Send** and **Send Replies** buttons in the texter to-do list. If you try to send a message outside of the designated texting hours, the text will not send, and you'll receive an error.

## Due dates

Every campaign has a due date that you specify on the campaign settings page. After the due date passes, texters can no longer send initial messages to contacts. This prevents you from accidentally starting a conversation regarding an outdated topic, such as information about an event that has already happened. 

Texters can continue ongoing conversations after the due date. A campaign ends only when you archive it.

## Contact lists

Contact lists are part of every campaign. The contact list provides the full list of people you wish to contact for that campaign. You must provide the contact list in a comma separated values (CSV) format.

Once uploaded to the campaign, Spoke maintains an internal version of the list and modifies it as the campaign progresses. You can export the modified contact list for your own record keeping. For more information, see [Export data from a campaign](#export-data-from-a-campaign).

## CSV Format

Your contact list should be a comma separated values (CSV) file with the following column headings in the first row:

- **firstName** -- (Required) First names of your contacts.
- **lastName** -- (Required) Last names of your contacts.
- **cell** -- (Required) Cell number of your contacts.
- **zip** -- (Optional) Zip code of your contacts. If you don't provide a value for timezone, the zip code is used to estimate your contact's timezone.
- **timezone** -- (Optional) Timezone of your contacts. This is used to enforce [texting hours](#texting-hours). You can find a list of time zones in the [Time zone reference]().
- **external_id** -- (Optional) ID to map your contacts to a CRM.

*NOTE:* The **firstName** and **lastName** fields will be automatically capitalized for all values other than common placeholders for unknown names: "friend" and "there".

#### Custom fields

You can include additional, custom fields in the contact list. You can use these fields in the campaign's [interaction script](#interaction-scripts), similar to the **firstName** and **lastName** fields.

## Uploading contact lists

You can upload contact lists from the campaign settings page. To start a campaign, you must provide an initial contact list. 

> Note: If you upload another contact list, it removes all previously uploaded contacts and replaces them with the most recent contact list.

When you upload a contact list, Spoke performs two rounds of processing. The first round, which happens in the Spoke application, handles the following for that contact list:

- The removal of duplicate contacts (duplicates are determined based on phone number; the first instance is kept).
- The removal of contacts without phone numbers.
- The removal of contacts with invalid phone numbers.

After you click **Save**, the second round handles the following for the campaign's complete contact list:

- The removal of all contacts that have opted out.
- The removal of all contacts from campaigns that you specified in **Filter Existing Campaigns** (see below).
- Automated filtering can be done with [Assemble Numbers](#assemble-numbers-api-key).

![Filtering](https://checkupon.me/docs/images/filter.png)

Any automated handling of your contact list is detailed in the upload report. You can view the upload report from the contacts window of the campaign settings page.

## Filtering existing campaigns

You can choose to filter contacts that are already contacts in another campaign. This helps you prevent sending too many messages to a contact or sending redundant information from two similar campaigns.

When uploading contact lists to a campaign, enter the names of the campaigns that are used to filter out contacts. You can enter multiple campaign names at once.

## Conversation tags

Conversation tags are used by texters to attach additional information to a conversation or contact. 

> Note: Conversation tags apply only to the current conversation and do not persist across campaigns.

You can use conversation tags to provide more information about the contact, such as their primary language. For example, a texter could tag a conversation with "Language: Spanish". When you export data from the campaign, you can update your CRM with this information to ensure that the contact is messaged in Spanish in future conversations.

## Bulk script editor

The bulk script editor is a tool that allows you to find and replace parts of your interaction scripts across multiple campaigns. With this tool, you provide the text you want to replace and the text you want to replace it with. The editor searches all campaigns in your organization and performs the replacement for all interaction scripts. 

You can use a filter to restrict the replacement to a smaller set of campaigns. A filter can restrict the editor to active campaigns and to campaigns with names that begin with specific text.

To use this tool, you must provide the exact text you want to replace. If your interaction scripts all have slight variations, the bulk script editor must be used for each variation. Keep this in mind when writing interaction scripts.

If you leave the **Replace with** field blank, the bulk script editor replaces all instances of the text with nothing, effectively deleting them.

The bulk script editor works only for a single Spoke [organization](#organizations). If you have multiple organizations, you must use the bulk script editor for each one.

> Note: Clicking the **Find & Replace** button performs the action without confirmation. Click this button only after you've double-checked the text, filters, and other options.

After you use the bulk script editor, a notification displays all instances (or occurrences) of replacement. Once you exit this notification, you cannot open it again. If you want to save the details of the replacements, copy them before clicking **Ok**.

## Short-link domains

Short-link domains let you minimize the chance that your messages with links are blocked by carriers. Short links are one of the more common reasons why carriers block messages. Spoke can interface with link shortening services to replace a short link's domain with one that isn't blocked by carriers. 

You can add to a list of short-link domains from the [administration dashboard](https://docs.spokerewired.com/article/52-dashboards). When a texter sends a message that includes a shortened link, Spoke uses this list to automatically detect and replace the short link's domain with another domain in the list. Spoke cycles through the domains in this list to spread out usage of the domains. The **Maximum** **usage** setting for a domain specifies the number of times Spoke will use that domain before moving on to the next one.

You must set up the short links outside of the Spoke application, and they must resolve to the same end location for the domain replacement to work. 

> Note: If you don't set up short links outside of the application, the links you send out will not work as expected.

Spoke can detect only the domains you've added to the short-link domain list. URLs with other domains will not be replaced.

## Settings

The following settings apply to all campaigns in your Spoke organization. You can access these settings from the administrator [dashboard](#dashboards).

## Opt-out message

You can set the default opt-out message that auto-fills the message field when texters use the opt-out feature.

## Texting hours

You can enforce [texting hours](#texting-hours) across all campaigns by turning on this feature. This prevents you from disturbing contacts outside of these hours. Each campaign has its own set of texting hours that you specify on the campaign settings page.

## Assemble Numbers API key

Assemble Numbers is a service that helps you determine whether you can reach a phone number in your contact list. For example, you can use Assemble Numbers to determine whether a phone number is a cell number or a landline.

If you provide your Spoke organization with an API key for Assemble Numbers, Spoke automatically checks all phone numbers in your contact list and filters out all unreachable numbers.

You can request an Assemble Numbers API key from [here](https://airtable.com/shruW0ZhyOSw3KzIw). 

## Sending locations

Sending locations let you message your contacts from localized numbers, giving the conversation a more personal feel. Each sending location is defined by a zip code and has several associated area codes for phone numbers. When a texter messages a contact, Spoke automatically uses the sending location closest to the contact to send the message.

For most, the one or two sending locations pre-configured when you sign up will be all you need. Sending locations can be added on the fly, however, if you are texting in many places or otherwise need more granular control over sending locations. Keep in mind that the more sending locations you have, the more numbers you need to purchase, and the higher the cost.

![Sending Locations](https://checkupon.me/docs/images/proximity.jpg)

**Managing Sending Locations**

If you need to create and manage a large number of sending locations, we can give you an API token that will allow you to create sending locations yourself.

To do this, you will need to make a GraphQL request to [https://numbers.assemble.live](https://numbers.assemble.live/), with a "token" header that is the API token we provide over email. If you are not familiar with GraphQL, check out [this getting started guide](https://graphql.org/learn/). You will also need to know your profile id, which we can provide over email as well. We recommend using [Postman](https://www.postman.com/), [Insomnia](https://insomnia.rest/), or [GraphiQL](https://www.electronjs.org/apps/graphiql) to make these API requests.

To get all currently active sending locations, use the following query:

```
query activeSendingLocations {
    sendingLocations(condition: { decomissionedAt: null }) {
        nodes {
            referenceName
            center
        }
    }
}
```

To get all sending locations, even ones that have been discarded, simply remove the condition:

```
query allSendingLocations {
    sendingLocations {
        nodes {
            referenceName
            center
        }
    }
}
```

You could also, for example, look at sending locations by state:

```
query getSendingLocationsForState($state: String!) {
    sendingLocations(condition: { decomissionedAt: null, state: $state }) {
        nodes {
            referenceName
            center
        }
    }
}
```

With the variables:

```
{
	"state": "NY"
}
```

To create a sending location, use the following mutation, providing the zip code to use as the center point for the sending location you would like to create. This will return additional information about the sending location including the area codes it will begin purchasing numbers from.

```
mutation createSendingLocation($center: ZipCode!, $referenceName: String!, $profileId: UUID!) {
    createSendingLocation(input: {sendingLocation: {center: $center, referenceName: $referenceName, profileId: $profileId, purchasingStrategy: SAME_STATE_BY_DISTANCE}}) {
        sendingLocation {
            referenceName
            center
            state
            location {
                x
                y
            }
            areaCodes
        }
    }
}
```

And include something like the following payload as variables:

```
{
	"profileId":"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx",
	"center": "11206",
	"referenceName": "My Special Sending Location"
}
```

## Send Status

"Send status" is a column on the messages export from Spoke. It refers to the status of an outbound message (inbound messages are always DELIVERED).

There are 3 possible values for send status: **SENT,** **DELIVERED,** and **ERROR**.

A send status of **ERROR** means that the message was not delivered to the recipients phone. The most common reason for this is that the recipients carrier rejected the message as part of their spam filters, and the most common thing that would cause the recipient's phone to have identified your message as spam is if it included links or URLs.

The other common cause of an ERROR send status is texting someone who has replied "STOP" or "UNSUBSCRIBE". Don't worry - you won't be charged for messages rejected for this reason (you are charged for messages rejected by carriers for other reasons), and it's still considered best practice to send an opt-out confirmation message according to the official CTIA (a big carrier industry group) guidelines.

A send status of **DELIVERED** means that Spoke received confirmation that the message was delivered to the recipient's phone. Almost all of the time, this means that the recipient's phone received the message. Some of the time, however, we have seen carriers send us affirmative delivery reports without having sent the message. This typically occurs after sending a large volume of a particular URL, and we believe they do it in order to prevent you and us from reverse engineering their spam filters.

**SENT** means that the message was just sent by the user and is in the process of being delivered. This is most often a temporary status, and you'll see more messages than usual marked as SENT if you export from a running campaign. Delivery reports typically arrive in a few seconds, but can also arrive minutes or hours later. A small percent of messages will stay SENT forever because we never received a delivery report from the carrier. Just like false positive delivery reports, this just happens sometimes and is likely done to prevent the reverse engineering of spam filters.

## User Roles

### Owner

### Administrator

### Texter

# Managing campaigns

## Create a new campaign

![Campaign](https://checkupon.me/docs/images/campaign.png)

Creating a [campaign](#campaigns) lets you reach out to your contacts in a systematic and scripted manner. Spoke administrators can create campaigns from the Spoke [administration dashboard](#dashboards).

> Note: After you create and start a campaign, you can continue editing the campaign information with the exception of the contact list.

To create a new campaign, use the following steps:

### Step 1: Start the campaign creation wizard

In the administrator dashboard, click the **New campaign** button.

### Step 2: Enter campaign information

The first panel in the campaign creation wizard includes fields for basic campaign information. Enter values for the following fields:

- **Title** (required) -- The title of the campaign. This will be visible to texters and will be used for email notifications and for naming export files. Campaign titles can be useful for the [bulk script editor](#bulk-script-editor), so you should consider grouping similar campaigns with the same text at the beginning of the title.
- **Description** (required) -- A description of the campaign. This can be used to include instructions or perhaps just some inspirational text for your texters.
- **Due Date** (required) -- The date on which the campaign ends. After this date, texters cannot send initial messages for this campaign, and future replies from contacts are stored in the database. This ensures, for example, that you never text out recruiting for an event after that event has passed.
- **Intro HTML** (optional) -- The HTML that is displayed to texters.
- **Logo Image URL** (optional) -- The URL for an image that is displayed to texters.
- **Primary Color** (optional) -- The color that is displayed to texters.

### Step 3: Import contacts to the campaign

From the "Contacts" window, perform the following steps:

1. (Optional) Filter out contacts that are also contacts in another campaign.
   1. Start typing the name of the campaign you want to use for filtering.
   2. Click the campaign name in the list.
   3. Repeat until you've finished adding the campaigns you want to use.
2. Click **Upload contacts**.
3. Browse for the contact-list CSV file, and click **Open**.
4. Review the upload notifications for processing notes.

For more information on the formatting requirements for your CSV file, see [Contact lists](#contact-lists).

> Note: Once you start the campaign, you will not be able to change the contact list.

### Step 4: Resolve any overlapping contacts with other campaigns

If you uploaded contacts that are also contacts for other active campaigns, those campaigns are listed in the "Campaign overlap management" window. Perform one of the following:

- Leave the campaign with overlapping in the list.
- Click the trash icon to remove the overlapping contacts from this campaign.

For more information, see [Contact overlap management](#contact-overlap-management).

### Step 5: (Optional) Assign teams to the campaign

Add teams to the campaign from the "Teams" window:

1. Enter a team name in the field, and click the team name in the list.
2. (Optional) Add additional teams by repeating the previous step.
3. (Optional) Restrict conversation assignment to members of the listed teams by clicking the switch.

### Step 6: Set the assignment options for texters

In the "Texter" window, set the options for assigning contacts to texters.

> Note: You can turn on auto-assignment in Step 10. Auto-assignment does not impact manual and dynamic assignment.

#### Manually assign contacts to texters

To manually assign a number of contacts to an individual texter:

1. Search for the name of the texter. The texter must already exist in Spoke.
2. Specify the number of contacts to assign to the texter.

#### Dynamically assign contacts to texters

To dynamically assign contacts to texters:

1. Select the dynamic assignment option to turn on dynamic assignment.
2. Copy the generated URL.
3. Share the URL with the texters you want to assign to this campaign.

#### Auto-assignment

Auto-assignment occurs when texters in your organization request assignment. You can enable auto-assignment in Step 10.

### Step 7: Create an interaction script for your texters

To create an interaction script, follow the instructions in [Create an interaction script](#create-an-interaction-script).

### Step 8: Create canned responses for off-script responses

To add a canned response:

1. Open the "Canned Responses" window.
2. Click **Add new canned response**.
3. Enter a title for the canned response.
4. Write a message for the response:
   1. Click the **Script version 1** field.
   2. Enter an initial message using the replaceable fields ({firstName}, {lastName}, etc.).
   3. Click **Done**.
5. Click **Add response**.
6. (Optional) Add additional canned responses.
7. Click **Save**.

For more information, see [Canned responses](#canned-responses).

### Step 9: Set texting hours to minimize disturbance

To set texting hours:

1. Open the "Texting Hours" window.
2. Enter a start time. Use a 12-hour time, such as **9 am**.
3. Enter an end time. Use a 12-hour time, such as **9 pm**.
4. Select a default timezone to apply to contacts without zip codes.
5. Click **Save**.

For more information, see [Texting hours](#texting-hours).

### Step 10: Set the auto-assignment option

Turning on auto-assignment allows the campaign to automatically assign texters to your organization. By default, auto-assignment is turned off.

To turn on auto-assignment:

1. Open the "Autoassign Mode" window.
2. Click the switch.
3. Click **Save**.

### Step 11: Start the campaign

Before you start the campaign, double-check the previous steps to ensure you have properly entered and saved the campaign details. When you are ready to start the campaign, click the **Start this campaign** button.

## Create an interaction script

You can create an [interaction script](#interaction-scripts) while editing the settings of a campaign.

1. Navigate to the campaign settings page by editing a campaign.

2. Open the "Interactions" window.

3. Write an initial message:

   1. Click the **Script version 1** field.
   2. Enter an initial message using the replaceable fields ({firstName}, {lastName}, etc.).
   3. Click **Done**.
   4. (Optional) Write additional versions of the initial message. Different versions are randomly selected by Spoke.
   5. Write a survey question to split the interaction script into multiple paths. This question is viewed only by texters.

4. Add a response by clicking **Add a response** and following these steps:

   1. Write an answer to the previous survey question. Texters select this answer to access this response. This answer is viewed only by texters.
   2. Write a response message.
   3. (Optional) Write additional versions of the response message. Different versions are randomly selected by Spoke.
   4. Write a survey question. This question is viewed only by texters.

5. Repeat step 4 -- adding responses to the initial message and to other responses -- until you have completed the full set of responses you want to include in the script.

   > Note: Make sure you are adding responses under the appropriate message.

6. Click **Save**.

## Colors and tags for active campaigns

The campaign list on the administration dashboard uses colors and tags to help you keep track of your active campaigns. The colors and tags are automatically applied to the campaigns based on their state.

## Color coding

Active campaigns in the campaign list are categorized by the color of their titles. They are color-coded as follows:

- **Orange** -- The campaign has not been started, or it has unassigned contacts.
- **Blue** -- The campaign has been started but not all initial messages have been sent.
- **Green** -- The campaign has been started and all initial messages have been sent.

## Tags

Active campaigns in the campaign list can have one or more of the following tags:

- **Unassigned Contacts** -- Some contacts have not been assigned to texters.
- **Unsent Initial Messages** -- Some contacts have not received an initial text.
- **Unhandled Replies** -- Some contacts have not received a reply from a texter.
- **Autoassign Eligible** -- The campaign has auto-assignment mode enabled.

## Reassign conversations to texters

There are several ways for you to reassign conversations to new texters or to unassign conversations to release them back to the assignment pool. The following sections describe the various methods of reassignment and unassignment.

## From the message review page

From the message review page, you can manually reassign (or unassign) conversations to different texters.

To reassign conversations from the message review page:

1. Go to the **Message Review** page from the administration dashboard.

2. Filter the message list from the **Message** **Filter** window. Using the filter gives you the option of reassigning all conversations that match the filter.

3. Find the conversations you want to reassign, and select them with the checkbox.

4. Open the **Message Actions** window.

5. Select **Reassign**.

   > Note: You can also select **Unassign** to release the conversations back into the assignment pool.

6. Specify one or more texters who will receive the reassignment.

7. Click **Reassign selected** to reassign all selected contacts or **Reassign all \*n\* matching** to reassign all contacts that match the filter.

![Review](https://checkupon.me/docs/images/messagereview.png)

## From the escalated conversations page

From the escalated conversations page, you can manually reassign (or unassign) escalated conversations to texters who can handle the conversation.

To reassign an escalated conversation:

1. Go to the **Escalated Convos** page from the administration dashboard.

2. Select conversations for reassignment with either or both of the following methods:

   1. Filter the message list from the **Message** **Filter** window. Using the filter gives you the option of reassigning all escalated conversations that match the filter.
   2. Manually find the conversations you want to reassign, and select them with the checkbox.

3. Open the **Message Actions** window.

4. Select **Reassign**.

   > Note: You can also select **Unassign** to release the conversations back into the assignment pool.

5. Specify one or more texters who will receive the reassignment.

6. Click **Reassign selected** to reassign all selected contacts or **Reassign all \*n\* matching** to reassign all contacts that match the filter.

## From the campaign list

From the campaign list, you can perform two campaign actions to release conversations.

#### Release unsent messages

The release unsent messages campaign action releases all conversations where the texter has not sent an initial message.

To release unsent messages for a campaign:

1. Go to the **Campaigns** page from the administration dashboard.
2. Open the actions menu of the campaign.
3. Click **Release Unsent Messages**.

#### Release unreplied conversations

The release unreplied conversations campaign action releases all conversations where the texter has not sent a response to a contact.

To release unreplied conversations for a campaign:

1. Go to the **Campaigns** page from the administration dashboard.
2. Open the actions menu of the campaign.
3. Click **Release Unreplied Conversations**.

## Export data from a campaign

Exporting data from a campaign gives you access to your updated contact list and to the messages in your campaign. The exported messages file contains information about which messages were successfully delivered.

To export data from a campaign:

1. Open a campaign from the campaign list.

   > Note: If the campaign has not started, the campaign settings page opens. To open the campaign page, remove "edit" from the URL.

2. Click **Export data**. This starts the export process.

3. Open your email, and wait for a message from Spoke Rewired. Exporting campaign data can take a long time, depending on the amount of data. Check your spam folder if you haven't received an email in a reasonable amount of time.

4. Click the first link to download the campaign data.

5. Click the second link to download the message data.

## Campaign actions

You can manage active campaigns with campaign actions. The following actions are available for each campaign in the campaign list.

#### Release Unsent Messages

Unassigns all conversations waiting for an initial message from a texter.

Sometimes, texters request a number of conversations but won't handle all of them. If that happens, you can release those conversations so that they can be assigned to other texters.

#### Mark For Second Pass

Marks all conversations that didn't receive a response from the contact as needing an initial message.

> Note: You can use this action only before the due date of a campaign.

This action is useful for following up with contacts who didn't see the initial message or who forgot to reply. If you use this action, you should also change the script's initial message so that texters don't send the exact same message twice. For example, you could start the new initial message with, "Hey, not sure if you saw my first text..."

When you use this action, a notification displays the number of conversations that are marked for a second pass.

#### Release Unreplied Conversations

Unassigns conversations waiting for a response from a texter.

When you use this action, you must specify a number of hours since the contact's last message. Any conversations that haven't been idle for that long are not unassigned.

Similar to Release Unsent Messages, this action is useful to make sure your contacts are receiving prompt responses from your texters.

#### Archive Campaign

Stops the campaign, marks it as archived, and disables all future texting and notifications for the campaign.

# Spoke Contact Tool Guide

![Mobile App](https://checkupon.me/docs/images/mobile.png)

# Text a contact

After you have [requested and received conversation assignments](#request-texts-for-assignment), you can begin texting contacts.

## Send initial messages

To send an initial message:

1. Open the [texter dashboard](#dashboards).

2. Click **Send first texts**.

3. Click **Send**.

   > Note: You cannot edit the initial message.

Following this procedure takes the conversation out of your to-do list. When the contact responds, the conversation will reappear under the **Send replies** category.

## Send replies

To send replies to contacts who have responded to an initial message:

1. Open the [texter dashboard](#dashboards).
2. Click **Send replies**.
3. Answer the survey question. This fills the message field with a prepared response.
4. (Optional) Edit the message as needed. We recommend using the response that your Spoke administrators have carefully crafted for you.
5. Click **Send**.

Following this procedure takes the conversation out of your to-do list. When the contact responds, the conversation will re-enter your to-do list.

This is the standard procedure for sending a reply. In certain cases, you might need to do one of the following when crafting a reply:

- [Skip the reply](#skip-a-reply)
- [Use a canned response](#use-a-canned-response)
- [Opt out the contact](#opt-out-a-contact)
- [Add a tag to the conversation](#add-tags-to-a-conversation)
- [Escalate the conversation](#escalate-a-conversation)

## Request texts for assignment

If you are a [texter](#user-roles) for your organization, you can request text assignments to start conversations with contacts.

To request texts:

1. Open the texter [dashboard](#dashboards).
2. In the **Count** field, specify the number of conversations you want assigned to you. If there are no unassigned conversations, a message will be displayed.
3. Click **Request More Texts**.

## Add tags to a conversation

Adding tags to a conversation allows your Spoke administrators to keep informed about your contacts. You can use tags to indicate your contact's primary language, or you can use tags to [escalate a conversation](#escalate-a-conversation). For information on how you should be using tags, contact your Spoke administrators.

To add a tag to a conversation:

1. From an open conversation, click **Manage tags**.
2. Choose one or more tags from the list. You cannot create your own tag. 
3. Click **Save**.

![Tags](https://checkupon.me/docs/images/tags.png)

## Opt out a contact

Opting out a contact adds them to your organization's opt-out list. This prevents you from sending more messages to the contact. All future campaigns automatically remove contacts who are on the opt-out list.

### Opt out with a message

Opting out a contact with a message allows you to apologize for the inconvenience.

To opt-out a contact with a followup message:

1. While in a conversation, click **Opt-out**.
2. Either enter your own followup message, or use the one automatically provided.
3. Click **Send**.

### Opt out without a message

Opting out a contact without a message prevents you from disturbing them further.

To opt-out a contact without a followup message:

1. While in a conversation, click **Opt-out**.
2. Delete the message that's automatically provided.
3. Click **Opt out without text**.

## Use a canned response

Canned responses are messages prepared for you by your Spoke administrators. You can use these in case a conversation goes off script.

To use a canned response:

1. From a conversation, click **Canned responses**.
2. Click the canned response you want to use.
3. (Optional) Edit the response as needed.
4. Click **Send**.

## Skip a reply

Skipping a reply allows you to move onto the next conversation without sending a reply to a contact. You can return to conversations that you skipped using the **Skipped messages** button on the texter dashboard.

To skip a reply:

1. From a conversation, click **Skip reply**, as shown in the following figure:

![Skip Reply](http://checkupon.me/docs/images/skipreply.jpg)

## Escalate a conversation

Escalating a conversation brings it to the attention of your Spoke administrators, allowing them to take appropriate action. In general, use the escalate tag when you need someone to help you out with a conversation, but ask your Spoke administrators about when they think it's appropriate.

To escalate a conversation:

1. From an active conversation, click **Manage tags**.
2. Click **Escalate conversation**.
3. Click **Save**.

## Include an image in a message

You can include images with your messages to send event posters or other media to your contacts. 

> Note: Multimedia messages cost more to send than text-only messages. Ask your organization for guidelines and permission.

To include images with your messages:

1. From a conversation, paste a URL between two square brackets, [ ]. For example: `[https://image-url.com/image-is-here]`.
2. Write a message to be sent with the image. Any text before and after the bracketed URL is combined into a single message with the bracketed URL removed.
3. Click **Send**.

### Size limitations

Cellular carriers have different limitations on MMS attachments. We recommend keeping attachment size below **600 KB** for best results.

Size limitations for the top 4 US carriers are:

| **Carrier** | **MMS attachment size** |
| ----------- | ----------------------- |
| AT&T        | 1.4 MB                  |
| Sprint      | 1.4 MB                  |
| T-mobile    | 0.675 MB                |
| Verizon     | 0.675 MB                |

### Send an image with links

The SMS/MMS protocol, regardless of provider, does not support hyperlinked images. If you want to provide a link with an accompanying image, you can add [meta tags for social media](https://css-tricks.com/essential-meta-tags-social-media/) to the linked website itself, and then send the link. These tags let messaging applications show a preview of the linked content. For example, this is how YouTube link previews are displayed.

If you don't have control of the linked website, you can create an intermediate page that redirects to the destination page [using a refresh tag](https://www.lifewire.com/meta-refresh-tag-3469046). Then, you can add meta tags to the intermediate page.

# Appendix

## Timezone Reference

The following is the full list of useable time zones:

```
'Europe/Andorra',
'Asia/Dubai',
'Asia/Kabul',
'Europe/Tirane',
'Asia/Yerevan',
'Antarctica/Casey',
'Antarctica/Davis',
'Antarctica/DumontDUrville', 
'Antarctica/Mawson',
'Antarctica/Palmer',
'Antarctica/Rothera',
'Antarctica/Syowa',
'Antarctica/Troll',
'Antarctica/Vostok',
'America/Argentina/Buenos_Aires',
'America/Argentina/Cordoba',
'America/Argentina/Salta',
'America/Argentina/Jujuy',
'America/Argentina/Tucuman',
'America/Argentina/Catamarca',
'America/Argentina/La_Rioja',
'America/Argentina/San_Juan',
'America/Argentina/Mendoza',
'America/Argentina/San_Luis',
'America/Argentina/Rio_Gallegos',
'America/Argentina/Ushuaia',
'Pacific/Pago_Pago',
'Europe/Vienna',
'Australia/Lord_Howe',
'Antarctica/Macquarie',
'Australia/Hobart',
'Australia/Currie',
'Australia/Melbourne',
'Australia/Sydney',
'Australia/Broken_Hill',
'Australia/Brisbane',
'Australia/Lindeman',
'Australia/Adelaide',
'Australia/Darwin',
'Australia/Perth',
'Australia/Eucla',
'Asia/Baku',
'America/Barbados',
'Asia/Dhaka',
'Europe/Brussels',
'Europe/Sofia',
'Atlantic/Bermuda',
'Asia/Brunei',
'America/La_Paz',
'America/Noronha',
'America/Belem',
'America/Fortaleza',
'America/Recife',
'America/Araguaina',
'America/Maceio',
'America/Bahia',
'America/Sao_Paulo',
'America/Campo_Grande',
'America/Cuiaba',
'America/Santarem',
'America/Porto_Velho',
'America/Boa_Vista',
'America/Manaus',
'America/Eirunepe',
'America/Rio_Branco',
'America/Nassau',
'Asia/Thimphu',
'Europe/Minsk',
'America/Belize',
'America/St_Johns',
'America/Halifax',
'America/Glace_Bay',
'America/Moncton',
'America/Goose_Bay',
'America/Blanc-Sablon',
'America/Toronto',
'America/Nipigon',
'America/Thunder_Bay',
'America/Iqaluit',
'America/Pangnirtung',
'America/Atikokan',
'America/Winnipeg',
'America/Rainy_River',
'America/Resolute',
'America/Rankin_Inlet',
'America/Regina',
'America/Swift_Current',
'America/Edmonton',
'America/Cambridge_Bay',
'America/Yellowknife',
'America/Inuvik',
'America/Creston',
'America/Dawson_Creek',
'America/Fort_Nelson',
'America/Vancouver',
'America/Whitehorse',
'America/Dawson',
'Indian/Cocos',
'Europe/Zurich',
'Africa/Abidjan',
'Pacific/Rarotonga',
'America/Santiago',
'America/Punta_Arenas',
'Pacific/Easter',
'Asia/Shanghai',
'Asia/Urumqi',
'America/Bogota',
'America/Costa_Rica',
'America/Havana',
'Atlantic/Cape_Verde',
'America/Curacao',
'Indian/Christmas',
'Asia/Nicosia',
'Asia/Famagusta',
'Europe/Prague',
'Europe/Berlin',
'Europe/Copenhagen',
'America/Santo_Domingo',
'Africa/Algiers',
'America/Guayaquil',
'Pacific/Galapagos',
'Europe/Tallinn',
'Africa/Cairo',
'Africa/El_Aaiun',
'Europe/Madrid',
'Africa/Ceuta',
'Atlantic/Canary',
'Europe/Helsinki',
'Pacific/Fiji',
'Atlantic/Stanley',
'Pacific/Chuuk',
'Pacific/Pohnpei',
'Pacific/Kosrae',
'Atlantic/Faroe',
'Europe/Paris',
'Europe/London',
'Asia/Tbilisi',
'America/Cayenne',
'Africa/Accra',
'Europe/Gibraltar',
'America/Godthab',
'America/Danmarkshavn',
'America/Scoresbysund',
'America/Thule',
'Europe/Athens',
'Atlantic/South_Georgia',
'America/Guatemala',
'Pacific/Guam',
'Africa/Bissau',
'America/Guyana',
'Asia/Hong_Kong',
'America/Tegucigalpa',
'America/Port-au-Prince',
'Europe/Budapest',
'Asia/Jakarta',
'Asia/Pontianak',
'Asia/Makassar',
'Asia/Jayapura',
'Europe/Dublin',
'Asia/Jerusalem',
'Asia/Kolkata',
'Indian/Chagos',
'Asia/Baghdad',
'Asia/Tehran',
'Atlantic/Reykjavik',
'Europe/Rome',
'America/Jamaica',
'Asia/Amman',
'Asia/Tokyo',
'Africa/Nairobi',
'Asia/Bishkek',
'Pacific/Tarawa',
'Pacific/Enderbury',
'Pacific/Kiritimati',
'Asia/Pyongyang',
'Asia/Seoul',
'Asia/Almaty',
'Asia/Qyzylorda',
'Asia/Qostanay', 
'Asia/Aqtobe',
'Asia/Aqtau',
'Asia/Atyrau',
'Asia/Oral',
'Asia/Beirut',
'Asia/Colombo',
'Africa/Monrovia',
'Europe/Vilnius',
'Europe/Luxembourg',
'Europe/Riga',
'Africa/Tripoli',
'Africa/Casablanca',
'Europe/Monaco',
'Europe/Chisinau',
'Pacific/Majuro',
'Pacific/Kwajalein',
'Asia/Yangon',
'Asia/Ulaanbaatar',
'Asia/Hovd',
'Asia/Choibalsan',
'Asia/Macau',
'America/Martinique',
'Europe/Malta',
'Indian/Mauritius',
'Indian/Maldives',
'America/Mexico_City',
'America/Cancun',
'America/Merida',
'America/Monterrey',
'America/Matamoros',
'America/Mazatlan',
'America/Chihuahua',
'America/Ojinaga',
'America/Hermosillo',
'America/Tijuana',
'America/Bahia_Banderas',
'Asia/Kuala_Lumpur',
'Asia/Kuching',
'Africa/Maputo',
'Africa/Windhoek',
'Pacific/Noumea',
'Pacific/Norfolk',
'Africa/Lagos',
'America/Managua',
'Europe/Amsterdam',
'Europe/Oslo',
'Asia/Kathmandu',
'Pacific/Nauru',
'Pacific/Niue',
'Pacific/Auckland',
'Pacific/Chatham',
'America/Panama',
'America/Lima',
'Pacific/Tahiti',
'Pacific/Marquesas',
'Pacific/Gambier',
'Pacific/Port_Moresby',
'Pacific/Bougainville',
'Asia/Manila',
'Asia/Karachi',
'Europe/Warsaw',
'America/Miquelon',
'Pacific/Pitcairn',
'America/Puerto_Rico',
'Asia/Gaza',
'Asia/Hebron',
'Europe/Lisbon',
'Atlantic/Madeira',
'Atlantic/Azores',
'Pacific/Palau',
'America/Asuncion',
'Asia/Qatar',
'Indian/Reunion',
'Europe/Bucharest',
'Europe/Belgrade',
'Europe/Kaliningrad',
'Europe/Moscow',
'Europe/Simferopol',
'Europe/Kirov',
'Europe/Astrakhan',
'Europe/Volgograd',
'Europe/Saratov',
'Europe/Ulyanovsk',
'Europe/Samara',
'Asia/Yekaterinburg',
'Asia/Omsk',
'Asia/Novosibirsk',
'Asia/Barnaul',
'Asia/Tomsk',
'Asia/Novokuznetsk',
'Asia/Krasnoyarsk',
'Asia/Irkutsk',
'Asia/Chita',
'Asia/Yakutsk',
'Asia/Khandyga',
'Asia/Vladivostok',
'Asia/Ust-Nera',
'Asia/Magadan',
'Asia/Sakhalin',
'Asia/Srednekolymsk',
'Asia/Kamchatka',
'Asia/Anadyr',
'Asia/Riyadh',
'Pacific/Guadalcanal',
'Indian/Mahe',
'Africa/Khartoum',
'Europe/Stockholm',
'Asia/Singapore',
'America/Paramaribo',
'Africa/Juba',
'Africa/Sao_Tome',
'America/El_Salvador',
'Asia/Damascus',
'America/Grand_Turk',
'Africa/Ndjamena',
'Indian/Kerguelen',
'Asia/Bangkok',
'Asia/Dushanbe',
'Pacific/Fakaofo',
'Asia/Dili',
'Asia/Ashgabat',
'Africa/Tunis',
'Pacific/Tongatapu',
'Europe/Istanbul',
'America/Port_of_Spain',
'Pacific/Funafuti',
'Asia/Taipei',
'Europe/Kiev',
'Europe/Uzhgorod',
'Europe/Zaporozhye',
'Pacific/Wake',
'America/New_York',
'America/Detroit',
'America/Kentucky/Louisville',
'America/Kentucky/Monticello',
'America/Indiana/Indianapolis',
'America/Indiana/Vincennes',
'America/Indiana/Winamac',
'America/Indiana/Marengo',
'America/Indiana/Petersburg',
'America/Indiana/Vevay',
'America/Chicago',
'America/Indiana/Tell_City',
'America/Indiana/Knox',
'America/Menominee',
'America/North_Dakota/Center',
'America/North_Dakota/New_Salem',
'America/North_Dakota/Beulah',
'America/Denver',
'America/Boise',
'America/Phoenix',
'America/Los_Angeles',
'America/Anchorage',
'America/Juneau',
'America/Sitka',
'America/Metlakatla',
'America/Yakutat',
'America/Nome',
'America/Adak',
'Pacific/Honolulu',
'America/Montevideo',
'Asia/Samarkand',
'Asia/Tashkent',
'America/Caracas',
'Asia/Ho_Chi_Minh',
'Pacific/Efate',
'Pacific/Wallis',
'Pacific/Apia',
'Africa/Johannesburg'
```