# WordPress OAuth Server

This project is an OAuth 2.0 compatible authentication method for WordPress.

The goal of WP OAuth Server (WordPress Open Authentication) is to provide an easy to use authentication method that 3rd party services can use to securely connect to any server running WordPress site.

### Framework

This project is built on top of [Brent Shaffer's](https://github.com/bshaffer) PHP OAuth Server project.

### Supported Grant Types
* Authentication Code
* Implicit 
* User Credentials
* Client Credentials
* Refresh Token

WP OAuth Server does not currently support `Jwt Bearer` or `Crypto Tokens`.

## Installation

1. Upload `wordpress-oauth` to the `/wp-content/plugins/` directory or use the built-in plugin install system
1. Activate the plugin through the `Plugins` menu in WordPress
1. Click `Settings` and then `Permalinks`. Then simply click `Save Changes` to flush the rewrite rules.
1. You're Ready to Rock


## Adding a new Client?

Visit the dashboard by clicking `Provider` in the WordPress admin panel under `Setiings`. Once you are in the dashboard, there is a form labeled `Add Client`. Give your client a name and a redirect uri and description. The redirect uri is the HTTP location where the user will be returned to after authenticating (your client should provide this for you). Click `Add Client`.

## Authentication Documentation

*The following documentation assumes that you are famialr with PHP and at least a basic understand the workflow for OAuth 2.0 works.*

Since the main framework of this plugin was built on Brent Shaffers sevrver, you can follow his documentation. The only difference is the endpoints. The plugin endpoints are below:

- `/oauth/authorize`
- `oauth/token`

Brent Shaffer has created a very detailed Step-by-Step guide to using the Authentication API. You can view the 
homepage of this documentation [here](http://bshaffer.github.io/oauth2-server-php-docs/cookbook/). 



## Resource API

{STILL NEEDS DOCUMENTATION}