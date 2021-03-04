---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 4b34731c0cd0c2d49a7c26112d370d8d4a2f948e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957277"
---
# Get-AzEventHubConsumerGroup

## SYNOPSIS
Recupera i dettagli di un gruppo consumer specificato di hub eventi o ottiene un elenco di gruppi consumer in un hub eventi.

## SINTASSI

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il Get-AzEventHubConsumerGroup cmdlet ottiene i dettagli di un determinato gruppo di utenti consumer Hub eventi oppure un elenco di gruppi consumer in un determinato Hub eventi.
Se viene fornito il nome di un gruppo consumer, vengono restituiti i dettagli di un singolo gruppo consumer.
Se il nome di un gruppo consumer non viene fornito, viene restituito un elenco di gruppi consumer nell'hub eventi specificato.

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

Ottiene il gruppo consumer \` MyConsumerGroupName nell'hub eventi MyEventHubName, che si trova nello spazio dei nomi MyResourceName con il gruppo \` \` di risorse \` \` \` \` MyResourceGroupName. \`

### Esempio 2
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Ottiene un elenco di gruppi consumer nell'hub eventi MyEventHubName, che si trova nello spazio dei nomi \` \` MyResourceName con il gruppo di risorse \` \` \` MyResourceGroupName. \`

## PARAMETERS

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -EventHub
Nome EventHub

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Determinare il numero massimo di Gruppi Consumer da restituire.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
ConsumerGroup Name

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Nome spazio dei nomi

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome gruppo di risorse

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes

## NOTE

## COLLEGAMENTI CORRELATI
