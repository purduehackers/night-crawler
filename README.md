# night crawler
crawls around `#hack-night` in the purdue hackers discord waiting for you to share something. fork of [blairhackclub/scrappy](https://github.com/blairhackclub/scrappy). currently used for [purduehackers/night](https://github.com/purduehackers/night).

<img width="418" alt="Screen Shot 2022-10-17 at 10 23 11 PM" src="https://user-images.githubusercontent.com/14811170/196320643-99ce97af-7f52-455c-9c85-47813e79a08f.png">

## Environment variables
- AIRTABLE_BASE_ID
- AIRTABLE_API_KEY
- CLIENT_ID
- TOKEN
- GUILD_ID
- SCRAPBOOK_CHANNEL_ID

## Airtable integration
This bot integrates with an Airtable base to store and manage data. The base should have the following tables with the following fields:
- `Scraps` table
  - `Scrap ID`: Autonumber
  - `Created time`: Created time
  - `Discord Message ID`: Single line text
  - `Discord Thread ID`: Single line text
  - `Description`: Long text
  - `Attachments`: Attachment
  - `Tags`: Multiple select (not implemented yet)
  - `Mentions`: Link to Users, Allow linking to multiple records (not implemented yet)
  - `User`: Link to Users
  - `User Record ID`: Lookup, User, Record ID
  - `Username (from User)`: Lookup, User, Username
  - `Avatar (from User)`: Lookup, User, Avatar
- `Users` table
  - `Username`: Single line text
  - `Record ID`: Formula, `RECORD_ID()` (optional)
  - `Discord UID`: Single line text
  - `Avatar`: Attachment,
  - `GitHub User`: Single line text (not implemented yet)
  - `Website`: Single line text (not implemented yet)
  - `Scraps`: Link to Scraps, Allow linking to multiple records
  - `Mentions`: Link to scraps, Allow linking to multiple records (not implemented yet)

Read more about Airtable's API: https://airtable.com/api
