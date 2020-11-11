# HM-WebUI-LED16-Mod
WebUI modification to display the LED states of the HM-OU-LED16

Login via SSH and execute the following commands (note: every point is one line with no line breaks):<br/>
- `mount -o remount,rw /`<br/>
- `cp /www/rega/esp/controls/button.fn /www/rega/esp/controls/button.fn.bak`
- `cd /www/rega/esp/controls/ ; wget --no-check-certificate -q -O - https://raw.githubusercontent.com/jp112sdl/HM-WebUI-LED16-Mod/master/patch/button.fn.patch | patch button.fn`<br/>
- `mount -o remount,ro /`<br/>
- running RaspberryMatic:<br/>
  - `monit restart ReGaHss`<br/>
- running CCU3 FW:<br/>
  - `/etc/init.d/S70ReGaHss restart`<br/>
  
**At least: clear browser cache!**
<br/>
**Caution: This mod must be applied after every ccu/raspberrymatic firmware update.**


![WebUI](Images/WebUI_Display.png)
