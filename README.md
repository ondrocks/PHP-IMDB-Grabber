# PHP IMDB.com Grabber

**This class enables you to retrieve data from IMDB.com with PHP.**

*The script is a proof of concept. It's working, but you shouldn't use it, since IMDB does not allow this method of data grabbing!*

The technique used is called “web scraping” (see [Wikipedia](http://en.wikipedia.org/wiki/Web_scraping "Web scraping") for details). That means: If IMDB changes anything on their HTML, the script is going to fail.

---

Did you know about the available IMDB.com API? The price to use it is around $15.000. This might be fine for commercial projects, but it's impossible to afford for private/non-commercial ones.

---

**If you want to thank me for my work and the support, feel free to do this through PayPal (use mail@fabian-beiner.de as payment destination) or just buy me a book at Amazon (http://www.amazon.de/wishlist/3IAUEEEY6GD20) – thank you! :-)**

## Changes

5.2.2

- Forgot a link in getCastAndCharacterAsUrl() function

5.2.1

- Added getCastAndCharacter() and getCastAndCharacterAsUrl() *(Thanks to Taha Demirhan for snippets)*
- Added imdb.search.php - a small example search form *(Thanks to xsabianus)*

5.2.0

- Added series functions getSeasons() and getCreator()/getCreatorAsUrl() *(Coded by mali11011)*

5.1.1

- Fixed getCastAsUrl(); *(Reported by od3n)*

5.1.0

- Throws an exception if there is no posters/cache directory or cURL available
- Some code cleanup
- Added IMDB_LOCATION

5.0.4

- Removed/cleaned some variable names
- Fixed IMDB_POSTER regular expression
- Changed IMDB_PLOT regular expression

5.0.3

- Fixed regular expression for title

5.0.2

- Added regular expression for original title (which I prefer instead of the localized one)

5.0.1

- Renamed 'redirects' to 'cache'
- Added a simple caching mechanism. Defaults to one day (1440 minutes). Feel free to change this: **new IMDB('Movie', 60)** (for one hour). This speeds up everything dramatically.
- Removed /10 from rating return

5.0.0

- **Complete rewrite**
- Added caching for redirects
- Fixed ALL regular expressions according to new IMDB layout
- Added getBudget function
- Added debug option

## Bugs?
If you run into a problem, feel free to contact me. I will help you if my time allows it. However, support is not guaranteed.

I will only answer bug report if you provide me a detailed output of the failing script – please enable debug through setting "**const IMDB_DEBUG = true;**" in imdb.class.php.

## Wishes?

Add your wish to the project wiki or send me an email.

## Usage

The usage of this script is simple. Just have a look at imdb.example.php – you will understand easily how it works.

## Example output (of imdb.example.php)

![Screenshot](http://img801.imageshack.us/img801/3749/imdbc.png "Screenshot of imdb.example.php output")
