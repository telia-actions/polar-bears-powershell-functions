# polar-bears-powershell-functions
Action that allows to import some powershell functions to use in workflows running on Windows runners.

## Usage example

```
jobs:
  example-job:
    steps:
      - uses: actions/checkout@v4

      - name: Setup PowerShell functions
        uses: telia-actions/polar-bears-powershell-functions@v1

      - name: Use the functions (step 1)
        shell: pwsh
        run: |
          Import-Module PolarBearsPSFunctions
          Copy-Files -Source "Some/Source/Path" -Destination "Some/Destination/Path"
```

## Available functions

### Copy-Files
Copies files from given source directory to given destination directory using robocopy

Parameters:
* [string]$Source
* [string]$Destination
