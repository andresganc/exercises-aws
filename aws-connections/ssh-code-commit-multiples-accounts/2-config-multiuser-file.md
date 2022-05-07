
# This file is:  ~/.ssh/config

# You may have other (non-CodeCommit) SSH credentials stored in this
# config file – in addition to the CodeCommit settings shown below.

# NOTE: Make sure to run [ chmod 600 ~/.ssh/config ] after creating this file!

# Credentials for Account1

Host awscc-account1                                 # 'awscc-account1' is a name you pick
  Hostname git-codecommit.us-east-1.amazonaws.com   # This points to CodeCommit in the 'US East' region
  User A1EXAMPLE01234567891                         # UserID as provided by IAM Security Credentials (SSH)
  IdentityFile ~/.ssh/account1-awsCC-rsa            # Path to corresponding key file

# Credentials for Account2
Host awscc-account2
  Hostname git-codecommit.us-east-1.amazonaws.com
  User A2EXAMPLE01234567892
  IdentityFile ~/.ssh/account2-awsCC-rsa

# Credentials for Account3
Host awscc-account3
  Hostname git-codecommit.us-east-1.amazonaws.com
  User A3EXAMPLE01234567893
  IdentityFile ~/.ssh/account3-awsCC-rsa



## CLONING A REPO
When newly cloning a repo, make the following change to your clone command:

_	_
Command	git clone ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos/my-repo
Becomes	git clone ssh://awscc-account1/v1/repos/my-repo
