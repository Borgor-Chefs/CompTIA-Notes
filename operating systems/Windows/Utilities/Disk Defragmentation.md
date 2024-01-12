Tags: [#os #windows #utility]
Program Name: `defrag.exe`

# Disk Defragmentation

This moves file fragments so that they are continous, this improves read and write times.

>Note that you cannot defrag an SSD because it doesn't use spinning magnetic platters like an HDD.

There is a graphical version in the drive properties.

This also requires elevated permissions and is executable from the command line.

```powershell
defrag [volume]
defrag C:
```
