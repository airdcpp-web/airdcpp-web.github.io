---
layout: documentation
title: Submitting translations
description: Setting up an own hub
category: Advanced
order: 7.7
---

*Translation support is available starting from version 2.6.0*

# Submitting translations

You may use [Transifex](https://www.transifex.com/airdcpp/airdcpp/) to translate the application strings online.

Anyone who has created an account on the site is able to submit new translations. After registration, choose the language that you want to translate and submit a request to join the language team.

## Testing translations

You may download your newly made translations from [Transifex](https://www.transifex.com/airdcpp/airdcpp/) for testing them in the application before they made available to all users.

### Testing Web UI translations

**Translation resource**: webui.main.json

1. Create a new directory ```<webui root>/js/locales/<language code>``` and put your translation file into that directory (the filename must be `webui.main.json`)
2. If there are existing locale files for the same language in ```<webui root>/js/locales```, you must delete/rename those (all files starting with your language code) so that the new files get downloaded
3. Clear the browser cache and reload the Web UI page (this can be generally done with Ctrl+F5)



### Testing core application translations

**Translation resource**: EN_Example.xml

Core application translations are being downloaded automatically by the application once per night. You may also replace the translation files with the files downloaded from [Transifex](https://www.transifex.com/airdcpp/airdcpp/). Just note that some strings aren't displayed correctly for manually downloaded translations but they will be converted to the correct format by the script that manages language updates on the update site.

