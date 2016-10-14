== README
== <img src="https://s3.amazonaws.com/libra-static/libra_logo_full_white-01.png">

## Setup

1. Clone the repo via SSH or https.
2. Goto your project path (i.e. ~/marketplace-ui) in Finder/File Explorer.
3. Rename `**database.sample.yml**` to `**database.yml**`.
4. Then open `**Terminal**` and goto path `~/marketplace`
5. Type `bundle install` (assuming you have bundler installed) to install the necessary gems for the project.

Assuming you have Mac or Linux installed you need the following components via **Homebrew(brew)** or **Advanced Packing Tool(apt)**.

1. Postgresql
2. Paperclip
3. Nodejs(for Messaging system) which can also be downloaded from nodejs website.
<br><br>

## Getting Started

####Linux
1. In your ~/marketplace-ui path type `rake db:create db:migrate db:seed`
2. Start your Unicorn server by typing `rails s`
3. Goto your browser and type `lvh.me:3000` for Client/Professional login or `libra.lvh.me:3000` for Professional only login to get started.

####Mac
1. In your ~/marketplace-ui path type `rake db:create db:migrate db:seed`
2. Since Multi-Domain setup, Goto this folder `/private/etc` and edit the `**hosts**` file and add this line<br> `127.0.0.1	lvh.me` after existing `127.0.0.1	localhost`
3. Start your Unicorn server by typing `rails s -b 0.0.0.0`.
4. Goto your browser and type `lvh.me:3000` to get started.
<br><br>

## Misc
1. For getting localities list for different areas, create a folder in your `**~/User**` directory named `vs_csv` and inside `vs_csv` add `localities.csv` and then goto terminal and run this rake command<br> `rake import:localities_from_csv`
2. To setup and get 2-Factor-Authentication working for your professional profile run this rake command<br> `rake users:build_google_secret`
