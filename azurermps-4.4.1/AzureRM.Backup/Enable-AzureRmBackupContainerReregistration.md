---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 1c89db6267fffeb73820150d1c73c3225f45cde2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510767"
---
# Enable-AzureRmBackupContainerReregistration

## Sinossi
Registra nuovamente un server per la connessione a un caveau di backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Enable-AzureRmBackupContainerReregistration** registra nuovamente un server per la connessione a un Vault di backup di Azure e continua la catena del punto di ripristino del backup.

Se si distrugge un server, tutti i punti di backup del cloud rimarranno nell'archivio di backup.
Se si crea un server sostitutivo e lo si assegna allo stesso nome di dominio completo, è possibile riconnettere il server allo stesso Vault.
Questo cmdlet consente di eseguire il backup per creare backup e aggiungere nuovi punti di backup al set esistente.
Il nuovo server continua nella catena di backup.

## ESEMPI

## PARAMETRI

### -Contenitore
Specifica il contenitore di cui questo cmdlet viene riregistrato.
Per ottenere un **AzureRmBackupContainer** , usare il cmdlet Get-AzureRmBackupContainer.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### AzureBackupContainer

## OUTPUT

### Nessuno

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Registro-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


