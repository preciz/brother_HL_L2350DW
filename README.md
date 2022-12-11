# Linux setup of Brother ‎HL-L2350DW printer

## Use only if printer otherwide doesn't work.

Arch linux:
```bash
pacman -S ipp-usb
systemctl enable --now ipp-usb
```

Run the following command to list available printer URIs:

```bash
lpinfo -v
```

Add printer URI:

```bash
sudo lpadmin -p brother_usb_ipp -E -u allow:all -v "ipp://Brother%20HL-L2350DW%20series%20(USB)._ipp._tcp.local/" -m everywhere
```

Open [http://localhost:631/printers/brother_usb_ipp](http://localhost:631/printers/brother_usb_ipp)

Modify printer model to Generic IPP printer.

It should print fine now. 
