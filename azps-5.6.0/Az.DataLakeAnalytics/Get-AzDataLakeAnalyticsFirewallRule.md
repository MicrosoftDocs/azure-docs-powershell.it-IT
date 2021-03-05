---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: e95d29b5a91f8df257649693bdd9d4029ca3d166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998379"
---
# Get-AzDataLakeAnalyticsFirewallRule

## SYNOPSIS
Recupera una regola del firewall o un elenco di regole del firewall da un account Data Lake Analytics.

## SINTASSI

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzDataLakeAnalyticsFirewallRule** recupera una regola del firewall o un elenco di regole del firewall da un account Azure Data Lake Analytics.

## ESEMPI

### Esempio 1: Ottenere una regola del firewall
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

Questo comando recupera la regola del firewall denominata "regola del firewall" dall'account "ContosoAdlAcct"

### Esempio 2: Elencare tutte le regole del firewall
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

Questo comando recupera tutte le regole del firewall dall'account "ContosoAdlAcct"

## PARAMETERS

### -Account
Account Data Lake Analytics da cui ottenere la regola del firewall

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
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

### -Name
Nome della regola del firewall.

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

### -ResourceGroupName
Nome del gruppo di risorse in cui si vuole recuperare l'account.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule

## NOTE

## COLLEGAMENTI CORRELATI
