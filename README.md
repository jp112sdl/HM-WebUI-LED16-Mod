# HM-WebUI-LED16-Mod
WebUI modification to display the LED states of the HM-OU-LED16

Login via SSH and execute the following commands (note: every point is one line with no line breaks):<br/>
- `mount -o remount,rw /`<br/>
- `cd /www/rega/esp/controls/ ; wget --no-check-certificate -q -O - https://raw.githubusercontent.com/jp112sdl/HM-WebUI-CC-Mod/master/patch/buttons.fn.patch | patch buttons.fn`<br/>
- `mount -o remount,ro /`<br/>
- RaspberryMatic:<br/>
 - `monit restart ReGaHss`<br/>
- CCU3 FW:<br/>
 - `/etc/init.d/S70ReGaHss restart`<br/>
  
**At least: clear browser cache!**
<br/>
**Caution: This mod must be applied after every ccu/raspberrymatic firmware update.**


![WebUI](Images/WebUI_Display.png)
