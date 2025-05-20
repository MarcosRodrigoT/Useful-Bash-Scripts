# nvidia_reboot

This script simply automates the typical steps after updating Nvidia/CUDA drivers.

## Getting started

To run this command, simply:

```bash
nvidia_reboot
```

This will stop the typical processes making use of the Nvidia GPU and reload the Nvidia kernel modules.

>[!Note]
>Running this script disables `gdm` by default. If you want to enable it again run:
>
>```bash
>sudo systemctl start gdm
>```
>Depending on your OS configuration, it is possible that even after restarting `gdm`, this won't make use of the Nvidia driver until reboot.
