
---

# Trespasser (1998) Autosplitter - Tresspasser CE

A lightweight **LiveSplit Autosplitter** for the classic 1998 title *Trespasser* when using the CE patch.
Automatically handles load detection for accurate timing.

## Version
* This script will only work when using TresCE, found here:
https://www.trescom.org/download/trespasser-2020-a-trespasser-modding-starter-kit/

## ✨ Features

* ✔️ Detects game load states
* ✔️ Prevents time from running during loads

## 📜 Autosplitter Script
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

## 📦 Installation

1. Copy the code above into Notepad, and save it as an `.asl` script.
2. Open LiveSplit → *Edit Layout* → **+** → *Control* → **Scriptable Autosplitter**.
3. Select this `.asl` file.

OR

Install the direct ASL file in Releases.

## 📝 Notes

* Compatible with *Trespasser CE* which is found here: https://www.trescom.org/download/trespasser-2020-a-trespasser-modding-starter-kit/
* Uses memory offset `0x653AF8` to track load-state byte.


---
