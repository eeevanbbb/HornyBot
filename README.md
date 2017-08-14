# HornyBot

## Requirements

- `python 2.7`
- TwitterBot credentials

## Installation

`pip install -r Requirements.txt`

## Usage
```
usage: HornyBot [-h] [--subjects SUBJECTS_FILE] [--twitter TWITTER_FILE]
                [--schedule SCHEDULE_FILE] [--used USED_FILE] [--debug]

Run HornyBot.

optional arguments:
  -h, --help            show this help message and exit
  --subjects SUBJECTS_FILE
                        The file containing things the bot is horny for, one
                        per line (default: config/subjects.txt)
  --twitter TWITTER_FILE
                        The file containing the Twitter keys, one per line
                        with the format key_name=key_value (default:
                        config/twitter.txt)
  --schedule SCHEDULE_FILE
                        The file containing the times to post each day, one
                        per line with the format HH:MM (default:
                        config/schedule.txt)
  --used USED_FILE      The file containing the subjects that have already
                        been used, one per line (default: config/used.txt)
  --debug               Ignore twitter config info, print tweets to the
                        command line instead
```

## Config Files

Customize this bot using configuration files. Configuration files specify the subjects about which the bot is horny, the twitter credentials for posting, the times each day to post, and a list of posts the bot has already sent. Each of these files has a default location in the `config` folder, but you can specify different files by using the flags shown above.

Config files are read once the bot is started and then ignored, so changes to the files will require restarting the bot.

### Subjects File

A list of subjects, one per line, about which the bot is horny. These will be tweeted in random order. The subjects will be appended with "-Horny" before being tweeted.

### Schedule File

A list of times, one per line, that the bot should tweet each day. These should be specified in zero-padded 24-hour time.

### Used Subjects File

This file contains a list of subjects the bot has already tweeted about, useful for stopping and restarting the bot without modifying the subjects list. If this file does not exist, one will be created when the first tweet is sent.

## TODO

- Add support for different times on different days
- Add more cool features like responding to tweets etc.