# TiddlyWiki 5 Performance Test Rig

# Setup

1. Clone or download this repo
2. Run `npm install` in the root
3. Clone the repo https://github.com/Jermolene/TiddlyWiki5 into a sibling directory to this one called "TiddlyWiki5"

# Comparing two specific versions of TW with the test wiki

```
./compare-tiddlywiki-versions.sh v5.2.3 parameterised-transclusions ./tmp/
```

# Building and running specific versions of the test wiki

The following command builds the latest master and the previous v5.1.23 release:

```sh
./build-tiddlywiki-at-version.sh ./wiki v5.1.23 ./tmp/v5.1.23 && ./build-tiddlywiki-at-version.sh ./wiki master ./tmp/master
```

The following command runs the two wikis under Puppeteer and reports the performance log

```
node ./index.js ./tmp/v5.1.23/index.html && node ./index.js ./tmp/master/index.html 
```
