# German-Words-Library in JSON

This is a collection of 2 German word lists. One 1.6 million words long. The other 5,000 words long.

# Features
- JSON format
- original spelling including uppercase and lowercase
- original spelling including letters liket `ä`, `ö`, `ü`, `ß`, ect.
- Two sizes: 1,6M and 5K.
- The 5000 words have been selected randomly
- Both lists are alphabetically sorted

# Files

```
["Abbaumaschinen",
"Abbauorte",
"Abbausituationen",
"Abendwache",
"Abfallens",
"Abfalltasche",
...
"übersäten",
"überzeugend",
"üblicheres"]

```

# Original source
- https://raw.githubusercontent.com/WithEnglishWeCan/generated-german-words-full-list/master/words.full.list.build.txt
- This has only a 1.6M words file and its in a TXT format.

# Example usage in JavaScript

- Raw link (5000 words): https://raw.githubusercontent.com/Jonny-exe/German-Words-Library/master/German-words-5000-words.json
- Raw link (1.6 M words): https://raw.githubusercontent.com/Jonny-exe/German-Words-Library/master/German-words-1600000-words.json

```
var getJSON = function(url, callback) {
  var xhr = new XMLHttpRequest();
  xhr.open('GET', url, true);
  xhr.responseType = 'json';
  xhr.onload = function() {
    var status = xhr.status;
    if (status === 200) {
      callback(null, xhr.response);
    } else {
      callback(status, xhr.response);
    }
  };
  xhr.send();
};

getJSON('https://raw.githubusercontent.com/Jonny-exe/German-Words-Library/master/German-words-5000-words.json',
    function(err, data) {  
      if (err !== null) {
        alert('Something went wrong: ' + err);
      } else {
        // Data is the JS array
      }
    }
  );
```

# Enjoy 
