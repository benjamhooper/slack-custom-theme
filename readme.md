# Windows Install

1. Please have [NodeJS](https://nodejs.org/en/download/) Installed.

2. If they're fonts used in the theme you will have to manually installed those specified by the theme designer.

3. You must have Powershell 5.0, aka Windows 10 to get full compatibility. If you don't have Windows 10 install the latest [powershell](https://github.com/PowerShell/PowerShell#get-powershell) for windows.

4. When running this script always run powershell in **Adminstrator Mode**. Hit your windows start button then type `powershell`, right click powershell, then `Run as administrator`.

**Note:**

- These instructions are error handled in the script.
- Please restart/close powershell if you have installed NodeJS during this install. This will refresh your environment variables to which NodeJS/Windows uses for commands. If you have [Chocolatey](https://chocolatey.org/) installed just type `refreshenv` while in powershell and run the install command below without closing/restarting powershell.

## Install

To install theme just open powershell as administrator (Refer to #4 above) and run this command below.

`iex (new-object net.webclient).downloadstring('https://raw.githubusercontent.com/benjamhooper/slack-custom-theme/master/slackcustomtheme.ps1')`

### Potential Errors

1. If you get an error when you try and run the install command above you might need to change the execution policy (i.e. enable Powershell). You need to be an administrator on your computer to do this.

    Open powershell(Refer to #4 above) and run this command: `Set-ExecutionPolicy RemoteSigned -scope CurrentUser`

2. If you happen to get this error. While the command `npx asar extract app.asar app.asar.unpackedcustom` has run:

```powershell
npm ERR! code ENOLOCAL
npm ERR! Could not install from "...\AppData\Roaming\npm-cache\_npx\*****" as it does not contain a package.json file.

npm ERR! A complete log of this run can be found in:
npm ERR!     "C:\Users\...\AppData\Roaming\npm-cache\_logs\**********-debug.log
Install for asar@latest failed with code 1"
```

Please enter this: `npm config set cache C:\tmp\nodejs\npm-cache --global` -- [Origin](https://github.com/zkat/npx/issues/146#issuecomment-384016791)

# Contributors

[benjamhooper](https://github.com/benjamhooper/) - Maintainer & Designer
