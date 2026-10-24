
# Troubleshooting File Transfers

## 1. Connection refused

Check whether vsftpd is running:

```bash
sudo systemctl status vsftpd
```

## 2. Login failed

Verify the Linux username and password.

## 3. Upload permission denied

Check the FTP configuration:

```bash
grep -E '^(anonymous_enable|local_enable|write_enable)=' /etc/vsftpd.conf
```

Expected settings:

```ini
anonymous_enable=NO
local_enable=YES
write_enable=YES
```

Check the destination folder:

```bash
ls -ld "$HOME" "$HOME/ftp-upload"
```

Test local write access:

```bash
touch ~/ftp-upload/test.txt
```

If successful, remove the test file:

```bash
rm ~/ftp-upload/test.txt
```

## 4. FTP connection timeout

Check the IP address, network connectivity, firewall,
and passive FTP configuration.

## 5. Verify the FTP port from Windows

Run in PowerShell:

```powershell
Test-NetConnection 192.168.1.50 -Port 21
```

Replace the example IP with the actual Kali IP.

## Security

Do not expose plain FTP to the public internet.
Use SFTP or properly configured FTPS when encryption
is required.
