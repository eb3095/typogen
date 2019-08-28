# typogen
Introduce configurable typos into a string.

### Usage

```javascript
// Require the project
const Typo = require('typogen').Typo;

// This library will load a default config unless one is specified
// See bellow for the details of the config structure
var config = require('./defaults.json');

// Create the Typo object
var typo = new Typo(config);

// Take a string
let string = "This is a common string. There are some things we could misspell. Don't forget it's random!";

// Introduce typos at random
string = typo.introduceTypos(string);

console.log(string);
```

### Configuration

* typoRate is in 10ths of a percent. 1 = 0.1%, 10 = 1%, 100 = 10%.
* typoCommas is to forget commas
* typoApostrophes is to forget apostrophes
* typoCase is to forget to capitalize
* speechParts.string is the word to be misspelled
* speechParts.typos are the randomly chosen typos to introduce

Json Configuration,
```json
{
  "typoRate": 100,
  "typoCommas": true,
  "typoApostrophes": true,
  "typoCase": true,
  "speechParts": [
    {
      "string": "they're",
      "typos": [
        "theyre",
        "there",
        "their"
      ]
    },
    {
      "string": "theyre",
      "typos": [
        "there",
        "their"
      ]
    },
    {
      "string": "their",
      "typos": [
        "there",
        "theyre"
      ]
    },
    {
      "string": "there",
      "typos": [
        "theyre",
        "their"
      ]
    },
    {
      "string": "your",
      "typos": [
        "youre"
      ]
    },
    {
      "string": "youre",
      "typos": [
        "your"
      ]
    },
    {
      "string": "you're",
      "typos": [
        "your"
      ]
    },
    {
      "string": "you",
      "typos": [
        "u"
      ]
    },
    {
      "string": "ei",
      "typos": [
        "ie",
        "ee"
      ]
    },
    {
      "string": "ie",
      "typos": [
        "ee",
        "ei"
      ]
    },
    {
      "string": "ai",
      "typos": [
        "ia"
      ]
    },
    {
      "string": "ia",
      "typos": [
        "ai"
      ]
    },
    {
      "string": "qu",
      "typos": [
        "q"
      ]
    }
  ]
}
```

Javascript Configuration
```javascript
var config = {
    typoRate: 100,
    typoCommas: true,
    typoApostrophes: true,
    typoCase: true,
    speechParts: [
        {
            string: "they're",
            typos: [
                "theyre",
                "there",
                "their"
            ]
        },
        {
            string: "theyre",
            typos: [
                "there",
                "their"
            ]
        },
        {
            string: "their",
            typos: [
                "there",
                "theyre"
            ]
        },
        {
            string: "there",
            typos: [
                "theyre",
                "their"
            ]
        },
        {
            string: "your",
            typos: [
                "youre"
            ]
        },
        {
            string: "youre",
            typos: [
                "your"
            ]
        },
        {
            string: "you're",
            typos: [
                "your"
            ]
        },
        {
            string: "you",
            typos: [
                "u"
            ]
        },
        {
            string: "ei",
            typos: [
                "ie",
                "ee"
            ]
        },
        {
            string: "ie",
            typos: [
                "ee",
                "ei"
            ]
        },
        {
            string: "ai",
            typos: [
                "ia"
            ]
        },
        {
            string: "ia",
            typos: [
                "ai"
            ]
        },
        {
            string: "qu",
            typos: [
                "q"
            ]
        }
    ]
};
```