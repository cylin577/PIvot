
# PIvot

A Raspberry Pi OS variant for self-hosters.
##  Getting Started

Default connection details are managed via [`pivot-gen/config`](https://github.com/cylin577/pivot-gen/blob/master/config):

*   **Hostname:** `pivot`
*   **Username:** `pivot`
*   **Password:** `tovip`
*   **SSH:** Enabled by default
*   **Sudo:** Passwordless access for the default user

---

##  Connecting to PIvot

### Via SSH
Connect from your terminal using the local hostname:
```bash
ssh pivot@pivot.local
```

*If mDNS is not supported on your network, use the device IP address: `ssh pivot@<device-ip>`*

### Via Web Browser
On first boot, a setup screen is exposed on port **7681**:
*   ```http://pivot.local:7681```
*   ```http://<device-ip>:7681```

---

##  Important Notes

*   **Wi-Fi Setup:** If you do not use an Ethernet cable on the first boot, you must connect a keyboard and screen to the Pi to configure your wireless network manually.
*   **Security:** If you intend to expose this device to the internet, immediately update the default password by running the `passwd` command or you could get all your data stolen if someone has access to your network
*   **Remote Access:** For secure access outside your local network (LAN), it is highly recommended to use [Tailscale](https://login.tailscale.com/admin).