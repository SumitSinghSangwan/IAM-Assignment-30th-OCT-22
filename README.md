# Assignment Interview question

# 1. What is the need of IAM?

 Ans-->  it is a global service. (IAM) ensures that the right people and job roles in your organization (identities) can access the tools they need to do their jobs. Identity management and access systems enable your organization to manage employee apps without logging into each app as an administrator


# 2. If i am a non tech person, how will you define policies in
IAM?

 Ans--> giving premission to the person to do his task define for his role.


3. Please define a scenerio in which you would like to create
your on own IAM policy.

 Ans-->  we want a user, group or role in which he can only read and no other premission given.


# 4. Why do we prefer not using root account?

 Ans-->   If the credentials for the root account are stolen they will be able to access or change anything in the account giving them the ability to misuse any data or resources in the account


# 5. How to revoke policy for an IAM user?

 Ans-->  To revoke a policy for an IAM user in AWS, you can follow these steps:

Sign in to the AWS Management Console with your AWS account credentials.
Open the IAM console by navigating to the IAM service.
In the left navigation pane, click on "Users" to view a list of IAM users.
Locate the IAM user for whom you want to revoke the policy and click on their username.
In the "Permissions" tab, you will see a list of policies attached to the user.
Identify the policy you want to revoke and click on the "X" icon next to it.
A confirmation dialog will appear asking if you want to detach the policy. Click on "Detach" to confirm.
The policy will be immediately revoked, and the user will no longer have the permissions granted by that policy.
It's important to note that when you revoke a policy from an IAM user, it removes the permissions associated with that policy. Ensure that you review the policy and its effects on the user's access before detaching it.

Additionally, if the user has multiple policies attached, revoking one policy will not affect the others. You can detach multiple policies by repeating steps 6 and 7 for each policy you want to revoke.

Remember to regularly review and manage the permissions of IAM users to maintain the principle of least privilege and ensure the security of your AWS resources.

# 6. Can a single IAM user be a part of multiple policy via group
and root? how?

Ans-->Yes, a single IAM user can be associated with multiple policies through the use of IAM groups and the root account. Here's how it works:

IAM Groups: You can create IAM groups and attach policies to them. IAM groups allow you to logically group users and manage their permissions collectively.

Create an IAM group: Go to the IAM console, click on "Groups" in the left navigation pane, and then click on "Create New Group". Give the group a name and proceed.
Attach policies to the group: Select the created group, click on "Permissions" tab, and then click on "Attach Policies". Choose the desired policies from the list and attach them to the group.
Users that are members of the group will inherit the policies attached to the group. So, by adding the IAM user to multiple groups, you can associate them with multiple policies simultaneously.

Root Account: The AWS account root user has full administrative access to all AWS services and resources. While it's recommended to avoid using the root account for day-to-day operations, you can attach policies directly to the root account if necessary.

Attach policies to the root account: In the IAM console, click on "Access management" in the top navigation bar, and then click on "Root user". Select the "Permissions" tab and click on "Add Permissions" to attach policies directly to the root account.
Policies attached to the root account will apply to all IAM users within the account, including the root user.

By utilizing IAM groups and the root account, you can assign multiple policies to a single IAM user by adding them to multiple groups and attaching policies to the root account. This allows for more efficient management of permissions and simplifies the process of granting and revoking access for users in AWS.
