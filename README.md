# XcodeFix
Commands to fix multiple instances of same OS showing in Xcode platforms tab (for own future reference). Probably simpler ways to do it but this worked first

1. download latest runtime at https://developer.apple.com/download/all/
   
3. 
   ```zsh
   xcrun simctl runtime add "{path to dmg}"
   ```
4. 
   ```zsh
   xcrun simctl runtime list
   ```
   and identify latest/desireable runtime, note name
5.
   ```zsh
   xcrun simctl runtime match set {os} {runtime name}
   ```
   eg.
   ```zsh
   xcrun simctl runtime match set iphoneos17.0 21A342
   ```


Done! can verify with
```zsh
xcrun simctl runtime match list
```
