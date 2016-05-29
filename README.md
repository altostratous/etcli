## Telegram messenger CLI [![Build Status](https://travis-ci.org/vysheng/tg.png)](https://travis-ci.org/vysheng/tg)

Command-line interface for [Telegram](http://telegram.org). Uses readline interface.

#Extended Telegram Cli (etcli)
This application is based on telegram-cli.

###Added features:
- now "history" and "get_message" commands return views count for messages as well.
- now "channel_info" returns about channel (Channel description) as well. 

###Common use for channels 
1 - channel_join <channel>	Joins to channel
2 - channel_leave <channel>	Leaves from channel
3 - history <peer> [limit] [offset]	Prints messages with this peer (most recent message lower). Also marks messages as read, views are shown as "views" both in json and text.
4 - channel_info <channel>	Prints info about channel (id, members, admin, description(about), name)
5 - get_message <msg-id>	Get message by id, number of views is represented as "views" as well.

###Commands in details based on telegram-cli:
accept_secret_chat <secret chat>	Accepts secret chat. Only useful with -E option
add_contact <phone> <first name> <last name>	Tries to add user to contact list
block_user <user>	Blocks user
broadcast <user>+ <text>	Sends text to several users at once
channel_get_admins <channel> [limit=100] [offset=0]	Gets channel admins
channel_get_members <channel> [limit=100] [offset=0]	Gets channel members
channel_info <channel>	Prints info about channel (id, members, admin, etc.)
channel_invite <channel> <user>	Invites user to channel
channel_join <channel>	Joins to channel
channel_kick <channel> <user>	Kicks user from channel
channel_leave <channel>	Leaves from channel
channel_list [limit=100] [offset=0]	List of last channels
channel_set_about <channel> <about>	Sets channel about info.
channel_set_admin <channel> <admin> <type>	Sets channel admin. 0 - not admin, 1 - moderator, 2 - editor
channel_set_username <channel> <username>	Sets channel username info.
channel_set_photo <channel> <filename>	Sets channel photo. Photo will be cropped to square
chat_add_user <chat> <user> [msgs-to-forward]	Adds user to chat. Sends him last msgs-to-forward message from this chat. Default 100
chat_del_user <chat> <user>	Deletes user from chat
chat_info <chat>	Prints info about chat (id, members, admin, etc.)
chat_set_photo <chat> <filename>	Sets chat photo. Photo will be cropped to square
chat_upgrade <chat>	Upgrades chat to megagroup
chat_with_peer <peer>	Interface option. All input will be treated as messages to this peer. Type /quit to end this mode
clear	Clears all data and exits. For debug.
contact_list	Prints contact list
contact_search username	Searches user by username
create_channel <name> <about> <user>+	Creates channel with users
create_group_chat <name> <user>+	Creates group chat with users
create_secret_chat <user>	Starts creation of secret chat
del_contact <user>	Deletes contact from contact list
delete_msg <msg-id>	Deletes message
dialog_list [limit=100] [offset=0]	List of last conversations
export_card	Prints card that can be imported by another user with import_card method
export_channel_link	Prints channel link that can be used to join to channel
export_chat_link	Prints chat link that can be used to join to chat
fwd <peer> <msg-id>+	Forwards message to peer. Forward to secret chats is forbidden
fwd_media <peer> <msg-id>	Forwards message media to peer. Forward to secret chats is forbidden. Result slightly differs from fwd
get_terms_of_service	Prints telegram's terms of service
get_message <msg-id>	Get message by id
get_self 	Get our user info
help [command]	Prints this help
history <peer> [limit] [offset]	Prints messages with this peer (most recent message lower). Also marks messages as read
import_card <card>	Gets user by card and prints it name. You can then send messages to him as usual
import_chat_link <hash>	Joins to chat by link
import_channel_link <hash>	Joins to channel by link
load_audio <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_channel_photo <channel>	Downloads file to downloads dirs. Prints file name after download end
load_chat_photo <chat>	Downloads file to downloads dirs. Prints file name after download end
load_document <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_document_thumb <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_file <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_file_thumb <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_photo <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_user_photo <user>	Downloads file to downloads dirs. Prints file name after download end
load_video <msg-id>	Downloads file to downloads dirs. Prints file name after download end
load_video_thumb <msg-id>	Downloads file to downloads dirs. Prints file name after download end
main_session	Sends updates to this connection (or terminal). Useful only with listening socket
mark_read <peer>	Marks messages with peer as read
msg <peer> <text>	Sends text message to peer
msg <peer> <kbd> <text>	Sends text message to peer with custom kbd
post <peer> <text>	Sends text message to peer as admin
post_audio <peer> <file>	Posts audio to peer
post_document <peer> <file>	Posts document to peer
post_file <peer> <file>	Sends document to peer
post_location <peer> <latitude> <longitude>	Sends geo location
post_photo <peer> <file> [caption]	Sends photo to peer
post_text <peer> <file>	Sends contents of text file as plain text message
post_video <peer> <file> [caption]	Sends video to peer
quit	Quits immediately
rename_channel <channel> <new name>	Renames channel
rename_chat <chat> <new name>	Renames chat
rename_contact <user> <first name> <last name>	Renames contact
reply <msg-id> <text>	Sends text reply to message
reply_audio <msg-id> <file>	Sends audio to peer
reply_contact <msg-id> <phone> <first-name> <last-name>	Sends contact (not necessary telegram user)
reply_document <msg-id> <file>	Sends document to peer
reply_file <msg-id> <file>	Sends document to peer
reply_location <msg-id> <latitude> <longitude>	Sends geo location
reply_photo <msg-id> <file> [caption]	Sends photo to peer
reply_video <msg-id> <file>	Sends video to peer
resolve_username username	Searches user by username
safe_quit	Waits for all queries to end, then quits
search [peer] [limit] [from] [to] [offset] pattern	Search for pattern in messages from date from to date to (unixtime) in messages with peer (if peer not present, in all messages)
send_audio <peer> <file>	Sends audio to peer
send_contact <peer> <phone> <first-name> <last-name>	Sends contact (not necessary telegram user)
send_document <peer> <file>	Sends document to peer
send_file <peer> <file>	Sends document to peer
send_location <peer> <latitude> <longitude>	Sends geo location
send_photo <peer> <file> [caption]	Sends photo to peer
send_text <peer> <file>	Sends contents of text file as plain text message
send_typing <peer> [status]	Sends typing notification. You can supply a custom status (range 0-10): none, typing, cancel, record video, upload video, record audio, upload audio, upload photo, upload document, geo, choose contact.
send_typing_abort <peer>	Sends typing notification abort
send_video <peer> <file> [caption]	Sends video to peer
set <param> <value>	Sets value of param. Currently available: log_level, debug_verbosity, alarm, msg_num
set_password <hint>	Sets password
set_profile_name <first-name> <last-name>	Sets profile name.
set_profile_photo <filename>	Sets profile photo. Photo will be cropped to square
set_ttl <secret chat>	Sets secret chat ttl. Client itself ignores ttl
set_username <name>	Sets username.
set_phone_number <phone>	Changes the phone number of this account
show_license	Prints contents of GPL license
start_bot <bot> <chat> <data>	Adds bot to chat
stats	For debug purpose
status_online	Sets status as online
status_offline	Sets status as offline
unblock_user <user>	Unblocks user
user_info <user>	Prints info about user (id, last online, phone)
version	Prints client and library version
view_audio <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_channel_photo <channel>	Downloads file to downloads dirs. Then tries to open it with system default action
view_chat_photo <chat>	Downloads file to downloads dirs. Then tries to open it with system default action
view_document <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_document_thumb <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_file <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_file_thumb <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_photo <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_user_photo <user>	Downloads file to downloads dirs. Then tries to open it with system default action
view_video <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view_video_thumb <msg-id>	Downloads file to downloads dirs. Then tries to open it with system default action
view <msg-id>	Tries to view message contents
visualize_key <secret chat>	Prints visualization of encryption key (first 16 bytes sha1 of it in fact)

### API, Protocol documentation

Documentation for Telegram API is available here: http://core.telegram.org/api

Documentation for MTproto protocol is available here: http://core.telegram.org/mtproto

### Upgrading to version 1.0

First of all, the binary is now in ./bin folder and is named telegram-cli. So be careful, not to use old binary.

Second, config folder is now ${HOME}/.telegram-cli

Third, database is not compatible with older versions, so you'll have to login again.

Fourth, in peer_name '#' are substitued to '@'. (Not applied to appending of '#%d' in case of two peers having same name).

### Installation

Clone GitHub Repository

     git clone --recursive https://github.com/vysheng/tg.git && cd tg

### Python Support

Python support is currently limited to Python 2.7 or Python 3.1+. Other versions may work but are not tested.

#### Linux and BSDs

Install libs: readline, openssl and (if you want to use config) libconfig, liblua, python and libjansson.
If you do not want to use them pass options --disable-libconfig, --disable-liblua, --disable-python and --disable-json respectively.

On Ubuntu/Debian use: 

     sudo apt-get install libreadline-dev libconfig-dev libssl-dev lua5.2 liblua5.2-dev libevent-dev libjansson-dev libpython-dev make 

On gentoo:

     sudo emerge -av sys-libs/readline dev-libs/libconfig dev-libs/openssl dev-lang/lua dev-libs/libevent dev-libs/jansson dev-lang/python

On Fedora:

     sudo dnf install lua-devel openssl-devel libconfig-devel readline-devel libevent-devel libjansson-devel python-devel

On Archlinux:

     yaourt -S telegram-cli-git

On FreeBSD:

     pkg install libconfig libexecinfo lua52 python

On OpenBSD:

     pkg_add libconfig libexecinfo lua python

On openSUSE:

     sudo zypper in lua-devel libconfig-devel readline-devel libevent-devel libjansson-devel python-devel libopenssl-devel

Then,

     ./configure
     make

#### Other methods to install on linux

On Gentoo: use ebuild provided.

On Arch: https://aur.archlinux.org/packages/telegram-cli-git

#### Mac OS X

The client depends on [readline library](http://cnswww.cns.cwru.edu/php/chet/readline/rltop.html) and [libconfig](http://www.hyperrealm.com/libconfig/), which are not included in OS X by default. You have to install these libraries manually.

If using [Homebrew](http://brew.sh/):

     brew install libconfig readline lua python libevent jansson
     export CFLAGS="-I/usr/local/include -I/usr/local/Cellar/readline/6.3.8/include"
     export LDFLAGS="-L/usr/local/lib -L/usr/local/Cellar/readline/6.3.8/lib"
     ./configure && make

Thanks to [@jfontan](https://github.com/vysheng/tg/issues/3#issuecomment-28293731) for this solution.

If using [MacPorts](https://www.macports.org):
     
     sudo port install libconfig-hr
     sudo port install readline
     sudo port install lua51
     sudo port install python34
     sudo port install libevent
     export CFLAGS="-I/usr/local/include -I/opt/local/include -I/opt/local/include/lua-5.1"
     export LDFLAGS="-L/usr/local/lib -L/opt/local/lib -L/opt/local/lib/lua-5.1"
     ./configure && make

Install these ports:

* devel/libconfig
* devel/libexecinfo
* lang/lua52

Then build:

     env CC=clang CFLAGS=-I/usr/local/include LDFLAGS=-L/usr/local/lib LUA=/usr/local/bin/lua52 LUA_INCLUDE=-I/usr/local/include/lua52 LUA_LIB=-llua-5.2 ./configure
     make

#### Other UNIX

If you manage to launch it on other UNIX, please let me know.

### Contacts 
If you would like to ask a question, you can write to my telegram or to the github (or both). To contact me via telegram, you should use import_card method with argument 000653bf:0738ca5d:5521fbac:29246815:a27d0cda


### Usage

    bin/telegram-cli -k <public-server-key>
    
By default, the public key is stored in tg-server.pub in the same folder or in /etc/telegram-cli/server.pub. If not, specify where to find it:

    bin/telegram-cli -k tg-server.pub

Client support TAB completion and command history.

Peer refers to the name of the contact or dialog and can be accessed by TAB completion.
For user contacts peer name is Name <underscore> Lastname with all spaces changed to underscores.
For chats it is it's title with all spaces changed to underscores
For encrypted chats it is <Exсlamation mark> <underscore> Name <underscore> Lastname with all spaces changed to underscores. 

If two or more peers have same name, <sharp>number is appended to the name. (for example A_B, A_B#1, A_B#2 and so on)
  
### Supported commands

#### Messaging

* **msg** \<peer\> Text - sends message to this peer
* **fwd** \<user\> \<msg-seqno\> - forward message to user. You can see message numbers starting client with -N
* **chat_with_peer** \<peer\> starts one on one chat session with this peer. /exit or /quit to end this mode.
* **add_contact** \<phone-number\> \<first-name\> \<last-name\> - tries to add contact to contact-list by phone
* **rename_contact** \<user\> \<first-name\> \<last-name\> - tries to rename contact. If you have another device it will be a fight
* **mark_read** \<peer\> - mark read all received messages with peer
* **delete_msg** \<msg-seqno\> - deletes message (not completly, though)
* **restore_msg** \<msg-seqno\> - restores delete message. Impossible for secret chats. Only possible short time (one hour, I think) after deletion

#### Multimedia

* **send_photo** \<peer\> \<photo-file-name\> - sends photo to peer
* **send_video** \<peer\> \<video-file-name\> - sends video to peer
* **send_text** \<peer\> \<text-file-name> - sends text file as plain messages
* **load_photo**/load_video/load_video_thumb/load_audio/load_document/load_document_thumb \<msg-seqno\> - loads photo/video/audio/document to download dir
* **view_photo**/view_video/view_video_thumb/view_audio/view_document/view_document_thumb \<msg-seqno\> - loads photo/video to download dir and starts system default viewer
* **fwd_media** \<msg-seqno\> send media in your message. Use this to prevent sharing info about author of media (though, it is possible to determine user_id from media itself, it is not possible get access_hash of this user)
* **set_profile_photo** \<photo-file-name\> - sets userpic. Photo should be square, or server will cut biggest central square part


#### Group chat options

* **chat_info** \<chat\> - prints info about chat
* **chat_add_user** \<chat\> \<user\> - add user to chat
* **chat_del_user** \<chat\> \<user\> - remove user from chat
* **rename_chat** \<chat\> \<new-name\>
* **create_group_chat** \<chat topic\> \<user1\> \<user2\> \<user3\> ... - creates a groupchat with users, use chat_add_user to add more users
* **chat_set_photo** \<chat\> \<photo-file-name\> - sets group chat photo. Same limits as for profile photos.

#### Search

* **search** \<peer\> pattern - searches pattern in messages with peer
* **global_search** pattern - searches pattern in all messages

#### Secret chat

* **create_secret_chat** \<user\> - creates secret chat with this user
* **visualize_key** \<secret_chat\> - prints visualization of encryption key. You should compare it to your partner's one
* **set_ttl** \<secret_chat\> \<ttl\> - sets ttl to secret chat. Though client does ignore it, client on other end can make use of it
* **accept_secret_chat** \<secret_chat\> - manually accept secret chat (only useful when starting with -E key)

#### Stats and various info

* **user_info** \<user\> - prints info about user
* **history** \<peer\> [limit] - prints history (and marks it as read). Default limit = 40
* **dialog_list** - prints info about your dialogs
* **contact_list** - prints info about users in your contact list
* **suggested_contacts** - print info about contacts, you have max common friends
* **stats** - just for debugging
* **show_license** - prints contents of GPLv2
* **help** - prints this help
* **get_self** - get our user info

#### Card
* **export_card** - print your 'card' that anyone can later use to import your contact
* **import_card** \<card\> - gets user by card. You can write messages to him after that.

#### Other
* **quit** - quit
* **safe_quit** - wait for all queries to end then quit
