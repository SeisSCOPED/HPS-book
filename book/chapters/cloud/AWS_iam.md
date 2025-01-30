# AWS Role Management

## Federated/IAM User

An IAM user is an user created in IAM (within the AWS account), whose permission could be managed by the policies. A federated user is an user Marine creates from Cloud Bank, which could be used to manage the AWS account.

## Pass Role to EC2

An IAM role is an IAM identity that you can create in your account that has specific permissions. An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it. Also, a role does not have standard long-term credentials such as a password or access keys associated with it. Instead, when you assume a role, it provides you with temporary security credentials for your role session.

When passing a role to resources, the policies attached to the role are automatically granted to the resources. The resources, for example an EC2 instance, will have access through the role, and access a S3 bucket (usually, a credential file is required on the instance).

When launching an EC2 instance, there is an option to pass a role to the instance. If IAMFullAccess is granted to the user, no addition action is required. However, if IAMReadOnlyAccess is granted, administrators are generally required to grant two policies to the user:

iam:GetRole
iam:PassRole

## Creating accounts en-masse

We recommend making temporary roles for workshop participants or research groups. The script below permits the automated creation of roles under a ``user group``. The policies are attached to teh user group and will be automatically granted to each new new user.

We recommend collecting all email addresses of group as rows in a CSV file with the column header ``Email``. The script below can be ran from a user account with admin privileges in python. All participants will be granted a temporary password, which they will be asked to update at first log in. In the example below, the usergroup is ``SCOPED_workshop_2024`` and for this example was granted EC2 full access. The temporary password is ``scoped2024@uw``.

```python
# read user list
df = pd.read_csv('userlist.csv')
df['Username'] = df.apply(lambda row: row['Email'].split("@")[0], axis = 1)
password = "scoped2024@uw"
usergroup = "SCOPED_workshop_2024"

for id, i in df.iterrows():
    username = i['Username']
    
    # create user
    rec = os.system(f"aws iam create-user --user-name {username}")

    if rec != 0:
        print(f"Error: {username}")
        continue
    
    # assign default password and request first-login reset
    os.system(f'aws iam create-login-profile --user-name {username} --password "{password}" --password-reset-required')
    
    # add user to a usergroup
    os.system(f"aws iam add-user-to-group --group-name {usergroup} --user-name {username}")
    print(f"=====================")
```

