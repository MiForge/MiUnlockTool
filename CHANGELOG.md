### Version 1.4.8:

- Make the installation method easier, just download and run the file, it will take care of the rest.
- Other improvements

### Version 1.4.9:

- Improvements and fixes

### Version 1.5.0:

- un-lock has been restructured and rebuilt.
- Improved and reduced un-lock size.
- un-lock is now compatible with all operating systems.
- Resolved the "securityStatus16" issue and fixed other problems.

#### Version 1.5.0 (Update):
- Deleted `cmd getvar all` in `def CheckB` and replaced it with `getvar token` and `getvar product`.
- In case of failure to obtain `deviceToken` and `product`, added a step to enter them manually.
- Other improvements

#### Version 1.5.0 (Update):
- Simplified cookie extraction for concise code.
- Streamlined URL determination for better clarity based on the geographical region.
- Specified "https" directly in the `Url` constructor for secure communication and improved clarity.
- Deleted requests to "/api/v3/unlock/userinfo" and "/api/v2/unlock/device/clear" to reduce code size as they are not currently important.
- Adjusted message formatting for enhanced readability.
- Changed `cmd = "tfastboot"` to `cmd = "fastboot"`. Also, removed `adb`.

### Tool name update: "un-lock" is now "MiUnlockTool".

#### Version 1.5.0 (Update):
- Minor bug fix
- Add command (cmd, "oem", "get_token")
- In the event of failure to obtain the device token, the user will be asked to enter it manually
- Other improvements

#### Version 1.5.0 (Update):
- When 2 or more tokens are obtained via the festboot oem get_token ..
tool will now merge them automatically

#### Version 1.5.0 (Update):
- Updated client version to 7.6.727.43.
- Improved unlocking process.

#### Version 1.5.0 (Update):
- Save keys:values ​​directly

#### Version 1.5.0 (Update):
- Added a step to check if the com.termux.api application is installed ..

#### Version 1.5.0 (Update):
- A few users are experiencing an issue regarding "Check if device is connected in bootloader mode..."
Due to the slow transmission with the device
So the time was increased from 1s to [6s](https://github.com/offici5l/MiUnlockTool/blob/main/MiUnlockTool.py#L112)

#### Version 1.5.0 (Update):
- get tokens(deviceToken) and merging them Automatically done. ( MTK devices )

#### Version 1.5.0 (Update):
- Add ability to choose server(host region) from terminal

#### Version 1.5.0 (Update):
- Adding some improvements

#### Version 1.5.0 (Update):
- improvements

#### Version 1.5.0 (Update):
- Skip saving device information such as token and product, so as not to cause problems during unlocking...
- improvements

#### Version 1.5.0 (Update):
- Adding some improvements

#### Version 1.5.0 (Update):
- Correct the issue of the confirmation page not opening in Linux

#### Version 1.5.0 (Update):
- fix ( For Linux( and termux ) users : the 401 issue .... during account confirmation ... )

#### Version 1.5.0 (Update):
- add colorama to handle colors instead of ANSI
- Add requests to access the region and deal with the region, to send the request to the correct server accurately
- improvements

#### Version 1.5.0 (Update):
- Adding some improvements

#### Version 1.5.0 (Update):
- Add manual mode to unlock the bootloader

#### Version 1.5.0 (Update):
- Enhanced request security and improved access to region data to fix issues "code 20033"

#### Version 1.5.0 (Update):
- Replace command "oem device-info" with "getvar unloked"

#### Version 1.5.0 (Update):
- Adding steps to deal with "security Status 4", regarding adding email to xiaomi account This will fix "Failed to get pass Token"

#### Version 1.5.0 (Update):
- Re-added request 'api/v2/unlock/device/clear' to check if the device is cleared or not After unlocking bootloader

### Version 1.5.1:
- improvements
- Simplified browser login: Confirm login instead of re-entering credentials

### Version 1.5.1 (Update):
- Simplified browser login canceled currently due to some problems. so Means »
- `fix "Invalid link"`

### Version 1.5.2:
- Fix `"device is not recognized but termux-api popup appears !"`
- Improvements
- Delete some unimportant messages ..

### Version 1.5.2 (Update):
- Add a step to verify that storage access(termux-setup-storage) is granted


### Version 1.5.3:
- A global variable connect was added to track the device connection status. the code now checks for device connection only if it hasn't been connected yet, reducing redundant checks.
This will reduce the process time by about half, and it cannot be reduced further because the problem is with termux &termux-api itself.

- Add some messages to let the user know that the process is in progress.


### Version 1.5.4:
- Edit the encryptData save path to be in /sdcard/encryptData Instead of being in /sdcard/Download/encryptData ( this will fix the issue :
FileNotFoundError: [Errno 2] No such file or directory: '/sdcard/Download/encryptData' )


### Version 1.5.5:
- Output management has been enhanced by using threads to read from stdout and stderr concurrently, which reduces verification delays and improves system responsiveness.

- The fastboot devices command has been removed from the verification process, which reduces the number of executed commands and increases process efficiency. (This will minimize waiting time for devices facing issues.)

- Manual input on failure has been removed and some unnecessary elements have been eliminated.


### Version 1.5.5 (Update):

[#L289-L323:](https://github.com/offici5l/MiUnlockTool/blob/main/MiUnlockTool.py#L289-L323)

- Retry 4 attempts, in case of failure to get phone info

- Add print the type of SoC, based on the order that gets the token.

### Version 1.5.6:

- Remove manual mode, and remove some functions that are no longer necessary. 
- Some improvements, to handle jobs better.
- Fix the issue with termux (Error message: fastboot: error: cannot load /sdcard/encryptData) , due to some termux-setup-storage issues, the encryptData will now be saved in $PREFIX/bin instead of /sdcard...
- Other improvements in the installation process regarding Termux.

### Version 1.5.7:

- Enhanced performance of functions. 
- Automatically update the MiUnlockTool if a new version is available.

### Version 1.5.8:

- fix "FileNotFoundError: ...fastboot"

### Version 1.5.9:

- minor bug fixes

### Version 1.6.0:

(The project has been completely restructured from a single MiUnlockTool.py script into a multi-file Python library.)

fixes, improvements, and additions:

- Major improvements and fundamental changes
- Fixed "Failed to get passToken!" error by simulating the verification step through sending verification code to email/phone number...
- Fixed "KeyError: 'ssecurity'" error by simulating the captcha entry step...
- Improved login process
- Added custom encryption/decryption library, AES - no longer dependent on external libraries

### Version 1.6.1:

- improvements

### Version 1.6.2:

- Fix: error (`com.termux.api app is not installed`)

### Version 1.6.3:

- Minor improvements

### Version 1.6.4:

- Fix: error (`401 Client Error: Unauthorized for url`)
- improvements
- Add migate (github.com/offici5l/migate) for authentication

### Version 1.6.5:

- minor bug fixes

### Version 1.6.6:

- minor fixes

### Version 1.6.7:

- minor fixes
- [ migate 1.0.5: Fixes and improvements](https://github.com/offici5l/migate) 

### Version 1.6.8:

- minor fixes & improvements

### Version 1.6.9:

- improvements

### Version 1.7.0:

- Minor improvements
- [migate](https://github.com/offici5l/migate): New login methods: Browser(default), Terminal, QR code

### Version 1.7.1:

- Improved region data center detection
- improvements [migate](https://github.com/offici5l/migate)

### Version 1.7.2:

- minor fixes & improvements

### Version 1.7.3:

- minor improvements: support `python -m miunlock` when entry point is unavailable

### Version 1.7.4:

- improvements (added `pyaes` dependency)

### Version 1.7.5:

- Fix #221: error 10005 `Invalid nonce param`