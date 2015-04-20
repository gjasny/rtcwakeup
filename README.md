# rtcwakeup
RTC wakeup for systemd

# Basic usage
1. Install all files
2. Enable service with `systemctl enable rtcwakeup`
3. Write wake-up time into /var/run/wakeup
4. Poweroff system

# Usage with vdr
Repository has shutdown hook for debian based VDR installations in etc/vdr/shutdown-hooks/S01.rtcwakeup. Edit file for your requirements

1. Install all files
2. Enable service with `systemctl enable rtcwakeup`
3. Add shutdown script or hook which writes into /var/run/wakeup
4. Run Poweroff by VDR
