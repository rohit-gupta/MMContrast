

The dataset contains the following files:

math_urls.csv
literacy_urls.csv
background_urls.csv


format:
```
video ID,youtube url
```

e.g.

```
1088,https://www.youtube.com/watch?v=4YuP6ySZYvk
1092,https://www.youtube.com/watch?v=IPhqBO0C7cU
1095,https://www.youtube.com/watch?v=Uv55rB8RTIs
1096,https://www.youtube.com/watch?v=V6m9J4l0Qwg
...
```

The labels and data splits are provided in a dictionary file dumped using python stdlib's json.dump() function:
(Note that background videos are not included in any particular split, we use them all during training only)

approve_label_data.json:

```
{
  "test": {
    "math": {
      "<video ID>": [
       <list of class labels>
      ],
      "41509": [
        "addition_subtraction",
        "counting",
        "quantity_of_objects",
        "written_numerals"
      ],
      ...
    }
    "literacy": {
      ...
    }
  },
  "train": {
    "math": {
      ...
    }
    "literacy": {
      ...
    }
  },
  "val": {
    "math": {
      ...
    }
    "literacy": {
      ...
    }
  }
}
```