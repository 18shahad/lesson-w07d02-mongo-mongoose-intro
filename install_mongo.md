[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)![Misk Logo](https://i.ibb.co/KmXhJbm/Webp-net-resizeimage-1.png)

# Install Mongo

## Install with Homebrew

- [Homebrew: The missing package manager for macOS](https://brew.sh/)
- [Mongo Manual Install](https://docs.mongodb.com/manual/installation/)

* Check if homebrew is installed: `brew`

      	* If not, install [Homebrew](https://brew.sh/) by following the instructions on the web page
      	* If brew is already installed `brew upgrade`.

* **Install Mongodb on Mac OS X:** `brew install mongodb`

## Set data location

In terminal type `brew services start mongodb` to run the mongo server.

You will probably get an error saying

> "Data directory `/data/db` not found., terminating"

    - if so, you will need to make the directories in your **root** directory as follows (do these commands anywhere):

- Create data directories (at the root level)
  _ `sudo mkdir /data`
  _ `sudo mkdir /data/db`

- Next, set root permissions \* `sudo chmod -R 777 /data`

Run the mongo server again: `mongod`.

Should see: "waiting for connections on port 27017"

## Open and close mongo

- Open another terminal tab `cmd + T` and type `mongo`

- To quit `mongo`, type `exit` or `quit()`.

- To quit `mongod` hit `control+c`

Finished!

## Errors

If at some point you get an error with `mongod`:

1. `ps -A | grep mongod`
1. find the line that just mentions `mongod`, but not `grep`
1. take note of the number on the left
1. type `kill 1774` or whatever that number is. Try `mongod` again.
1. If that doesn't work, go to `/data/db` and `rm mongod.lock`. Try `mongod` again.

## Down the Rabbit Hole: Hungry for More

[Understanding Permissions](https://www.elated.com/articles/understanding-permissions/)
