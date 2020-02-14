# Purpose:
This tools assisting in migrating permissions from one group to another in the event that your are changing group names in your upstream User Directory. For example, if you are using the group "jira-developers" and you would like to mirror the permissions for this group to a new group across your environment (on all projects and repositories) to a new group called "bitbucket-users", then this is the tool for you.

# Dependencies:
* [Python3](https://www.python.org/downloads/) This was written in python3.7 and requires at least 3.2+ to operate as expected.
* [Requests](http://docs.python-requests.org/en/master/)

        pip3 install requests requests_oauthlib --user

# Usage:
Update the 5 values at the top of the script and then run with "python3 change_group_in_all_repos_and_projects.py"

        from_group_name = ""    # Example: "old_group"
        to_group_name = ""  # Example: "new_group"
        bitbucket_url = ""  # Example: "https://bitbucket.example.com"
        admin_username = "" # Example: "admin"
        admin_password = "" # Example: "password"

Once done, you can run the script via:

        python3 change_group_in_all_repos_and_projects.py

