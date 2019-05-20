Spirent Technical Deep Dive 5/16

Rep: Mary Wheeler
SE: Ravi Ghadia

Followups:
Nathan: Global rebranching/permissions on enterprise level.
Outside collaborators good way to work with contractors
Julian: Does Activity Dashboard roll on an enterprise scale or only for org?
Julian: multiple invoices per org?
Chris: Git LFS with Enterprise, any changes/impacts?
Setting up trial/sandbox with IT or one of the attendees
Consolidate accounts
Lost visibility on build account in the past, how to recover?
Recap from Satellite
What would downgrading from Enterprise look like?
SEND SWAG <3 (esp for David) ​
Attendees:
John Civitano - CRM manager and how tools will integrate
Julian Chocholak - devops in San Jose (user and repo administration -> team’s customers -> Nathan Neulinger devOps abd Chris Mckluskey
Scott runs engineering for SX
Yiqin manages Engine Team
Stephen? ​ ​ ##Discussion:
​
Julian:
Shared IT org but not thinking about how someone from another team engages. ​ Don’t want IT to be the only one who manages permissions -> slow down changes being made .
​ Enterprise can structure things -> what are use cases that can be handled?
- Who can add an user - someone in business has all permissions in a repo, can they add a user and give grant access on certain repos - removing access, removing user ​

Each person can manage their own org and map duplicates?
Ravi: On enterprise account, there is the owner and then billing manager
People won’t see the org if they are not visible to it?
Ravi: Yes, but even if they are not in the org, they belong in the whole enterprise account
Is it correct, before I’m a member of an org I need to be a member of the enterprise?
Mary: You add organization to the account. Whichever is parent level org, you will search org and add it to the larger account. Doesn’t mean that those people have access to those other orgs, just under a umbrella.
Theres different people that need to move to those organizations, will they be automatically upgraded to enterprise view?
Mary: top level view of enterprise is the admin only
What does that mean for a user in more than 1 org? (Mary: you can audit for unique users)
Does their idp integration affect the audit outside of toggling it on? Active Directory in a per org way?
Ravi: User would be invited to org and granted resources in the same way
Nathan: in an enterprise or org level?
Mary: Whats your ideal state?
Nathan: Currently a mess of user IDs back to corporate IDs (40-50%)
Initially when you roll up into enterprise, enforcing saml/sso delegated to org level. On enterprise, you enable authentication for org - while each org opts when to do Saml sso
AD, challenge response/email confirmed from GH to corporate ID
Mary: On enterprise cloud, if you want to associate corp email to GH
Skim for automated provisioning and deprovisioning - expose API but isn’t necessarily automated? Would need provider to script it or do it internally?
Ravi: If your IDP doesn’t have that built in
LDAP usage?
GH Cloud does not, available in Enterprise Server
Nathan: IT doesn’t prefer LDAP
Onelogin most likely
Orgs enforced by Enterprise
only for private repos
If people using Enterprise, use onelogin and GH, how quickly does that workflow happen?
Ravi: Supported, configuring documentation available, well known path
Mary: followup with a sandbox org

Julian: How to break down bill to specific orgs?
Mary: goal would be to consolidate into one invoice
Could finance split it? Would it be internally?
Mary will check back with GH finance team
Recommendations for migration?
Nothing changes from adding org to parent but nothing changes until SSO is enforced
Which build accounts are relevant to repos? ​ ​ ​ ​
Nathan:
Does org level come into play with an authentications via SAML ​ No one at enterprise level but admins, yes. ​ GH Enterprise proxy product for workflow? - Ravi: would need to build to automate, if you’re on-premise application then theres a jira replication

Mary: GHUnified gets brought up here ​ ​
Mary:
Current State: ​

Individuals use GH for their team or a specific project
Start using across a department
Expand to multiple departments ​ Challenges when starting organically Administration:
Maintaining consistent settings
Reporting across teams ​ Security:
Granting and revoking access
Chris: on a enterprise level would like to be able to limit public repo creation(but understands why its a org level)
Ravi: policies can be set that there is prescriptive overarching default policies before pushed down to org. ​ Developer Productivity:
Measuring and leveling up teams ​ GH Cloud
Simplify and lock done users and code securely
Enterprise accounts (unify admin)
Inconveniences around unifying orgs to identify unique users Activity Dashboard:
Visualize how your team works, understand org activity, security vulnerabilities, active members and workflow
Julian: Rolls up into org or overall enterprise?

Julian: Whats the reason for enterprise visibility?
Ravi: If you elected one or more of your org admin, you can promote them to have enterprise but not necessary.
Julian: Someone in IT could be enterprise while also part of their own org
Ravi: Possibly Give access to finance as billing manager at enterprise level GHU
Unified search from both
