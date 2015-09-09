TermFeed
====


**Term**inal **Feed** is a *minimal* feed **reader** for the terminal (without curses).

To read, preview, open, store, or delete your favorite RSS feeds from the command line.

#### Why?

If 1) you are a terminal addict, and 2) you want to stay up to date with the outside world by reading quick feed and summaries WITHOUT having to leave your terminal; then TermFeed is for you. These are the main reasons I created TermFeed.

> Note: it's a pre-alpha release so nothing is so perfect.

### Usage

`$ feed`

- browse latest feed from your favorite rss sources (links stored under the default category `General`).

`$ feed <RSS-LINK>`

- browse latest feed from the single link `<RSS-LINK>` provided.
- e.g. `$ feed https://news.ycombinator.com/rss`

`$ feed -b`

- browse latest feeds by category of your library.

`$ feed -p <CATEGORY>`

- preview the RSS sources stored under <CATEGORY> in your library. 


`$ feed -a <RSS-LINK>`

- add new link to your rss library.

`$ feed -d <RSS-LINK>`

- delete a link from your rss library.



See `$ feed -h` for detailed usage.

### Features (what you can do?)

- Colorful text.
- Preview a short summary of a selected feed.
- Jump to (open) the source page of a feed in default browser.


### Examples

<!-- see: TermFeed gifs repo: http://imgur.com/a/EBHho
-->

Default browsing 

![default](http://i.imgur.com/CXFFIaF.gif?1)

Browse by topic 

![browse topics](http://i.imgur.com/J09EFVv.gif?1)

Update library (Add or delete links)

![add delete](http://i.imgur.com/wcHdK4l.gif?1)

Help

![help menu](http://i.imgur.com/Cnbbq2U.gif?1)


### Installation

1) from `PyPI` repository:

	$ pip install TermFeed


download and unpack the [zipped folder](https://github.com/iamaziz/TermFeed/archive/master.zip), then:

2) from the source distribution, 

	$ cd TermFeed
	$ python setup.py install

Or 
3) Alternatively link the executeable `feed.py` from the downloaded folder to some directory in your `PATH`, e.g.

	ln -s ~/Downloads/TermFeed/termfeed/feed.py /usr/local/bin/feed

### Uninstall


	$ pip uninstall TermFeed

I use a data file (`.termfeed.db`) as a mini-database to maintain the RSS URLs.
This file is created at the home directory (e.g. `$HOME/.termfeed.db`), delete it as well.


> Remember, you may need to run these commands as an admin e.g.
> 	`$ sudo ...`


#### Dependencies

- [feedparser](https://pypi.python.org/pypi/feedparser)


#### Miscellaneous

- Tested on OS X and Linux.
- Supports Python 2.7 and Python 3.4
- The URLs in `urls.py` are complementary. They will be added to your library at `$HOME/.termfeed.db` when you run TermFeed (`$ feed`) for the first time. You may delete them all and have your own list instead. 
- To re-initialize your feeds library (database) from `url.py`, delete `.termfeed.db`. TermFeed checks for that data file with every run, if it's not there it will be created from the feeds in `url.py`.
- [Instant RSS Search](http://ctrlq.org/rss) is a nice search engine for searching RSS feeds.


### Author

- Aziz Alto