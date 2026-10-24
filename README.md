
# Windows 11 to Kali Linux File Transfer

A hands-on guide to transferring files from Windows 11 to Kali Linux using FTP, WinSCP, and command-line tools.

## Project Goals

- Configure an FTP server on Kali Linux.
- Connect Windows 11 to Kali using WinSCP.
- Upload and download files.
- Troubleshoot FTP permission errors.
- Transfer files from the command line.
- Understand FTP versus SFTP security.

## Environment

- Client: Windows 11
- Server: Kali Linux
- FTP server: vsftpd
- GUI client: WinSCP
- CLI client: WinSCP.com or OpenSSH SFTP

## Project Documentation

1. [FTP Server Setup](docs/ftp-server-setup.md)
2. [WinSCP File Transfer](docs/winscp-transfer.md)
3. [Command-Line Transfer](docs/command-line-transfer.md)
4. [Troubleshooting](docs/troubleshooting.md)

## Security Notes

Standard FTP does not encrypt credentials or transferred files.
Use it only on a trusted network.

Prefer SFTP over SSH when encrypted transfers are required.

## Disclaimer

This guide is intended for authorized systems and networks.
