42_ft_irc 💬

🌟 About the Project

42_ft_irc is my implementation of an Internet Relay Chat (IRC) server, built as part of the 42 Abu Dhabi Common Core. This project dives into the world of real-time messaging, allowing multiple clients to connect, chat, and manage channels over TCP/IP. I used C++ 98 to create a robust server that handles authentication, messaging, and channel operations, all while working with a real IRC client for testing. It’s a team project that taught me the power of collaboration and networking!

🛠️ Features

Mandatory Part

Core Functionality:

Handles multiple clients simultaneously using non-blocking I/O with poll().

Supports TCP/IP (v4 or v6) for communication.

Requires a port and password to connect: ./ircserv <port> <password>.

Client Features (tested with a reference IRC client):

Authenticate, set a nickname, and username.

Join channels, send/receive private messages, and broadcast messages to channel members.

User Roles:

Operators and regular users with distinct privileges.

Channel Operator Commands:

KICK: Eject a client from a channel.

INVITE: Invite a client to a channel.

TOPIC: View or change the channel topic.

MODE: Manage channel modes:

i: Toggle invite-only mode.

t: Restrict topic changes to operators.

k: Set/remove channel password.

o: Grant/revoke operator privileges.

l: Set/remove user limit.

Bonus Part (Optional, if implemented)

File transfer between clients.

A bot for automated responses.

🚀 How to Use

1️⃣ Clone the Repository

git clone https://github.com/nourdev777/42_ft_irc.git

2️⃣ Compile the Server

make

Clean up:

make fclean

Recompile:

make re

3️⃣ Run the Server

./ircserv <port> <password>

Example:

./ircserv 6667 mypassword

4️⃣ Test with an IRC Client

Use a reference IRC client (e.g., HexChat, irssi, or WeeChat) to connect to your server.

Connect to localhost:<port> with the password you set.

Try commands like NICK, USER, JOIN, PRIVMSG, and operator commands (KICK, INVITE, etc.).

5️⃣ Simple Test with nc (Netcat)

To test basic communication, you can use nc:

nc 127.0.0.1 6667

Send commands in parts (e.g., com, man, d\n) to verify the server aggregates packets correctly.

💡 What I Learned

Building a network server using TCP/IP and non-blocking I/O with poll().

Writing C++ 98 code with modern practices (e.g., preferring <cstring> over <string.h>).

Managing multiple clients and ensuring the server never hangs.

Implementing IRC protocol features like authentication, channels, and operator commands.

Teamwork: Collaborating with peers to design, code, and debug a complex system.

Handling error cases like partial data, low bandwidth, and client disconnections.

📜 Original Task

Check out the full assignment details: here

Built with collaboration at 42 Abu Dhabi! ☕️🚀
