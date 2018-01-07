# wiki-actors

Some random exploration of Oscars data.
See [related blogpost](https://cldellow.com/bash/2018/01/06/scraping-wikipedia-using-bash.html)


## Setup

### pup

```
wget https://github.com/ericchiang/pup/releases/download/v0.4.0/pup_v0.4.0_linux_amd64.zip
unzip pup_v0.4.0_linux_amd64.zip
sudo mv pup /usr/bin/pup
```

### jq

```
wget https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64
sudo mv jq-linux64 /usr/bin/jq
```

### ministat

```
sudo apt-get install ministat
```

## Usage

Run `./wp` to see options.

Sample output:

```
$ ./wp infobox George_Clooney
[...html spew...]

$ ./wp bday George_Clooney
1961-05-06

$ ./wp age George_Clooney
56

$ ./wp age George_Clooney 1970-07-20
9

$ ./wp best_actor | head -n5
1927 1 Emil_Jannings won
1927 1 Richard_Barthelmess nominated
1928 2 Warner_Baxter won
1928 2 George_Bancroft_(actor) nominated
1928 2 Chester_Morris nominated

$ ./wp ages best_actor | head -n5
1927 1 Emil_Jannings won 42
1927 1 Richard_Barthelmess nominated 31
1928 2 Warner_Baxter won 38
1928 2 George_Bancroft_(actor) nominated 45
1928 2 Chester_Morris nominated 26
```
