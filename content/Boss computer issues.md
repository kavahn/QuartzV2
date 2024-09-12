# 1.  mouse disconnecting issue
- #### Leading theory
	- there probably was some kind of windows power plan miss management (as when the computer not shutting down fully), so the usb power saving feature is probably not working correctly (its the feature where after a while it disables the usb and shouldn't be on by default)
	- ###### fix
		- easiest would be just using a different power plan, so we should just get the one I'm using for my computer and the other desktop you have in the store
		- ###### in admin cmd run `powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61`
- #### 2nd theory
	- batteries might be low/dead so it could be shutting down and only waking when the dongle sends the wake command through restarting the system

# 2. computer not sleeping only hibernating
- #### leading theory
	- much like the mouse disconnecting it most likely is the power plan
	- ###### fix 
		- same as the mouse fix 
- #### 2nd theory
	- i am almost 100% it is the power plan

# 3. strange advanced startup behavior
- ### this probably will not affect you but this still should be investigated
- #### leading theory
	- there was some oddities when transferring the install, so the registries might be messed up
	- ###### fix
		- ok this one is a bit more complicated, this is still pretty straight forward we are just going to use windows built in verifier and rectifier 
		- ###### in an admin cmd run `DISM.exe /Online /Cleanup-image /Restorehealth` then `sfc /scannow` 
			- this should fix it, but we will test everything :) 