# JIRA-NL

![jirnal](https://user-images.githubusercontent.com/45729602/226185282-1d9f5e04-cb28-4cce-b555-15df49846791.gif)

JIRA-NL is a little python script that uses ChatGPT to add natural language capabilities to JIRA,
specifically in the context of creating JIRA issues.

## Dependencies

The script uses the `requests`, `openai` and `termcolor` python packages, make sure to install them
using the following commands before running the script

    pip install requests
    pip install openai
    pip install termcolor

## Setup

To work properly, start by configuring your JIRA email address, API token and workspace name, as well as the OpenAI API token
in the `jiranl_consts.py` file, after configuration it should looks something like this

    JIRA_API_KEY = 'xxxxxxxxx'
    OPENAI_API_KEY = 'xxxxxxxxx'
    EMAIL = 'john@doe.com'
    JIRA_WORKSPACE = 'johndoe' (i.e. the first part of the atlassian domain, e.g. https://johndoe.atlassian.net)

## Usage

### Create An Issue

To create an issue, simply call the script with a string description of your issue,
you can assign the issue to users using their account ID

    python3 jiranl.py "Create an issue named 'Login button is broken' assign it to 5c0bb5b48bb9b546bbb4b827"

### Get User/Project IDs

Passing `users` or `projects` will print project/users along with their identifiers

    $ python3 jiranl.py users

    1) Mike Mclean (5b0bb5b48bbb9b546efc4b827)
    2) Freddy Jacobson (5b0bb5b48bbb9b546efc4b827)
    3) Kara Mcbride (5b0bb5b48bbb9b546efc4b827)

**Pro Tip:** you can use a Raycast script command to run script using Raycast
