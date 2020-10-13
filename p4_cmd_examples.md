# Frequently used Perforce commands

## [Force the sync](https://www.perforce.com/manuals/v15.1/cmdref/p4_sync.html)
```
call p4 -c %workspace_name% sync -f
```
## [Edit and commit](https://www.perforce.com/manuals/v15.1/cmdref/p4_edit.html)
```
call p4 -c %workspace_name% edit //depot_name/stream_name/path_to_file
call p4 -c %workspace_name% submit -d "Submit comment"
```
## [Get the file without workspace creating](https://www.perforce.com/manuals/v15.1/cmdref/p4_print.html)
```
call p4 print -q -o common.ps1 //depot_name/stream_name/path_to_file
```
## [Edit the stream name in the workspace](https://www.perforce.com/manuals/v15.1/cmdref/p4_client.html)
```
call p4 client -f -s -S %new_stream_path% %workspace_name%
```
## [Display the workspace info](https://www.perforce.com/manuals/v15.1/cmdref/p4_client.html)
```
call p4 client -o %workspace_name%
```
## [Display the stream name](https://www.perforce.com/manuals/v15.1/cmdref/p4_stream.html)
```
call p4 stream -o %stream_name%
```
