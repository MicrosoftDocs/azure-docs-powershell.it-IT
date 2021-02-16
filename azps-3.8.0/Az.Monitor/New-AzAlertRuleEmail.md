---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411365"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Crea un'azione di posta elettronica per una regola di avviso.

## SINTASSI

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzAlertRuleEmail** crea un'azione di posta elettronica per una regola di avviso.

## ESEMPI

### Esempio 1: Creare un'azione di posta elettronica con una regola di avviso per i proprietari dei servizi
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Questo comando crea un'azione di posta elettronica relativa a una regola di avviso da inviare ai proprietari dei servizi quando viene creata una regola di avviso.

### Esempio 2: Creare un'azione di posta elettronica con una regola di avviso per i proprietari di servizi non
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Questo comando crea un'azione di posta elettronica con una regola di avviso per gli indirizzi di posta elettronica specificati, ma non per i proprietari dei servizi.

### Esempio 3: Creare un'azione di posta elettronica con una regola di avviso per proprietari di servizi e non proprietari di servizi
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Questo comando crea un'azione di posta elettronica con una regola di avviso per l'indirizzo specificato e per i proprietari dei servizi.

## PARAMETERS

### -CustomEmail
Specifica un elenco di indirizzi di posta elettronica separati da virgola.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SendToServiceOwner
Indica che questa operazione invia un messaggio di posta elettronica ai proprietari del servizio quando la regola viene applicata.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String[]

### System.Management.Automation.SwitchParameter

## OUTPUT

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## NOTE

## COLLEGAMENTI CORRELATI


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


