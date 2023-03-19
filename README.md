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

To create an issue, use the `create_issue` command along with the `--prompt` parameter, e.g.

    python3 jiranl.py create_issue --prompt "Create an issue named 'Login button is broken'"

