# jpdb-phrase-list

Uses [jpdb.io](https://jpdb.io/) exported reviews to show a list of phrases you ~~should~~ *could* be able to read.
Made using [AlpineJS](https://alpinejs.dev/) and [Bootstrap](https://getbootstrap.com/docs/5.3/).

## How to use

Open `index.html` on your browser or [host it](https://www.google.com/search?client=firefox-b-d&q=how+to+host+a+html+file) somewhere for you.

## Disclaimer

WIP, maybe forever. Showing sentences directly on the page won't work for a number of reasons you can see below. **You can still use it**: we give you a link to [Tatoeba](https://tatoeba.org/) with a nice query, where you can read the phrases with the words selected.

### jpdb.io *doesn't* export everything needed

* We don't know any words you marked as **Never Forget** or as **Blacklisted**.
* We also don't know the **exact** algorithm used to give a **grasp/known** score; a questionable version of the [SM-0 algorithm](https://www.supermemo.com/en/blog/application-of-a-computer-to-improve-the-results-obtained-in-working-with-the-supermemo-method) + linear interpolation was used instead, which seems to work ~~i guess~~.

This means we don't accurately recognize all words you know or not.

### Todo to support actual phrases on the page

* CORS config on tatoeba server - can be worked around with a CORS proxy
* localStorage has a limit of 10mb - need to strip and filter all saved data
* bz2 library takes way too long (+50s) - load a good WASM library
* Need for conjugated words - add a dictionary to the mess as well
