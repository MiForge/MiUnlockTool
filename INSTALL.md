<h4>

Skip [here](#android-termux) for Termux instructions

</h4>

<h3> Step 1 </h3>
<p>Install Python</p>

<details>
<summary> Windows </summary>
<br>

You can download the installer [directly](https://www.python.org/downloads/) from Python's website (don't forget to check the "Add Python to PATH" option) or via WinGet:
```
winget install python
```

On Windows you can skip straight to [Step 4](#-step-4-) (and ignore the note at the bottom), but if you're getting an ```externally managed environment``` error you will need to do steps 2 and 3 as well

</details>

<details>
<summary> macOS </summary>
<br>

You can download the installer [directly](https://www.python.org/downloads/) from Python's website or via [Homebrew](https://brew.sh/):
```
brew install --cask python
```
</details>

<details>
<summary> Ubuntu/Debian </summary>
<br>
  
```
sudo apt install python3 python3-venv
```

</details>

<details>
<summary> Fedora </summary>
<br>

```
sudo dnf install python3
```
</details>

<details>
<summary> Arch Linux </summary>
<br>

```
sudo pacman -S python
```
</details>

<h3> Step 2 </h3>
<p>Create a virual environment for Python under any name you want</p>

```
python3 -m venv anyname
```
<h3> Step 3 </h3>
<p>Source the approriate variables inside the anyname/bin/ directory with your commandline shell. If you're unsure which shell your OS uses run the following command:

```sh
echo $SHELL
```
</p>

<details>
<summary> Windows </summary>
<br>
  
```sh
# PowerShell
anyname/bin/Activate.ps1
# CMD
anyname/bin/activate.bat
```
</details>

<details>
<summary> macOS/Linux </summary>
<br>

Choose the variable file intended for your shell

```sh
# bash/zsh (Default on macOS and most Linux distributions)
source anyname/bin/activate
```

```sh
# fish
source anyname/bin/activate.fish
```

```sh
# tcsh
source anyname/bin/activate.csh
```

</details>

<h3> Step 4 </h3>

<p>Install MiUnlockTool</p>

```
pip install miunlock
```
> [!NOTE]
> These steps make **MiUnlockTool** available to your **current** shell session, step 3 will have to be redone if you ever wish to use the tool again

---

## Android (Termux)

### Install termux-app & termux-api
**(Install both apps from a single source)** <br> ex: from GitHub:

- [Termux](https://github.com/termux/termux-app/releases/latest)
- [Termux API](https://github.com/termux/termux-api/releases/latest)

### Quick Installation

```sh
curl -sS https://raw.githubusercontent.com/offici5l/MiUnlockTool/main/.install | bash
```

### Step-by-step Installation

#### Install Python3
```sh
pkg install python-pip
```

#### Install MiUnlockTool
```sh
pip install miunlock
```

> [!NOTE]
> [termux-fastboot](https://github.com/nohajc/termux-adb) is installed automatically the first time you run `miunlock`
> However, you can do this manually:
> ```sh
> curl -s https://raw.githubusercontent.com/nohajc/termux-adb/master/install.sh | bash
> ```
