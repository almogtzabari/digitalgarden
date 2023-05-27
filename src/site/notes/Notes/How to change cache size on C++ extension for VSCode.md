---
{"dg-publish":true,"dg-path":"How to change cache size on C++ extension for VSCode.md","permalink":"/how-to-change-cache-size-on-c-extension-for-vs-code/","tags":[null]}
---



# How to change [[Notes/Cache\|cache]] size on [[Notes/C++\|C++]] extension for [[Notes/VSCode\|VSCode]]
Simply paste the following in `settings.json` (probably better to put it in the project settings and not the user):
```json
"C_Cpp.intelliSenseCachePath": "path/to/cache/dir/vscode-cpptools",
"C_Cpp.intelliSenseCacheSize": 32767
```
