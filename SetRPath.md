### Setting R Path in Windows ###

In order to run R libraries, such as HOPACH through on Windows, you will need to set the Python PATH following installation of R. This will allow you to type "R" in the "Command Prompt" (under "All Programs" > "Accessories") in order to run R programs. Perform the following after installing R.

  1. Open "Control Panel>System>Advanced System Settings>Environmental Variables"
  1. Under "System Variables" open "PATH"
  1. Append the path of python to the paths (e.g., ";C:\R-3.0.3")
  1. Select the "OK" button.
  1. Open a new Command Prompt window and type "R". Something like the following should be displayed:

`R version 3.0.3 (2014-03-06) -- "Warm Puppy"`

`Copyright (C) 2014 The R Foundation for Statistical Computing`