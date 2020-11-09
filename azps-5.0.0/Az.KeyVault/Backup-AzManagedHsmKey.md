---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296874"
---
# Backup-AzManagedHsmKey

## Sinossi
Eseguire il backup di una chiave in un HSM gestito.

## SINTASSI

### ByKeyName (impostazione predefinita)
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByKey
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **backup-AzManagedHsmKey** salva una chiave specificata in un HSM gestito tramite il download e l'archiviazione in un file.
Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.
Dato che il contenuto scaricato è crittografato, non può essere usato all'esterno dell'HSM gestito da Azure.
È possibile ripristinare una chiave di backup in qualsiasi HSM gestito nell'abbonamento a cui è stato eseguito il backup.
I motivi tipici per usare questo cmdlet sono i seguenti: 
- Si vuole ottenere una copia della chiave a garanzia, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave nell'HSM gestito.
 
- È stata creata una chiave usando l'HSM gestito e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.
Usa il cmdlet **backup-AzManagedHsmKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzManagedHsmKey e specifica un HSM gestito nella seconda area geografica.

## ESEMPI

### Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

Questo comando Recupera la chiave denominata TestKey dall'HSM gestito denominato testmhsm e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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
Sovrascrivere il file assegnato se esiste

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
Nome HSM. Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Bundle chiave per eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome chiave.
Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFile
File di output.
File di output in cui archiviare il BLOB della chiave di backup.
Se non è presente, viene scelto un nome file predefinito.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI

[Add-AzManagedHsmKey](./Add-AzManagedHsmKey.md)

[Get-AzManagedHsmKey](./Get-AzManagedHsmKey.md)

[Remove-AzManagedHsmKey](./Remove-AzManagedHsmKey.md)

[Undo-AzManagedHsmKeyRemoval](./Undo-AzManagedHsmKeyRemoval.md)

[Update-AzManagedHsmKey](./Update-AzManagedHsmKey.md)

[Ripristinare-AzManagedHsmKey](./Restore-AzManagedHsmKey.md)