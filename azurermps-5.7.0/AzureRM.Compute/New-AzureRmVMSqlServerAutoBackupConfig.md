---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508352"
---
# New-AzureVMSqlServerAutoBackupConfig

## Sinossi
Crea un oggetto Configuration per il backup automatico di SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### StorageUriSqlServerAutoBackup (impostazione predefinita)
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.

## ESEMPI

### Esempio 1: creare una configurazione di backup automatica usando l'URI di archiviazione e la chiave dell'account
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Questo comando crea un oggetto di configurazione di backup automatico specificando l'URI di archiviazione e la chiave dell'account.
Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.
Il comando Archivia il risultato nella variabile $AutoBackupConfig.
Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.

### Esempio 2: creare una configurazione di backup automatica tramite il contesto di archiviazione
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Il primo comando crea un contesto di archiviazione e lo archivia nella variabile $StorageContext.
Per altre informazioni, vedere New-AzureStorageContext.

Il secondo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.
Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.

### Esempio 3: creare una configurazione di backup automatica tramite il contesto di archiviazione con crittografia e password
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Questo comando crea e archivia un oggetto di configurazione di backup automatico.
Il comando specifica il contesto di archiviazione creato in un esempio precedente.
Il comando consente la crittografia con password.
La password è stata precedentemente archiviata come stringa sicura nella variabile $CertificatePassword.
Per creare una stringa sicura, usa il cmdlet ConvertTo-SecureString.

## PARAMETRI

### -BackupScheduleType
Tipo di pianificazione del backup, manuale o automatizzato

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Database di sistema di backup

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.
Se specifichi questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.
In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Indica che questo cmdlet Abilita la crittografia.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Frequenza di backup completa di SQL Server, giornaliera o settimanale

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Finestra backup completo di SQL Server in ore

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Specifica il numero di giorni per cui mantenere un backup.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Specifica l'account di archiviazione che verrà usato per archiviare i backup.
Per ottenere un oggetto **AzureStorageContext** , usa il cmdlet New-AzureStorageContext.
L'impostazione predefinita è l'account di archiviazione associato alla macchina virtuale di SQL Server.

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Specifica la chiave di archiviazione dell'account di archiviazione BLOB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


