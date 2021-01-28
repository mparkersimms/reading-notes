# Class 14 
## [Home Page](../README.md)

#### References:

Article on local storage for web applications



No.7. The past, present and future of local storage for web applications

Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides
- Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
- Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
- Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful


A brief history of local storage hacks before html5

- internet explorer
    - userData allows web pages to store up to 64 KB of data per domain
- in 2002 flash 6 was invented 
    - flash cookies properly known as local shared objects
        - allows objects to store 100 kbs of data per domain

- 2007 google launched Gears 
    - open source plugin 
    - provided extra capabilities
    - provides an API to an embedded SQL database based on SQLite
    - unlimited amounts of data per domain in SQL database
- dojox.storage upgrades
    - provide a unified interface to all these different plugins and APIs
    - could auto-detect adobe flash, gears, adobe AIR and early protoypes of HTML5

HTML 5 storage 

- "web storage"

- "local storage" or "DOM storage"

- a way for web pages to store named key/value paris locally, within the client web browser
- data persists even after you navigate away from the website, close the browser, exit your browser etc. 

- never transmitted to the remote web server, 
- available even when third party browswer plugins arent

- accessed through the localStorage object on the global window object

- before you can use it, you should detect whether your browser supports it. 

- function supports_html5_storage () {
    try {
        return 'localStorage' in window && window ['localStorage'] !== null;
    } catch (e) {
        return false;
    }
}
- if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}

Using HTML5 Storage

- HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string

- can be any type supported by JavaScript, including strings, Booleans, integers, or floats

- actually stored as a string

- If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype

- interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};

- Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

- There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};

- Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).

interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
   - If you call key() with an index that is not between 0–(length-1), the function will return null.

Tracking Changes to the HTML5 Storage Area

- If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something

- The storage event is supported everywhere the localStorage object is supported,

- if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};

HTML5 Storage in action

- calling this function saves data everytime a change happens on the page 

- function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}

