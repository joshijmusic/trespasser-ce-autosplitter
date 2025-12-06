
---

# Jurassic Park Trespasser (1998) Autosplitter - Trespasser CE

A lightweight **LiveSplit Autosplitter** for the classic 1998 title *Trespasser* when using the CE patch.
Automatically handles load detection for accurate timing.

## Version
* This script will only work when using TresCE, found [here](https://www.trescom.org/download/trespasser-2020-a-trespasser-modding-starter-kit/)

## Releases
[Releases Page](https://github.com/joshijmusic/trespasser-ce-autosplitter/releases)

## ✨ Features

* ✔️ Detects game load states
* ✔️ Pauses timer from running during loads & pauses.
* ❌ Does not automatically change level sections. This will come in 0.2.

## 📦 Installation

1. Install [LiveSplit](https://livesplit.org/)
2. Install the direct ASL file in [Releases.](https://github.com/joshijmusic/trespasser-ce-autosplitter/releases)
3. Open LiveSplit as Administrator → *Edit Layout* → **+** → *Control* → **Scriptable Autosplitter**.
4. Select the installed `.asl` file.
5. Right click your LiveSplit, Compare Against, Game Time.

* OR

1. Install [LiveSplit](https://livesplit.org/)
2. Copy the code below into Notepad, and save it as an `.asl` script.
3. Open LiveSplit as Administrator → *Edit Layout* → **+** → *Control* → **Scriptable Autosplitter**.
4. Select this `.asl` file.
5. Right click your LiveSplit, Compare Against, Game Time.

## 📜 Manual Autosplitter Script
(click copy in the top right, do not select and copy.)
```csharp
state("TresCE") {

    // Change bool to byte
    byte is_Loading_Byte : "TresCE.exe", 0x653AF8;
}

isLoading {

    // Check if the byte value is 1 (True/Paused)
    return current.is_Loading_Byte == 1;
}

update {}
```



## 📝 Notes

* Run LiveSplit as administrator. Accessing RAM usually requires this permission.
* Compatible with *Trespasser CE* which is found [here](https://www.trescom.org/download/trespasser-2020-a-trespasser-modding-starter-kit/)
* Uses memory offset `0x653AF8` to track load-state byte.


---
