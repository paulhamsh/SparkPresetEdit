# SparkPresetEdit
How to edit a preset from Spark Amp

FIrst, set up the Spark app to use Dropbox:   

https://help.positivegrid.com/hc/en-us/articles/8141122585869-Backup-Restore-Tone-Presets   

Then log into Dropbox, find the Apps folder, then SparkAmp then download the zip file there.   
Unzip it.

Open the new folder.   
Within that folder will be folders per genre, then with those are a folder per tone. Sadly they are named with a UUID so you have to guess which one to use.   
Within each folder is a ```preset.json``` file - you need to edit this.   

It will look like this:

```
{"bpm":120,"type":"jamup_speaker","sigpath":[{"params":[{"value":0.33693364262580872,"index":0},{"value":0.42482039332389832,"index":1},{"value":1,"index":2}],"dspId":"bias.noisegate","active":true,"type":"speaker_fx"},{"params":[{"value":0.52851718664169312,"index":0},{"value":0.99913471937179565,"index":1}],"dspId":"Compressor","active":true,"type":"speaker_fx"},{"params":[{"value":0.55907392501831055,"index":0}],"dspId":"Booster","active":true,"type":"speaker_fx"},{"params":[{"value":0.27408850193023682,"index":0},{"value":0.46934801340103149,"index":1},{"value":0.50413221120834351,"index":2},{"value":0.33689036965370178,"index":3},{"value":0.11793193221092224,"index":4}],"dspId":"AC Boost","active":true,"type":"speaker_fx"},{"params":[{"value":0.37711864709854126,"index":0},{"value":0.56779658794403076,"index":1},{"value":0.21610170602798462,"index":2},{"value":0.25,"index":3}],"dspId":"ChorusAnalog","active":false,"type":"speaker_fx"},{"params":[{"value":0.15595102310180664,"index":0},{"value":0.23305083811283112,"index":1},{"value":0.49051162600517273,"index":2},{"value":0.60677969455718994,"index":3},{"value":1,"index":4}],"dspId":"DelayMono","active":false,"type":"speaker_fx"},{"params":[{"value":0.68880146741867065,"index":0},{"value":0.3928571343421936,"index":1},{"value":0.46113801002502441,"index":2},{"value":0.69370460510253906,"index":3},{"value":0.48823529481887817,"index":4},{"value":0.46638655662536621,"index":5},{"value":0.30000001192092896,"index":6},{"value":0,"index":7}],"dspId":"bias.reverb","active":false,"type":"speaker_fx"}],"meta":{"icon":"icon.png","version":"0.7","name":"PH AC","description":"1-Clean","id":"C9B595DB-EE2D-4BEC-A094-1DD97265FCC0"}}.   
```
So you might want to format it better, like this:
```
{"bpm":120,
"type":"jamup_speaker",
"sigpath":[
  {"params":[
    {"value":0.33693364262580872,"index":0},
    {"value":0.42482039332389832,"index":1},
    {"value":1,"index":2}],
    "dspId":"bias.noisegate",
    "active":true,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.52851718664169312,"index":0},
    {"value":0.99913471937179565,"index":1}],
    "dspId":"Compressor",
    "active":true,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.55907392501831055,"index":0}],
    "dspId":"Booster",
    "active":true,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.27408850193023682,"index":0},
    {"value":0.46934801340103149,"index":1},
    {"value":0.50413221120834351,"index":2},
    {"value":0.33689036965370178,"index":3},
    {"value":0.11793193221092224,"index":4}],
    "dspId":"AC Boost",
    "active":true,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.37711864709854126,"index":0},
    {"value":0.56779658794403076,"index":1},
    {"value":0.21610170602798462,"index":2},
    {"value":0.25,"index":3}],
    "dspId":"ChorusAnalog",
    "active":false,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.15595102310180664,"index":0},
    {"value":0.23305083811283112,"index":1},
    {"value":0.49051162600517273,"index":2},
    {"value":0.60677969455718994,"index":3},
    {"value":1,"index":4}],
    "dspId":"DelayMono",
    "active":false,
    "type":"speaker_fx"},
  {"params":[
    {"value":0.68880146741867065,"index":0},
    {"value":0.3928571343421936,"index":1},
    {"value":0.46113801002502441,"index":2},
    {"value":0.69370460510253906,"index":3},
    {"value":0.48823529481887817,"index":4},
    {"value":0.46638655662536621,"index":5},
    {"value":0.30000001192092896,"index":6},
    {"value":0,"index":7}],
    "dspId":"bias.reverb",
    "active":false,
    "type":"speaker_fx"}],
"meta":{
  "icon":"icon.png",
  "version":"0.7",
  "name":"PH AC",
  "description":"1-Clean","id":"C9B595DB-EE2D-4BEC-A094-1DD97265FCC0"}}
```  
  
Then you can move the effect sections around - these are the bits like:   
```
  {"params":[
    {"value":0.55907392501831055,"index":0}],
    "dspId":"Booster",
    "active":true,
    "type":"speaker_fx"},
```
Then you may need to remove all the formatting you did - not sure about that.   
Then zip up the SparkAmp folder and upload to Dropbox.    
Then in the Spark App, restore from DropBox.   
