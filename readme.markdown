# lastfm.pl



## Installing

 1. Install `irssi` with Perl support.
 2. Install `Text::Template`, `JSON::XS`, `List::MoreUtils`, and `LWP::UserAgent`.
 3. Move `lastfm.pl` to your `.irssi/scripts` directory.
 4. Start `irssi`
 5. `/run ~/.irssi/scripts/lastfm.pl`
 6. Set your settings as needed.

## Settings
all settings are stored under lfmb

 - prefix
   - the bot prefix. 
   - default: "-"
 - get_player
   - do we fetch the player. 
   - only works with last.fm, 
   - default: OFF
 - default_site 
   - what site do we get information from. 
   - choices: last.fm or libre.fm
   - default: last.fm
 - np_output 
   - how do we display now playing output
   - see Text::Template for template details
 - owner  
   - the owners nick
   - default: 01 

## Commands 

Commands that access last.fm use the IRC nickname unless associated through .setuser.
Unlike IRC, all names are CASE SENSITIVE.

all commands have a prefix, this is set in irssi using /set lfmb_prefix <prefix>

### Everyone:
  - np [username]     
   - shows your currently playing song, or of another user if specified
  - compare u1 [u2]
   - compares yourself with u1 (another user) if u2 isn't specified compares u1 with u2 if both are given.
  - setuser user
   - associates the "user" last.fm username with your nickname.
  - whois username
   - given a last.fm username, return all nicknames that are associated to it.
  - deluser
   - removes your last.fm association.
  - source 
   - shows the source repo for the bot
  - version
   - shows the current version of the bot 

### Owner-only:
 - wp                - shows everyone's currently playing song
 - setuser nick user - associates the nick with the specified last.fm user
 - deluser nick      - removes the nick's association with his last.fm account

### Inline
 
 Some commands can be used with an inline form, so 
 you don't have to spam a channel with two lines to for example, show whats playing.
 To use these commands you use `<botnick>:<command>`, arguments can be added after 
 with another colon. 

