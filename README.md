# PIvot

A RPi OS variant for self-hosters.

## Connecting to PIvot

Default connection details come from [`pivot-gen/config`](https://github.com/cylin577/pivot-gen/blob/master/config):

- Hostname set to `pivot`.
- SSH enabled by default.
- Default username: `pivot`
- Default password: `tovip`
- `sudo` does not require password for default user.

You can connect over SSH with:

```bash
ssh pivot@pivot.local
```

If mDNS not available on your network, use device IP address instead:

```bash
ssh pivot@<device-ip>
```

On first boot, PIvot also exposes setup screen in browser on port `7681`:

- `http://pivot:7681`
- `http://pivot.local:7681`
- `http://<device-ip>:7681`

Change default password after first login if machine will be reachable by other devices.

## Note

I recommnend using [Tailscale](login.tailscale.com/admin) to reach your device outside of your LAN