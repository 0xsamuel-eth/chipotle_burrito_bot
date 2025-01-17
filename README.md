# Twitter->Message Bot
### A bot to automate Chipotle Tweet code-to-message promotions, using the [twscrape](https://github.com/vladkens/twscrape) API scrapper.

___
## Install & Requirements

* Python 3.10+
* Mac with iMessages enabled
* Text Message forwarding enabled
* valid twitter account
___
### Install
```
git clone https://github.com/awliu2/free-burritos.git
cd free-burritos
pip3 install -r requirements.txt
```

or `pip`, whichever one works for you.
___
## Setup

1. Ensure you have python3.10+ [latest version here](https://www.python.org/downloads/). 

2. Update pip:
    ```
    pip3 install --upgrade pip
    ```

3. Make sure to install the twscrape dependency using 
    ```
    pip3 install -r requirements.txt
    ```

4. Navigate to the `free-burritos` directory. Update the contents of `config.py` with the credentials of a valid twitter account. 

    ```
    login = {
        "email" : "john@gmail.com",
        "username" : "johnstwitter",
        "password" : "password123",
    }
    ```

5. Make sure you have text message forwarding enabled for your iMessages account: [instructions here.](https://support.apple.com/en-us/HT208386)

6. The first time you run the script, you may be prompted to grant terminal access to iMessages. Do so in system preferences.

7. You'll need to have a message log with "888222". So open iMessages and send them anything, otherwise the applescript will fail.
___
## Usage
Open iMessages, and start a new message with the Chipotle short code number (888222), make sure that it is on the top of your window, and run:
```
python3 burrito_bot.py
```
___
## Notes

* The twitter API has a 250 request per 15 minutes per account limit. Thus, if the script does not seem to be working, but it is able to locate the imessage window, the API request is likely timing out. (250 seconds / 2 seconds per request $\approx$ 8.3 minutes of continuous runtime before timing out).

___
## Credit
* credit to [awliu2](https://github.com/awliu2/), [baolong281](https://github.com/baolong281/), and [EvilWumpus](https://github.com/EvilWumpus/) for creating repos with similar intentions and code. A lot of what is compiled here is mixed and matched from these three repos, the majority being from the forked repo of [awliu2/free-burritos](https://github.com/awliu2/free-burritos).

* credit to [baolong281](https://github.com/baolong281/infinite-food-glitch) for the twscrape code used in original repo
