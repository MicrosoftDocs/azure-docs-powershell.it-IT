---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject.md
ms.openlocfilehash: c9f2a8440f2ed91003dc818824a8d7b8662a96a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197918"
---
# New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject

## SYNOPSIS
Creare una nuova regola di avviso personalizzata per l'elenco di indirizzi consentiti per il gruppo di sicurezza dei dispositivi (Sicurezza IoT)

## SINTASSI

```
New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -AllowlistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject cmdlet crea un nuovo elenco di regole di avviso personalizzate consentite per il gruppo di sicurezza dei dispositivi nella soluzione di sicurezza IoT.

## ESEMPI

### Esempio 1
```powershell
PS C:\> New-AzDeviceSecurityGroupAllowlistCustomAlertRuleObject -Enabled $false -Type "LocalUserNotAllowed" -AllowlistValue @()

RuleType: "LocalUserNotAllowed"
DisplayName: "Login by a local user that isn't allowed"
Description: "Get an alert when a local user that isn't allowed logins to the device"
IsEnabled: false
ValueType: "String"
AllowlistValues: []
```

Crea nuovo avviso personalizzato dell'elenco di utenti consentiti dal tipo "LocalUserNotAllowed" con stato impostato su disable

## PARAMETERS

### -AllowlistValue
Valori di elenco consentiti.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Enabled
La regola è abilitata.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Tipo di regola.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule

## NOTE

## COLLEGAMENTI CORRELATI
