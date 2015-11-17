<!--
title: 03 - Teams
featured: true
-->

# Teams

The key to managing access to packages via Organizations
is Teams.

## What are Teams?

Teams are sets of users that have access to a certain scope
within the Organization.

In order to create teams and manage team membership, you must be
a team admin under the given organization. Listing teams and team
memberships may be done by any member of the organizations.

Organization creation and management of team admins and organization
members is done through the [website](???), not the npm CLI.

For detailed information on the `team` command, check out the CLI
documentation [here](cli/team).

## The `developers` Team

When you first create an Organization, a team called `developers`
is created. This team contains all the people you have added to
your Organization.

To check who you have added to your organization you can type:

```
> npm team ls <org>:developers
```
...where `<org>` is the name of your Organization, e.g. `@npminc`.

## Creating Teams

To create a team, you can type:

```
> npm team create <org:team>
```
...where <org:team> is the name of your Organization, followed by
the name you'd like to give the new team. For example:

```
> npm team create @npminc:wombats
```

You can check that you created the team successfully by listing the
teams in your Organization. You can do that by typing:

```
> npm team ls <org>
```

You should see the new team you created.

## Adding Users to a Team

Once you've created a team you'll want to add users to it. To do
so you can type:

```
> npm team add <org:team> <user>
```
...where <org:team> is the name of your Organization, followed by
the name you'd like to give the new team and <user> is the npm
username of the user you'd like to add to the team. For example:

```
> npm team add @npminc:wombats ag_dubs
```

To check if you've added a user successfully, you can list all the
users on a particular team. To do so, type:

```
> npm team ls <org:team>
```

You see the user you just added to the team.

## Removing a User from a Team

```
> npm team rm <org:team> <user>
```
