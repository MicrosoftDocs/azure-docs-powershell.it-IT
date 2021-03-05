---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008285"
---
# Get-AzSupportTicket

## SYNOPSIS
Ottieni ticket di supporto.

## SINTASSI

### ListParameterSet (impostazione predefinita)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## DESCRIZIONE
Ottiene l'elenco dei ticket di supporto. Se non si specifica alcun parametro, verranno recuperati tutti i ticket di supporto. È anche possibile filtrare i ticket di supporto per stato o data di creazione usando il parametro Filter. Ecco alcuni esempi di valori di filtro che è possibile specificare.

| Scenario                                                         | Filtro                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Ottenere ticket in stato di apertura                               | "Status eq 'Open'"                               |
| Ottenere i ticket in stato chiuso                             | "Status eq 'Closed'"                             |
| Ottenere i biglietti creati il 20 dicembre 2019 o dopo il 20 dicembre 2019         | "CreatedDate ge 2019-12-20"                      |
| Ottenere i biglietti creati dopo il 20 dicembre 2019               | "CreatedDate gt 2019-12-20"                      |
| Ottiene i ticket creati dopo il 20 dicembre 2019 in stato aperto | "CreatedDate gt 2019-12-20 and Status eq 'Open'" |


Questo cmdlet supporta la suddivisione in pagine tramite i parametri First e Skip.

È anche possibile recuperare un singolo ticket di supporto specificando il nome del ticket. 

## ESEMPI

### Esempio 1: Ottenere i primi 2 biglietti
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Esempio 2: Ottenere i primi 2 ticket dopo aver ignorato i primi 2
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Esempio 3: Ottenere un ticket di supporto in base al nome
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Esempio 4: Ottenere i primi 2 ticket di supporto filtrati in base allo stato
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Esempio 5: Ottenere tutti i ticket di supporto nello stato Aperto e creati dopo il 20 dicembre 2019
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

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

### -Filter
Filtro da applicare ai risultati di questo cmdlet.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome del ticket di supporto che riceve questo cmdlet.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Segnala il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.
Se il cmdlet non riesce a determinare il conteggio totale, viene visualizzato "Numero totale sconosciuto". Il numero intero ha una proprietà Accuracy che indica l'affidabilità del valore totale del conteggio.
Il valore di Precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non è stato in grado di contare gli oggetti, 1,0 indica che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 indica una stima sempre più affidabile.

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

### -Skip
Ignora il numero specificato di oggetti e ottiene gli oggetti rimanenti.
Immettere il numero di oggetti da ignorare.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Ottiene solo il numero specificato di oggetti.
Immettere il numero di oggetti da recuperare.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## NOTE

## COLLEGAMENTI CORRELATI
