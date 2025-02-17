

The dataset contains the following files which provide a list of YouTube videos:

`math_urls.csv`

`literacy_urls.csv`

`background_urls.csv`


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

The labels and train/val/test split information is provided in a dictionary file dumped using python stdlib's json.dump() function:
(Note that background videos are not included in any particular split, we use them all during training only)

`approve_label_data.json`

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

## License
Copyright (and other rights) to the APPROVE annotations are reserved by SRI International and are provided for non-commercial use by researchers under the CC-BY-NC 4.0 license. See [LICENSE](LICENSE) for details.


