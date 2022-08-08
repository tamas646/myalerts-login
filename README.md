# myalerts-login
Send email alert on SSH or direct login attempt.

## Usage
Just install it, and you will receive emails to `root@localhost` if someone logins through SSH or tries to login from tty.

Note that your system must use `rsyslog` for this to work properly.

I recommend you to redirect root's email address to your own in `/etc/aliases` unless you won't receive these emails. (alternatively you can change it directly in `/etc/rsyslog.d/myalerts-login.conf`)

It will use your server's mail system, so if you want this script to work properly you have to setup one for outgoing mails.

## Installation
- You can either [download](https://github.com/tamas646/myalerts-login/raw/main/myalerts-login_1.0.1_all.deb) and install the deb package or use the source code and setup it yourself.

- If you wish, you can install it from my apt repository too:

  ```sh
  sudo echo "deb [signed-by=/usr/share/keyrings/ptamas-pub.gpg] http://apt.ptamas.hu/main/ ./" > /etc/apt/sources.list.d/apt.ptamas.list
  wget -qO - https://apt.ptamas.hu/ptamas-pub.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/ptamas-pub.gpg > /dev/null
  apt update && apt install myalerts-login
  ```
