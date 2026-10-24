
# FTP Server Setup on Kali Linux

## 1. Install vsftpd

```bash
sudo apt update
sudo apt install vsftpd
```

## 2. Start the service

```bash
sudo systemctl enable --now vsftpd
```

Verify:

```bash
sudo systemctl status vsftpd
```

## 3. Find the Linux IP address

```bash
hostname -I
```

Use the appropriate address for the shared network.

## 4. Configure FTP

Open the configuration file:

```bash
sudo nano /etc/vsftpd.conf
```

Ensure these settings are present and uncommented:

```ini
anonymous_enable=NO
local_enable=YES
write_enable=YES
```

Save the file.

## 5. Restart the service

```bash
sudo systemctl restart vsftpd
```

Verify the upload setting:

```bash
grep '^write_enable=' /etc/vsftpd.conf
```

Expected output:

```text
write_enable=YES
```

## 6. Create an upload directory

```bash
mkdir -p ~/ftp-upload
```

Check permissions:

```bash
ls -ld ~/ftp-upload
```

## Security

Use FTP only on trusted networks. Standard FTP does not
encrypt passwords or transferred data.

For secure transfers, consider SFTP over SSH.
