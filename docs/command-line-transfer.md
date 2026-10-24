
# Command-Line File Transfer

## Option A: WinSCP.com

WinSCP provides a command-line interface on Windows.

Example executable path:

```text
C:\Program Files (x86)\WinSCP\WinSCP.com
```

Launch it from PowerShell:

```powershell
& "C:\Program Files (x86)\WinSCP\WinSCP.com"
```

Connect to Kali:

```text
open ftp://kali@192.168.1.50/
```

Replace the example IP with the actual Kali IP.

Upload a file:

```text
put "C:\Users\YourName\Downloads\test.txt" /home/kali/ftp-upload/
```

Exit:

```text
exit
```

## Option B: SFTP

SFTP uses SSH and encrypts the connection.

On Kali Linux, install and start SSH if necessary:

```bash
sudo apt install openssh-server
sudo systemctl enable --now ssh
```

From Windows PowerShell:

```powershell
sftp kali@192.168.1.50
```

Upload a file at the sftp prompt:

```text
put "C:/Users/YourName/Downloads/test.txt" /home/kali/ftp-upload/test.txt
```

Exit:

```text
exit
```

Verify the file on Kali:

```bash
ls -l ~/ftp-upload
```

Verify the SSH host-key fingerprint before accepting
an unfamiliar server.

Never commit passwords, private keys, or real credentials.
