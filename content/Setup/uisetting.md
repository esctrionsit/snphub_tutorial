# UI Setting

**Optional**.Sometimes you may want the UI has some default value on the browser. Here is a fast way to set them. Just fill the json below, save it as a json file like `ui.json`. Then, change the value of **path_UIsetting** in the `config.R` as the path of your own UI setting json.

```json
{
    "VarTable": {
        "Samples1": "List of samples, must have variant",
        "Samples2": "List of samples, must NOT have variant",
        "Samples3": "List of samples, independent of having variant",
        "Region": "",
        "Flanking": "0"
    },
    "Heatmap": {
        "Region": "",
        "Flanking": "0",
        "Groups": ""
    },
    "HapNet": {
        "Region": "",
        "Flanking": "0",
        "Groups": ""
    },
    "PhyloTree": {
        "Region": "",
        "Flanking": "0",
        "Groups": ""
    },
    "HapMap": {
        "Samples": "",
        "Region": ""
    },
    "SnpFreq": {
        "Samples": "",
        "Region": "",
        "Flanking": "0",
        "tracks": "0"
    },
    "SeqMaker": {
        "Samples": "",
        "Region": ""
    }
}
```