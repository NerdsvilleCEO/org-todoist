org-todoist
===========

Sync TODOs between a emacs org-mode file and Todoist.

Todoist limits some API features to premium users, so it is recommended
to have a premium account.

How it works
------------

\`org-todoist\` syncs your org-mode file and Todoist tasks by following
steps.

1.  Pull all Todoist tasks
2.  Parse the org-mode file
3.  Update Todoist tasks by org-mode tasks
    -   Find a org-mode task by ID (in the PROPERTIES section)
    -   Update the Todoist task by the org-mode task
4.  Push changed tasks to Todoist
5.  Export org-mode file

Install
-------

``` {.example}
bundle install
```

Configuration
-------------

1.  Find your API token from [your account
    page](https://todoist.com/Users/viewPrefs?page=account)
2.  Write a configration file
    -   \`cp sample.env .env\`
    -   Update with your API token in \`.env\` file

Backup
------

**Please backup your org-mode files and Todoist project before sync**

[Todoist
backup](https://blog.todoist.com/2012/11/30/accidentally-delete-a-project-retrieve-it-from-a-backup/)

Run
---

``` {.example}
ruby ./sync.rb sample.org updated_sample.org
```
