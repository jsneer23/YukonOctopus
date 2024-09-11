# YukonOctopus

## Getting Started with MicroPython and Yukon libraries in VS Code

### Step 1: Acquire libraries

Option A: Start your own repository from scratch

```console
git init
git submodule add https://github.com/raspberrypi/pico-sdk/
git submodule add https://github.com/pimoroni/yukon/
```

Option B: Clone this repository

```console
git clone https://github.com/jsneer23/YukonOctopus/
git submodule update --init --recursive
```

### Step 2: Set path to libraries

To setup the pico-sdk library use

```console
export PICO_SDK_PATH=/home/path/to/pico-sdk
```

To setup the pimoroni yukon library add "./yukon/lib" to "python.analysis.extraPaths" in settings.json.

### Step 3: Install VS Code extensions

```console
code --install-extension ms-python.python
code --install-extension visualstudioexptteam.vscodeintellicode
code --install-extension ms-python.vscode-pylance
code --install-extension paulober.pico-w-go
```

### Step 4: Connect to shell on the yukon

To access the python shell on the rp2040 chip first install rshell

```console
pip install rshell
```

Then run

```console
rshell --buffer-size=512 -p /dev/ttyACM0
```
