# OMNIVERSE Starter Template

## How this app was built from the official template

```sh
git clone https://github.com/NVIDIA-Omniverse/kit-app-template.git

cd kit-app-template

.\repo.bat template new

Accept Terms [Enter]

Select Application [Enter]

Kit Base Editor [Enter]

Enter name of application: [enterprise.devapp]

Enter application_display_name: [Dev App]



Do you want to add application layers? [No]

.\repo.bat build

.\repo.bat launch
```


## Quickstart

```sh
git clone https://github.com/iainashmore/omniverse-devapp.git

cd omniverse-devapp

.\repo.bat build

.\repo.bat launch
```

## How this extension was built from the official template

```sh
.\repo.bat template new

Accept Terms [Enter]

Select Extension 'Python UI Extension' [Down & Enter]

Enter name of extension: [enterprise.dev_extension]

Enter extension_display_name: Dev Extension

Enter version: 0.1.0 [Enter]
```

Add enterprise.dev_extension to the .kit file.
Within the .kit file for the editor application (/source/apps/enterprise.devapp.kit), add the new extension to the [dependencies] section:

[dependencies]
"enterprise.dev_extension" = {}

Open the newly created extension file (/source/extensions/enterprise/dev_extension/extension.py) and add the following python dependencies:

```sh
import omni.kit.commands
import omni.usd

from pxr import Sdf, Usd
import random
```

```sh
.\repo.bat build

.\repo.bat launch
```
