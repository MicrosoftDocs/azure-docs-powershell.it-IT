---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: a23fc0f41bd50a956c68cb52fa341f1bd8119372
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861513"
---
# Get-AzEventHub

## Sinossi
Ottiene i dettagli di un singolo hub di eventi o restituisce un elenco di hub eventi.

## SINTASSI

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet Get-AzEventHub restituisce i dettagli di un hub eventi o un elenco di tutti gli hub eventi nello spazio dei nomi corrente.
Se viene fornito il nome dell'hub eventi, vengono restituiti i dettagli di un singolo hub eventi.
Se non viene specificato un nome Hub eventi, viene restituito un elenco di tutti gli hub eventi nello spazio dei nomi specificato.

## ESEMPI

### Esempio 1-EventHub specificato
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Restituisce i dettagli dell'hub dell'evento \` MyEventHubName \` .

### Esempio 2-elenco di EventHub nello spazio dei nomi specificato
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

Restituisce un elenco di hub eventi nello spazio dei nomi MyNamespace \` \` .

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

### -MaxCount
Determinare il numero massimo di EventHubs da restituire.

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

### -Nome
Nome EventHub

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Spazio dei nomi
Nome dello spazio dei nomi

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
Nome gruppo risorse

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

## OUTPUT

### Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes

## Note

## COLLEGAMENTI CORRELATI
