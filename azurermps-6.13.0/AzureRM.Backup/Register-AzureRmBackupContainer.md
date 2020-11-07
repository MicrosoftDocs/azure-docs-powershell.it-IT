---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 3431650296c29f06131f946910d1cbc3dc6e6bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685784"
---
# Register-AzureRmBackupContainer

## Sinossi
Registra il contenitore con un caveau di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Register-AzureRmBackupContainer** registra il contenitore con un Vault di backup di Azure.
Per configurare il backup con Azure Backup, prima di tutto registrare il server o la macchina virtuale con un caveau di backup.
Questo cmdlet registra una macchina virtuale dell'infrastruttura come servizio (IaaS) con il Vault specificato.
L'operazione Register associa la macchina virtuale Azure alla volta di backup e tiene traccia della macchina virtuale tramite il ciclo di vita del backup.

## ESEMPI

### Esempio 1: registrare una macchina virtuale in un caveau di backup
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.
Il comando Archivia il Vault nella variabile $Vault.
Il secondo comando registra la macchina virtuale denominata Contoso03Vm con il Vault in $Vault.
La macchina virtuale appartiene al servizio denominato ContosoService27.

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

### -Nome
Specifica il nome della macchina virtuale registrata da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse per la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifica il nome del servizio della macchina virtuale che questo cmdlet registra.
In genere, il nome di un servizio cloud ha un suffisso. cloudapp.net.
Non includere il suffisso quando specifichi questo parametro.
Per ottenere informazioni su una macchina virtuale, usare il cmdlet Get-AzureRMVM.
Il nome del servizio è la proprietà **DeploymentName** dell'oggetto macchina virtuale.

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vault
Specifica il Vault di backup a cui questo cmdlet registra la macchina virtuale.
Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault
Parameters: Vault (ByValue)

## OUTPUT

### Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


