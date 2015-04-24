# rtcwakeup
RTC wakeup for systemd

# Basic usage
1. Install all files
2. Enable service with `systemctl enable rtcwakeup`
3. Write wake-up time into /var/run/wakeup
4. Poweroff system

# Usage with VDR + Debian
Repository has shutdown hook for debian based VDR installations in etc/vdr/shutdown-hooks/S01.rtcwakeup. Edit file for your requirements. Add sudo command into WAKEUPCMD in /etc/defaul/rtcwakeup if required. Remember to configure sudo not to ask password.

1. Install all files
2. Enable service with `systemctl enable rtcwakeup`
3. Add shutdown script or hook which writes into /var/run/wakeup
4. Run Poweroff by VDR

# Usage with VDR
etc/vdr/shutdown-hooks/S01.rtcwakeup requires used directly as VDR's shutdown script(-s argument). Script might work if `exit 0`s are replaced with `$SHUTDOWNCMD`(Not tested).
