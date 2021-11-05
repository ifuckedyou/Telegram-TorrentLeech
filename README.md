 #  androidဖုန််းသုံးပြီး Telegram-TorrentLeech bot လုပ်နည်း

## Guide:
-  YouTube Link:[Tutorial video](https://youtu.be/vCj3_kufRCc)
-----

-  အရင်ဆုံး Termux ကို မိမိဖုန်းထဲ install လုပ်ပါ။Termux ကို ​အောက်ကပုံ နိပ်ပြီး downloadလုပ်ပါ
[![](x.png)version 0.117](https://drive.google.com/uc?export=download&id=19VycS90NijIR1u_KYTumRJDu4c2xKK7P)
--------
##  Service Accounts မလုပ်တက်ရင် ​အောက်ကနည်းအတိုင်းပြုလုပ်ပါ
<details>
    <summary><b>service accounts လုပ်နည်း</b></summary>
Guide:


- YouTube Link: https://youtu.be/LGWk-UeW4ls
------

```
termux-setup-storage
```
```
pkg update
```
```
pkg upgrade 
```
```
pkg install git
```
```
pkg install python
```
```
pip install --upgrade pip
```
```
mkdir /sdcard/MyTermux/ -p
```
```
cd /sdcard/MyTermux
```
```
git clone https://github.com/phoethar1/service-accounts
```
```
cd /sdcard/MyTermux/service-accounts
```
```
pip3 install -r requirements.txt
```
credentials.json file ကို [Google Console](https://console.cloud.google.com/?pli=1)မှာပြုလုပ်ပါ

```
python3 gen_sa_accounts.py --quick-setup -1
```
```
python3 gen_sa_accounts.py  --download-keys Project ID
```
[`Project ID​`](#) နေရာမှာ မိမိ Project IDထည့်

```
python generate_drive_token.py
```
```
cd accounts
```
```
python3 emails.py
```
</details>
          

   [Create Service Accounts](https://github.com/phoethar1/service-accounts)

--------
Telegram-TorrentLeech bot လုပ်နည်း
----------
```
termux-setup-storage
```
```
pkg update
```
```
pkg upgrade 
```
```
pkg install git
```
```
git config --global user.email "မိမိgmailထည့်@example.com"
```
```
git config --global user.name " Name ထည့်"
```
```
pkg install nodejs-lts
```
```
npm install -g heroku
```
```
npm install -g http-server
```
```
mkdir /sdcard/MyTermux/ -p
```
<summary><b>rclone config လုပ်နည်း</b></summary>
```
pkg install python
```
```
pkg install rclone
```
```










```
cd /sdcard/MyTermux
```
```
git clone https://github.com/phoethar1/Telegram-TorrentLeech
```
[`မိမိဖုန်းfile manager ထဲက MyTermuxဆိုတဲ့ folder ထဲဝင် service-accountsဆိုတဲ့ folderထဲက accounts folderကို Telegram-TorrentLeechဆိုတဲ့ folderထဲမှာ copy လုပ်ပြီးထည့် 
ပြီးရင် Telegram-TorrentLeech folderထဲက config.envကို ဖွင့်ပြီး မိမိ account နဲ သက်ဆိုင်တဲ့ တန်ဖိုးကို ပြင်ဆင်သတ်မှတ်ပါ`](#)

--------
-  confing.env ဖွင့်မရရင် ​[ဒီLINK က app](https://www.google.com/url?sa=t&source=web&rct=j&url=https://play.google.com/store/apps/details%3Fid%3Dcom.rhmsoft.edit%26hl%3Dmy%26gl%3DUS%26referrer%3Dutm_source%253Dgoogle%2526utm_medium%253Dorganic%2526utm_term%253Dquickedit%26pcampaignid%3DAPPU_1_ovhvYZL5C4e6qtsP5cWDsA4&ved=2ahUKEwiS0uPc7NjzAhUHnWoFHeXiAOYQ5YQBegQIBhAC&sqi=2&usg=AOvVaw1CNFUinhUrTrs3FLQFv64Q)ကိုdownloadလုပ် ပြီးရင်confing.env.txt​ ခန name changeလိုက် ဖြည့်စရာဖြည့်ပြီးရင် နဂို name (config.env )rename ပြန်လုပ်
--------
-  TG_BOT_TOKEN ​နေရာမှာ [BotFather](https://t.me/BotFather)က​နေToken ယူပြီးဖြည့်

-  APP_ID ​နေရာမှာ [my.telegram.org](my.telegram.org)မှာ loginဝင်ပြီးAPI developments tools ထဲက App api_id ကိုcopy လုပ်ပြီးဖြည့်ပါ ပြီးရင်App api_hashကို copyလုပ်ပြီး API_HASH ​နေရာမှာဖြည့်လိုက်ပါ

-  OWNER_ID ​နေရာမှာ [MissRose_bot](https://t.me/MissRose_bot)မှာ/idလို့ ပို့လိုက် idကျလာရင် idကို copy လုပ်ပီးဖြည့်လိုက်

-  AUTH_CHANNEL ​နေရာမှာ group id ဖြည့်

```
cd Telegram-TorrentLeech
```
```
heroku login
```
[`Enter ပြန်​ခေါက် Browser ​ပေါ်​ရောက်သွာမယ်`](#)

```
heroku create appname
```
[`appname က unique ဖြစ်နိုင်တာ ထားပါ`](#)
```
heroku stack:set container
```
```
git add *
```
```
git commit -m "Telegram-TorrentLeech"
```
```
git push heroku main
```


















<details>
    <summary><b>မူရင်းrepo၏README.md</b></summary>




 # Telegram Torrent Leecher
  
  A Telegram Torrent (and youtube-dl) Leecher based on [Pyrogram](https://github.com/pyrogram/pyrogram)
  ---
<p><a href="https://hub.docker.com/r/reaitten/tgtlg"> <img src="https://img.shields.io/docker/pulls/reaitten/tgtlg?style=for-the-badge" width="150""/></a> <a href="https://hub.docker.com/layers/reaitten/tgtlg/latest/images/sha256-2f8b28fa0b7998fcc917589e211c40d4621ac0eb4181cb96a4d18bfcb74e368c?context=explore"> <img src="https://img.shields.io/docker/image-size/reaitten/tgtlg/latest?style=for-the-badge" width="150""/></a> <a href="https://github.com/reaitten/tgtlg"> <img src="https://img.shields.io/github/repo-size/reaitten/tgtlg?style=for-the-badge" width="150"/></a> <a href="https://github.com/reaitten/tgtlg/blob/main/LICENSE"> <img src="https://img.shields.io/github/license/reaitten/tgtlg?style=for-the-badge" width="150"/></a></p> 
  
  ![GitHub Repo stars](https://img.shields.io/github/stars/reaitten/tgtlg?style=social) ![GitHub forks](https://img.shields.io/github/forks/reaitten/tgtlg?style=social)
  ---
  # Table of Contents
  
- [Benefits](#benefits)
- [To-Do](#to-do)
  * [Deployment](#deployment)
    + [Simple Way](#simple-way)
      - [Instructions](#instructions)
    + [Deploy on VPS](#deploy-on-vps)
      - [Setup `config.env`](#setup-configenv)
        * [Setup rclone](#setup-rclone)
      - [Deploying](#deploying)
    + [The Legacy Way](#the-legacy-way)
  * [Variable Explanations](#variable-explanations)
    + [Mandatory Variables](#mandatory-variables)
    + [Optional Configuration Variables](#optional-configuration-variables)
    + [Available Commands](#available-commands)
  * [How to Use?](#how-to-use)
  * [Credits](#credits-and-thanks-to)

  # Benefits
      ✓ Google Drive link cloning using gclone. (WIP)
      ✓ Telegram File mirrorring to cloud along with its unzipping, unrar and untar
      ✓ Drive/Teamdrive support/All other cloud services rclone.org supports
      ✓ Extract compatible archive
      ✓ Custom file name
      ✓ Custom commands
      ✓ Get total size of your working cloud directory
      ✓ You can also upload files downloaded from /ytdl command to gdrive using `/ytdl gdrive` command.
      ✓ You can also deploy this on your VPS
      ✓ Option to select either video will be uploaded as document or streamable
      ✓ Added /rename command to clear the downloads which are not deleted automatically.
      ✓ Added support for youtube playlist
      ✓ Renaming of Telegram files support added.
      ✓ Changing rclone destination config on fly (By using `/rclone` in private mode)
      
  # To-Do
  -   [ ] Adding mp3 files support while playlist downloading.
  -   [ ] Password support while Unarchiving the files.
  -   [ ] Selection of required files during leeching the big files using aria(/leech command)

  ## Deployment

  ### Simple Way

  #### Instructions 

  **Modified for use on Heroku, please do not heavily abuse!**

  **Join [this](https://t.me/tgleechsupport) Telegram Group if you want support, I will try to help you as much as I can.**

  <p><a href="https://heroku.com/deploy?template=https://github.com/phoethar1/Telegram-TorrentLeech"> <img src="https://img.shields.io/badge/Deploy%20To%20Heroku-blueviolet?style=for-the-badge&logo=heroku" width="200""/></a></p>

  ## Deploy on VPS

  - Clone this repo:
  ```
  git clone -b main https://github.com/reaitten/tgtlg tgtlg
  cd tgtlg
  ```

  - Install requirements
  For Debian based distros
  ```
  sudo snap install docker
  ```
  Install Docker by following the [official docker docs](https://docs.docker.com/engine/install/debian/)

  ### Setup `config.env`
  ```
  cp sample_config.env config.env
  ```
  After this step you will see a new file named ```config.env``` in root directory.

  Fill those compulsory variables.

  If you need more explanation about any variable then read [app.json](https://github.com/reaitten/tgtlg/blob/deploy-main/app.json)

  ### Setup rclone

  1. Set rclone locally by following the official repo: https://rclone.org/docs/
  2. Get your `rclone.conf` file will look something like this:
  
  ```
  [NAME]
  type = 
  scope =
  token =
  client_id = 
  client_secret = 
  ```
  
  3. Copy `rclone.conf` file in the root directory (Where `Dockerfile` exists).

  4. Your config can contains multiple drive entries. (Default: First one and change using `/rclone` command)

  ### Deploying

  - Start Docker Daemon (skip if already running):
  ```
  sudo dockerd
  ```
  - Build Docker Image:
  ```
  sudo docker build . -t torrentleech-gdrive
  ```
  - Run the image:
  ```
  sudo docker run torrentleech-gdrive
  ```
  Follow this [Video Tutorial](https://youtu.be/J3tMbngA9DE)
  ### The Legacy Way
  Simply clone the repository and run the main file:

  ```
  git clone -b 4forks https://github.com/reaitten/tgtlg
  cd TorrentLeech-Gdrive
  python3 -m venv venv
  . ./venv/bin/activate
  pip install -r requirements.txt
  # Create config.py appropriately
  python3 -m tgtlg
  ```
  ## Variable Explanations

  ### Mandatory Variables

  - `TG_BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API token.

  - `APP_ID`
  
  - `API_HASH`: Get these two values from [my.telegram.org/apps](https://my.telegram.org/apps).
    * N.B.: if Telegram is blocked by your ISP, try our [Telegram bot](https://telegram.dog/UseTGXBot) to get the IDs.

  - `AUTH_CHANNEL`: Create a Super Group in Telegram, add `@GoogleIMGBot` to the group, and send /id in the chat, to get this value.

  - `OWNER_ID`: ID of the bot owner, He/she can be abled to access bot in bot only mode too(private mode).

  ### Optional Configuration Variables

<details>
      <summary><b>Click Here for more Details</b></summary>


  - `DOWNLOAD_LOCATION`: 
  The location you would like the bot to download to locally.

  - `BOT_CMD_POSTFIX`:   
  If you want the bot to respond to you when you send a command along with the bot username. 
  Usage Example: /command@botusername
  Example Value: @mybotsusername
  Defualt Value is "".
  
  - `LEECH_COMMAND`:
  Change the /leech command.
  Defualt Value is "leech"
  - `LEECH_UNZIP_COMMAND`:
   Change the /extract command.
  Defualt Value is "extract"
  - `LEECH_ZIP_COMMAND`:
  Change the /archive command.
  Defualt Value is "archive" 
  - `YTDL_COMMAND`:
  Change the /ytdl command.
  Defualt Value is "ytdl"
  - `GYTDL_COMMAND`:
  Change the /gytdl command.
  Defualt Value is "gytdl"
  - `PYTDL_COMMAND`:
  Change the /pytdl command.
  Defualt Value is "pytdl"
  - `GLEECH_COMMAND`:
  Change the /gleech command.
  Defualt Value is "gleech"
  - `TELEGRAM_LEECH_COMMAND`:
  Change the /tleech command.
  Defualt Value is "tleech"
  - `TELEGRAM_LEECH_UNZIP_COMMAND`:
  Change the /textract command.
  Defualt Value is "textract"
  - `CLONE_COMMAND_G`:
  Change the /gclone command.
  Defualt Value is "gclone"
  - `UPLOAD_COMMAND`:
  Change the /upload command.
  Defualt Value is "upload"
  - `RENEWME_COMMAND`:
  Change the /leech command.
  Defualt Value is "leech"
  - `SAVE_THUMBNAIL`:
  Change the /savethumb command.
  Defualt Value is "savethumb"
  - `CLEAR_THUMBNAIL`:
  Change the /clearthumb command.
  Defualt Value is "clearthumb"
  - `GET_SIZE_G`:
  Change the /clearthumb command.
  Defualt Value is "clearthumb"
  - `TOGGLE_VID`:
  Change the /togglevid command.
  Defualt Value is "togglevid"
  - `TOGGLE_DOC`:
  Change the /toggledoc command.
  Defualt Value is "toggledoc"
  - `RENAME_COMMAND`:
  Change the /rename command.
  Defualt Value is "rename"
  - `CANCEL_COMMAND_G`:
  Change the /cancel command.
  Defualt Value is "cancel"

  - `MAX_FILE_SIZE`:
  - `TG_MAX_FILE_SIZE`:
  - `FREE_USER_MAX_FILE_SIZE`
  - `MAX_TG_SPLIT_FILE_SIZE`:
  - `CHUNK_SIZE`:
  - `MAX_MESSAGE_LENGTH`:
  - `PROCESS_MAX_TIMEOUT`:
  - `ARIA_TWO_STARTED_PORT`:
  - `EDIT_SLEEP_TIME_OUT`:
  - `MAX_TIME_TO_WAIT_FOR_TORRENTS_TO_START`:
  - `FINISHED_PROGRESS_STR`:
  - `UN_FINISHED_PROGRESS_STR`:
  - `TG_OFFENSIVE_API`:
  - `CUSTOM_FILE_NAME`:

  - `UPLOAD_AS_DOC`: Takes two option True or False. If True file will be uploaded as document. This is for people who wants video files as document instead of streamable.

  - `INDEX_LINK`: (Without `/` at last of the link, otherwise u will get error) During creating index, plz fill `Default Root ID` with the id of your `DESTINATION_FOLDER` after creating. Otherwise index will not work properly.

  - `DESTINATION_FOLDER`: Name of your folder in your respective drive where you want to upload the files using the bot.

</details>

  ### Available Commands

  - `/rclone`: This will change your drive config on fly. (First one will be default)
  - `/gclone`: This command is used to clone gdrive files or folder using gclone.

  - `/help`: To get a list of commands

  - `/leech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [this command will SPAM the chat and send the downloads a seperate files if there is more than one file, in the specified torrent]
  - `/archive`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. [This command will create a .tar.gz file of the output directory, and send the files in the chat, splited into PARTS of 1024MiB each, due to Telegram limitations]
  - `/extract`: This will unarchive file and upload to telegram.

  - `/gleech`: This command should be used as reply to a magnetic link, a torrent link, or a direct link. And this will download the files from the given link or torrent and will upload to the cloud using rclone.
  - `/garchive`: This command will compress the folder/file and will upload to your cloud.
  - `/gextract`: This will unarchive file and upload to cloud.
  - `/gclone`: This command is used to clone gdrive files or folder using gclone.

Syntax: `[ID of the file or folder][one space][name of your folder only (If the ID is of file, don't put anything)]` and then reply /gclone to it.

  - `/tleech`: This will mirror the telegram files to your respective cloud.
  - `/textract`: This will unarchive telegram file and upload to cloud.

  - `/ytdl`: This command should be used as reply to a [supported link](https://ytdl-org.github.io/youtube-dl/supportedsites.html)
  - `/pytdl`: This command will download videos from youtube playlist link and will upload to telegram.
  - `/gytdl`: This will download and upload to your cloud.
  - `/gpytdl`: This download youtube playlist and upload to your cloud.
  - `/getsize`: This will give you total size of your destination folder in cloud.
  - `/renewme`: This will clear the remains of downloads which are not getting deleted after upload of the file or after /cancel command.
  - `/rename`: To rename the telegram files.

  - `/rclone`: This will change your drive config on fly. (First one will be default)
  - `/log`: This will send you a txt file of the logs.

Only works with direct link and youtube link for now.
You can add a custom name as it's prefix to the file. Example: if gk.txt uploaded will be what you add in CUSTOM_FILE_NAME + gk.txt

  You can add a custom name as it's prefix of the original file name.
  e.g: if file is `gk.txt` uploaded will be what you added in ``CUSTOM_FILE_NAME`` + ``gk.txt``
  It is like you can add custom name as prefix of the original file name.
  Like if your file name is `gk.txt` uploaded will be what u add in `CUSTOM_FILE_NAME` + `gk.txt`

  ## How to Use?

  * send any one of the available commands, as a reply to a valid link/magnet/torrent.


  ## Credits
  - [GautamKumar](https://github.com/gautamajay52/TorrentLeech-Gdrive)
  - [SpEcHiDe](https://github.com/SpEcHiDe/PublicLeech) for his wonderful code
  - [cihanvol](https://github.com/cihanvol) for [direct_link_generator](https://github.com/reaitten/tgtlg/blob/main/tgtlg/helper_funcs/direct_link_generator.py)
  - [MaxxRider](https://github.com/MaxxRider) for tweaked version of [TorrentLeech-Gdrive](https://github.com/MaxxRider/Leech-Pro)
  - [Rclone Team](https://rclone.org) for theirs awesome tool
  - [Dan Tès](https://telegram.dog/haskell) for his [Pyrogram Library](https://github.com/pyrogram/pyrogram)
  - [Robots](https://telegram.dog/Robots) for their [@UploadBot](https://telegram.dog/UploadBot)
  - [@AjeeshNair](https://telegram.dog/AjeeshNait) for his [torrent.ajee.sh](https://torrent.ajee.sh)
  - [@gotstc](https://telegram.dog/gotstc), @aryanvikash, [@HasibulKabir](https://telegram.dog/HasibulKabir) for their TORRENT groups
