# Keepass URL handlers

These let you connect to the service by double clicking in the URL column
or single click on the URL at the bottom.

## Setting up

Go to Tools > Options > Integration > URL overrides

Add or edit the overrides. For example, if you set an override for scheme
`mysch`, this will be used to handle `mysch://` URLs.

And vice versa — to use the scheme `rdp` or `winbox` you have to specify
`rdp://hostname` or `winbox://some.ip.address` as the URL of the entry.

## URL overrides

These are all for Windows systems.

### RDP

```
cmd://cmd /c "cmdkey /generic:TERMSRV/{URL:RMVSCM} /user:{USERNAME} /pass:{PASSWORD} && mstsc /v:{URL:RMVSCM} && timeout /t 5 /nobreak && cmdkey /delete:TERMSRV/{URL:RMVSCM}"
```

### VNC

You must have the Tight VNC client available. I usually just include it in the
directory with the KeePass file.

```
cmd://"tvnviewer.exe" "{URL:RMVSCM}" -password={PASSWORD}
```

### SSH

> The difference between this override and the one bundled with Keepass is
> that this also supplies the password. You might want to use separate Scheme 
> if you want to also use Keepass URLs to start password-less auth sessions.

You must have the PuTTY client available. I usually just include it in the
directory with the KeePass file.

```
cmd://putty.exe -ssh {USERNAME}@{URL:RMVSCM} -pw {PASSWORD}
```

### WinBox (Mikrotik router client)

You must have the WinBox client available. I usually just include it in the
directory with the KeePass file.

```
cmd://winbox.exe {URL:RMVSCM} {USERNAME} {PASSWORD}
```

### FTP

You must have the WinSCP client available. I usually just include it in the
directory with the KeePass file.

```
cmd://winscp.exe ftp://{USERNAME}:{PASSWORD}@{URL:RMVSCM}
```

### SFTP

You must have the WinSCP client available. I usually just include it in the
directory with the KeePass file.

```
cmd://winscp.exe sftp://{USERNAME}:{PASSWORD}@{URL:RMVSCM}
```

### SCP

You must have the WinSCP client available. I usually just include it in the
directory with the KeePass file.

```
cmd://winscp.exe scp://{USERNAME}:{PASSWORD}@{URL:RMVSCM}
```
