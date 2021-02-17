---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192398"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Backup di un segreto in un vault delle chiavi.

## SINTASSI

### BySecretName (impostazione predefinita)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Backup-AzKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un vault delle chiavi scaricarlo e archiviarlo in un file.
Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.
Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno del Vault delle chiavi di Azure.
È possibile ripristinare un segreto di cui è stato eseguito il backup in qualsiasi vault della chiave nell'abbonamento da cui è stato eseguito il backup.
I motivi tipici per usare questo cmdlet sono:
- Si vuole eliminare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel vault delle chiavi.
- È stato aggiunto un segreto a un vault delle chiavi e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare da tutte le istanze dell'applicazione distribuita. Usare il cmdlet Backup-AzKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usare il cmdlet Restore-AzKeyVaultSecret e specificare un vault delle chiavi nella seconda area geografica. Si noti che le aree geografiche devono appartenere alla stessa area geografica.

## ESEMPI

### Esempio 1: Eseguire il backup di un segreto con un nome file generato automaticamente
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Questo comando recupera il segreto denominato MySecret dal vault della chiave denominato MyKeyVault e salva una copia di backup del segreto in un file denominato automaticamente e visualizza il nome del file.

### Esempio 2: Eseguire il backup di un segreto con un nome file specificato sovrascrivendo il file esistente senza chiedere conferma
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Questo comando recupera il segreto denominato MySecret dalla chiave vaultd MyKeyVault e salva una copia di backup del segreto in un file denominato Backup.blob.

### Esempio 3: Eseguire il backup di un segreto recuperato in precedenza con un nome file specificato
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Questo comando usa il nome $secret vault e il nome dell'oggetto per recuperare il segreto e salva il backup in un file denominato Backup.BLOB.

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Chiede conferma prima di sovrascrivere il file di output, se presente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Segreto di cui eseguire il backup, pipelined in seguito all'output di una chiamata di recupero.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifica il nome del segreto di cui eseguire il backup.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
Specifica il file di output in cui è archiviato il BLOB di backup.
Se non si specifica questo parametro, questo cmdlet genera automaticamente un nome file.
Se si specifica il nome di un file di output esistente, l'operazione non verrà completata e verrà restituito un messaggio di errore che indica che il file di backup esiste già.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Specifica il nome del vault della chiave che contiene il segreto di cui eseguire il backup.

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem

## OUTPUT

### System.String

## NOTE

## COLLEGAMENTI CORRELATI

[Set-AzKeyVaultSecret](./Set-AzKeyVaultSecret.md)

[Get-AzKeyVaultSecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-AzKeyVaultSecret](./Restore-AzKeyVaultSecret.md)

