# WordPress Plugin Debugging Tools Documentation
## Table of Contents
### 1. WordPress Configuration Settings
     define( 'WP_DEBUG', true );
     define( 'WP_DEBUG_LOG', true );
     define( 'WP_DEBUG_DISPLAY', true );
     define( 'SCRIPT_DEBUG', true );
### 2. Basic Debugging Plugins
  *  [Die Dumper (DD)](https://github.com/adreastrian/dd)
  *  [Debug Toolkit](https://wordpress.org/plugins/debug-toolkit/) by [hellofromTonya](https://knowthecode.io/)
  *  [Query Monitor](https://wordpress.org/plugins/query-monitor/) by [John Blackbourn](https://querymonitor.com/)
### 3. Mobile and Web Live Server Debugging
  * Herd/Valet Live Server Setup
     ```bash
     define('WP_SITEURL', 'http://' . $_SERVER['HTTP_HOST']);
     define('WP_HOME', 'http://' . $_SERVER['HTTP_HOST']);
     ```

  * Relative URL Plugin
     * Installation and Activation

  * Command for Live Server
      ```bash
      herd share    //for herd server
      valet share   //for valet server
      ```
### 4. Email Debugging
   * Ensure Mail Server is Running
       ```bash
       brew services list
       To run: brew services start mailhog
       ```
   * Use an SMTP Plugin 
     * [Mailhog for WordPress](https://wordpress.org/plugins/wp-mailhog-smtp/)
     * [FluentSTMP](https://wordpress.org/plugins/fluent-smtp/)
   * Mail Dashboard
     ```bash
      URL: mail.test:8025 // For mailhog
     ```
### 5. Additional Plugin Debugging Tools
   * [Debug Bar](https://wordpress.org/plugins/debug-bar/) By [wordpressdotorg](https://wordpress.org/)
   * Query Monitor Plugin Extension 


## 1. WordPress Configuration Settings
To enable debugging in WordPress plugins, make sure the following lines are added to your plugin's ``wp-config.php`` file:
```bash
define( 'WP_DEBUG', true );
define( 'WP_DEBUG_LOG', true );
define( 'WP_DEBUG_DISPLAY', true );
define( 'SCRIPT_DEBUG', true );
```

These settings will log errors, display them, and enable script debugging for your plugin.


## 2. Basic Debugging Plugins
### * Die Dumper (DD)
Die Dumper is a debugging tool that helps you inspect variables and data during runtime. Install and activate the plugin in your WordPress environment to use it for debugging your plugin.
### * Debug Toolkit - Hello from Tonya
Debug Toolkit by Tonya is another essential plugin for debugging. It provides various tools and features to streamline the debugging process for your plugin development.
### * Query Monitor
Query Monitor is a powerful debugging tool that gives you insights into database queries, PHP errors, and more. Install and activate the plugin within your plugin environment for in-depth debugging capabilities.


## 3. Mobile and Web Live Server Debugging
### * Herd/Valet Live Server Setup
Add the following lines to your plugin's ``wp-config.php`` file:
```bash
define('WP_SITEURL', 'http://' . $_SERVER['HTTP_HOST']);
define('WP_HOME', 'http://' . $_SERVER['HTTP_HOST']);
```
Install and activate the Relative URL plugin within your plugin environment to address any file path issues.

Run the command ``herd share`` in your plugin's root directory to set up a live server for debugging.


## 4. Email Debugging
### * Ensure Mail Server is Running
Check if your mail server is running using the command:
```bash
brew services start mailhog
```
### * To start the mail server, use:
```bash
brew services start mailhog
```

### Use an SMTP Plugin
Install an SMTP plugin like [MailHog for WordPress](https://wordpress.org/plugins/wp-mailhog-smtp/) By [Tareq Hasan](https://tareq.co) or [FluentSMTP] by [FluentSMTP & WPManageNinja Team](https://fluentsmtp.com) within your plugin environment to debug email-related issues.

### * Mail Dashboard (For Mailhog)
Access the mail dashboard at mail.test:8025 within your plugin environment to monitor and debug emails sent from your WordPress plugin.


## 5. Additional Plugin Debugging Tools
### * Debug Bar
Debug Bar is a plugin that adds a debugging menu to the admin bar, providing insights into database queries, hooks, and more. Install and activate this plugin for additional debugging capabilities.
### * Query Monitor Plugin Extension
Extend the functionality of Query Monitor with additional features specific to plugin development. Install and activate this extension for enhanced debugging tools.

This documentation provides a comprehensive guide to debugging WordPress plugins using various tools and configurations. Follow these steps to enhance your plugin development workflow and identify and resolve issues efficiently.

