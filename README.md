# Raspberrypi 4 - 2k Display (Blank Screen FIX)
If you have connected your Raspberry pi 4 with a 2K Monitor and don't see anuthing on screen(Blank) but if you connect it with any other monitor and it works for any lower resolution monitor. I got you covered.

#### Just add the below Display settings to the config.txt file in the boot folder

```
# DISPLAY FOR 2K (2560*1440)
disable_overscan=1
hdmi_group=2
hdmi_mode=87
framebuffer_depth=24
gpu_mem=192
framebuffer_ignore_alpha=1
start_x=1
hdmi_ignore_edid=0xa5000080
hdmi_cvt 2560 1440 50 3 0 0 1
hdmi_pixel_freq_limit=300000000
hvs_priority=0x32ff
max_framebuffer_width=2560
max_framebuffer_height=1440
framebuffer_width=2560
framebuffer_height=1440
config_hdmi_boost=4
hdmi_force_hotplug=1
```

**Note**: I would recommened to backup the config.txt file before making any changes. Also you can just add comment(#) on lines which aren't required. 
