
# File Transfer Using WinSCP

## 1. Install WinSCP

Download WinSCP from:

https://winscp.net/eng/index.php

Choose the Commander interface for a dual-panel layout.

## 2. Configure the connection

For the existing FTP server, enter:

- File protocol: FTP
- Host name: Kali Linux IP address
- Port: 21
- Username: Kali Linux username
- Password: Kali Linux account password

## 3. Connect

Click Login.

The left panel displays Windows files.
The right panel displays Linux files.

## 4. Upload a file

On the left, navigate to the source file.

On the right, open:

```text
/home/kali/ftp-upload
```

Drag the file from the left panel to the right panel.

## 5. Verify the upload

On Kali Linux:

```bash
ls -l ~/ftp-upload
```

## 6. Download a file

Drag a file from the Linux right panel to the
Windows left panel.

## Troubleshooting

If uploads fail with Permission denied, verify the
destination path, FTP write settings, and directory
permissions.
