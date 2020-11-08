---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201189"
---
# Get-AzManagedHsm

## Sinossi
Ottenere i HSM gestiti.

## SINTASSI

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzManagedHsm** ottiene informazioni sulle HSM gestite in un abbonamento. È possibile visualizzare tutte le istanze di HSM gestite in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un determinato HSM gestito.
Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando ricevi un singolo HSM gestito, dovresti farlo per migliorare le prestazioni.

## ESEMPI

### Esempio 1: ottenere tutti i HSM gestiti nell'abbonamento corrente
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Questo comando ottiene tutti i HSM gestiti nell'abbonamento corrente.

### Esempio 2: ottenere un HSM gestito specifico
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Questo comando ottiene l'HSM gestito denominato myhsm nell'abbonamento corrente.

### Esempio 3: ottenere HSM gestiti in un gruppo di risorse
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Questo comando ottiene tutti i HSM gestiti nel gruppo di risorse denominato myrg1.

### Esempio 4: ottenere HSM gestiti tramite filtro
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Questo comando ottiene tutti i HSM gestiti nell'abbonamento che iniziano con "myhsm".

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

### -Nome
Nome HSM. Cmdlet costruisce l'FQDN di un HSM in base al nome e all'ambiente attualmente selezionato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse associato all'HSM gestito in cui viene eseguita la query.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Specifica la chiave e il valore facoltativo del tag specificato per filtrare l'elenco di HSM gestiti.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. Collections. Hashtable

## OUTPUT

### Microsoft. Azure. Commands. Vault. Models. PSManagedHsm

### Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem

## Note

## COLLEGAMENTI CORRELATI

[New-AzManagedHsm](./New-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Update-AzManagedHsm](./Update-AzManagedHsm.md)