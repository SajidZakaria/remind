# Remind (+ Heroku)

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

A discord bot that sends reminders for future contests using [clist](https://clist.by/) API.

This repository helps to run Remind in heroku . For more information about Remind, check the [main repository](https://github.com/aryanc403/remind/).

---

## Steps for hosting a bot for your own server using Heroku.

1. Download the heroku CLI from [here](https://devcenter.heroku.com/articles/heroku-cli)
2. Now after installing the CLI, open up the CLI if you are on windows or open up a terminal if you are on linux.
3. Now enter the command `heroku login` and it will open up a link in the browser for login. Login using your credentials.
4. Now clone this repository from the terminal using the command `git clone https://github.com/SajidZakaria/remind.git`.
5. After cloning move into the REMIND directory using `cd remind`.
6. Now enter `heroku create` command in the terminal and hit enter. It will create a new app for you. Remember the name.
7. Now you need to add the Python buildpack to install essential packages.
8. To add Python buildpack type the following command `heroku buildpacks:add heroku/python`.
9. Now go to the personal dashboard [page](https://dashboard.heroku.com/apps) of heroku on your browser.
10. Next click on the app you created in step 6.
11. Now, go to resources and click on Find more add-ons and find Heroku Postgres.
12. Click to install the database on the Hobby Dev plan and set the app to the one that hosts the bot.
13. Go to settings tab and you will see a section called Config Vars. Click on the reveal config vars button.
14. Now you need to create a config var called BOT_TOKEN and paste your bot token created using discord and hit add. You might want to add a few more config vars depending on your needs (See the 'Config Vars' section).
15. Make sure that the name of the config var that contains the database url is named DATABASE_URL.
16. Now you are almost done. Type the following command `git push heroku master -f` and press enter.
17. It will take few minutes to build and deploy
18. After successful build open the heroku app in your browser. The same step as 9.
19. Go to Resources tab and turn on the worker. You are not charged for doing this its completely free.
20. That's it Enjoy!

#### Config Vars

- **BOT_TOKEN**: the Discord Bot Token for your bot.
- **CLIST_API_TOKEN**: your private clist token. Get it from [clist.by](https://clist.by/api/v2/doc/).
- **LOGGING_COG_CHANNEL_ID**: the [Discord Channel ID](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) of a Discord Channel where you want error messages sent to.
- **REMIND_MODERATOR_ROLE**: the name of the role that can run moderator commands of the bot. If this is not set, the role name will default to "Moderator".
- **TIME_ZONE**: to set the default timezone. You can get the list of available timezones in [timezones.txt](https://github.com/SajidZakaria/remind/blob/master/timezones.txt)

### Linting and Formatting

We are using [autopep8](https://github.com/hhatto/autopep8) for formatting the code.

## Credits

Shoutout to https://github.com/aryanc403/remind developer aryanc403 for creating the bot.  
Also thanks to [TLE](https://github.com/cheran-senthil/TLE) developers for the idea and initial contributions to this bot.  
Their bot used to remind about Codeforces contests and Remind is enhanced for all other judges.  

Special thanks to [TLE (+ Heroku)](https://github.com/ParsaAlizadeh/TLE/tree/hoi) developer ParsaAlizadeh. His work inspired me to port Remind for Heroku(I've also taken help from his README.MD :p).

## License
[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/aryanc403/remind/blob/master/LICENSE)

