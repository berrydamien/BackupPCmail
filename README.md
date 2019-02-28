# BackupPC_mail

## Usage

Simple script utilisé pour généger un mail de bilan des sauvegardes en HTML avec le tableau récapitulatif des machines.

Pour BackupPC traduction en français

## Install / config

Placer le script "BackupPC_mail" avec les autres script de BackupPC : /usr/share/backuppc/bin/BackupPC_mail

Modifier le script "/usr/share/backuppc/bin/BackupPC_nightly" ligne 232 pour l'exécution de ce script

```
if ( $opts{m} ) {
	    print("log BackupPC_nightly now running BackupPC_sendEmail\n");
	    system("$BinDir/BackupPC_sendEmail");
	    # >> RUN BackupPC_mail
	    print("log BackupPC_nightly now running BackupPC_mail\n");
	    system("$BinDir/BackupPC_mail");
	    doBackupInfoUpdate();
	}
```

