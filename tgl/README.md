###Extended Telegram Cli (etcli)
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

#Commands in details based on telegram-cli:
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

### Description about the project which this project is forked from.

This is library that handles telegram api and protocol.

Current versions:

- scheme.tl: Layer 38
- encrypted_scheme.tl: Layer 23

### API, Protocol documentation

Documentation for Telegram API is available here: https://core.telegram.org/api

Documentation for MTproto protocol is available here: https://core.telegram.org/mtproto

### Installation

Clone GitHub Repository

     git clone --recursive  https://github.com/vysheng/tgl.git && cd tgl

#### Linux and BSDs

Install libs: openssl, zlib
if you want to use provided net/timers then install libevent and add --enable-libevent key to configure

You can also avoid the OpenSSL dependency: Install gcrypt (>= 1.60, Debian derivates know it as "libgcrypt20-dev"), and add --disable-openssl key to configure

Then,

     ./configure
     make

### Contacts 
If you would like to ask a question, you can write to my telegram or to the github (or both). To contact me via telegram, you should use import_card method with argument 000653bf:0738ca5d:5521fbac:29246815:a27d0cda

