<!--
title: 04 - Package Access
featured: true
-->

# Managing Package Access

After setting up teams, the next step is to associate 
those teams with specific scopes. 

## Scope your package to your Organization  

Publish a package and adjust package access via CLI
* In package directory, run
```
npm init --scope=<org>
```
to scope it for your org & publish as usual
* Team admins can now set package access.

## Managing Team Package Access

* Grant access:  
```
npm access grant <read-only|read-write> <org:team> [<package>]
```
* Revoke access:
```
npm access revoke <org:team> [<package>]
```

## Monitor Package Access

* See what org packages a team member can access:
```
npm access ls-packages <org> <user>
```
* See packages available to a specific team:
```
npm access ls-packages <org:team>
```
* Check which teams are collaborating on a package:
```
npm access ls-collaborators <pkg>
```
