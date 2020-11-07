---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 6021e9c4c3be3ac4eb2721684b9f94463e1b69af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688412"
---
# Backup-AzureKeyVaultSecret

## Sinossi
Eseguire il backup di un segreto in un caveau chiave.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### BySecretName (impostazione predefinita)
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **backup-AzureKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un caveau chiave, scaricarlo e archiviarlo in un file.
Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.
Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.
È possibile ripristinare un segreto di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.
I motivi tipici per usare questo cmdlet sono i seguenti:
- Si vuole depositare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel caveau della chiave.
- È stato aggiunto un segreto a un Vault chiave e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita. Usa il cmdlet Backup-AzureKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usa il cmdlet Restore-AzureKeyVaultSecret e specifica un Vault chiave nella seconda area. Tieni presente che le aree geografiche devono appartenere alla stessa geografia.

## ESEMPI

### Esempio 1: eseguire il backup di un segreto con un nome file generato automaticamente
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

Questo comando Recupera il segreto di nome segreto dal caveau della chiave denominato MyKeyVault e salva una copia di backup di tale segreto in un file denominato automaticamente e visualizza il nome del file.

### Esempio 2: eseguire il backup di un segreto in un nome file specificato, sovrascrivendo il file esistente senza richiedere conferma
```powershell
PS C:\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Questo comando Recupera il segreto di nome segreto dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale segreto in un file denominato backup. blob.

### Esempio 3: eseguire il backup di un segreto recuperato in precedenza in un nome file specificato
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Questo comando usa il nome e il nome del Vault dell'oggetto $secret per recuperare il segreto e salva il backup in un file denominato backup. blob.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Richiede la conferma prima di sovrascrivere il file di output, se esistente.

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
Segreto di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.

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

### -Nome
Specifica il nome del segreto a cui eseguire il backup.

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
Se non specifichi questo parametro, questo cmdlet genera un nome file.
Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.

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

### -VAULTNAME
Specifica il nome del Vault chiave che contiene il segreto di cui eseguire il backup.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

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
Mostra cosa succede se il cmdlet viene eseguito.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem
Parametri: InputObject (ByValue)

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Remove-AzureKeyVaultSecret](./Remove-AzureKeyVaultSecret.md)

[Ripristinare-AzureKeyVaultSecret](./Restore-AzureKeyVaultSecret.md)

