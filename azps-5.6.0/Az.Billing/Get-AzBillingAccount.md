---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959789"
---
# Get-AzBillingAccount

## SYNOPSIS
Ottenere account di fatturazione.

## SINTASSI

### Elenco (impostazione predefinita)
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Single
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzBillingAccount** ottiene gli account di fatturazione a cui l'utente ha accesso. 

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzBillingAccount
```

Ottieni tutti gli account di fatturazione a cui l'utente ha accesso.

### Esempio 2
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

Ottenere l'account di fatturazione con il nome specificato.

### Esempio 3
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi l'indirizzo nel risultato.

### Esempio 4
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi i profili di fatturazione nel risultato.

### Esempio 5
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

Ottenere tutti gli account di fatturazione a cui l'utente ha accesso e includere i profili di fatturazione e le sezioni delle fatture al di sotto di essi nei risultati.

### Esempio 6
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

Ottenere l'account di fatturazione con il nome specificato e includere l'indirizzo, i profili di fatturazione e le sezioni delle fatture al di sotto di essi nel risultato.

## PARAMETERS

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

### -IncludeAddress
Includere l'indirizzo dell'account di fatturazione.

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

### -ExpandBillingProfile
Includere i profili di fatturazione nell'account di fatturazione.

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

### -ExpandInvoiceSection
Includere i profili di fatturazione nelle sezioni account di fatturazione e fatture.

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

### -Name
Nome di un account di fatturazione specifico.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListEntitiesToCreateSubscription
Elenca le entità di fatturazione sotto l'account di fatturazione che possono essere usate come input per creare una sottoscrizione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Billing.Models.PSBillingAccount

## NOTE

## COLLEGAMENTI CORRELATI
