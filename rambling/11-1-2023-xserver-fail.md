1: [make your life harder](https://github.com/sickcodes/Docker-OSX#id-like-to-run-docker-osx-on-windows)<br>
2: make your life even harder (use https://github.com/sickcodes/Docker-OSX/discussions/458 because i use ubuntu 22.x and windows 11)<br>
3: fail miserably?? xhost + -> `Authorization required, but no authorization protocol specified`<br>
(unable to open display, even sudo didnt work)<br>
4: [google](https://www.google.com/search?q=how+to+fix+Authorization+required%252C+but+no+authorization+protocol+specified+vcxsrv) and find that a lot of people had a similar issue: https://github.com/microsoft/WSL/issues/4820<br>
(however they werent using xhost)<br>
4.5: follow this link: https://github.com/microsoft/WSL/issues/4793#issuecomment-588321333 (idk if it works or not)<br>
5: try multiple solutions, the best one was as follows:<br>
```
use the following commands:
export DISPLAY=172.17.192.1:0.0
export LIBGL_ALWAYS_INDIRECT=1

now use:
xhost +
```
6: open vcxsrv (i have it pinned in my taskbar because im a freak)<br>
oh yeah also whenever you get "failed to establish listening ports" just wait and open it again

4832908: whoops i broke it<br>
4832908: ok its fine now
