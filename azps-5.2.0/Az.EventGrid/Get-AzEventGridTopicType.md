---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338251"
---
# Get-AzEventGridTopicType

## Sinossi
Ottiene i dettagli relativi ai tipi di argomenti supportati dalla griglia di eventi di Azure.

## SINTASSI

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrizione
Ottiene i dettagli dei tipi di argomenti supportati dalla griglia di eventi Azure.
Se viene specificato un nome tipo di argomento, vengono restituiti i dettagli relativi al tipo di argomento.
Se non si specifica un nome di tipo di argomento, vengono restituiti i dettagli su tutti i tipi di argomenti.
Se IncludeEventTypes è specificato, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.

## ESEMPI

### Esempio 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

Ottiene un elenco dei tipi di argomenti.

### Esempio 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Ottiene le informazioni sul tipo di argomento StorageAccounts.

### Esempio 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Ottiene le informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -IncludeEventTypeData
Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.

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

### -Nome
Nome tipo argomento EventGrid.

```yaml
Type: System.String
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

## OUTPUT

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo

## Note

## COLLEGAMENTI CORRELATI
