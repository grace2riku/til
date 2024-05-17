# PowerShell
便利なPowerShellスクリプトなどをメモしておく

## 240517 ディスク容量を消費しているファイルを一覧表示する

* 1Gバイト以上のファイルを表紙する
  * 検索ファイルパスは調整のこと

```
Get-ChildItem -Path C:\Users -Recurse -File | Where-Object { $_.Length -gt 1GB } | Select-Object FullName, @{Name="Length(GB)";Expression={[math]::round($_.Length / 1GB, 3)}}
```

* 500Mバイト以上のファイルを表紙する
```
Get-ChildItem -Path C:\Users\koji.abe\Documents\work -Recurse -File | Where-Object { $_.Length -gt 500MB } | Select-Object FullName, @{Name="Length(GB)";Expression={[math]::round($_.Length / 1GB, 3)}}
```
