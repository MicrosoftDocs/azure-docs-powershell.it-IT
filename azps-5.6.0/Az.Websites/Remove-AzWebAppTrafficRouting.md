---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990694"
---
# Remove-AzWebAppTrafficRouting

## SYNOPSIS
Rimuovere una regola di routing dallo slot.

## SINTASSI

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzWebAppTrafficRouting** rimuove una regola di routing da uno slot Di Azure Web App.

## ESEMPI

### Esempio 1: rimuovere la regola di routing specifica dallo slot della webapp
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

Questo comando rimuove una regola di routing per un determinato slot webapp.

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

### -ResourceGroupName
Nome gruppo di risorse

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

### -RuleName
Nome regola

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

### -WebAppName
Nome WebApp

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

### -PassThru
Restituire l'oggetto configurazione della restrizione di accesso.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft.Azure.Management.WebSites.Models.RampUpRule

## NOTE

## COLLEGAMENTI CORRELATI
[Add-AzWebAppTrafficRouting](./Add-AzWebAppTrafficRouting.md)

[Get-AzWebAppTrafficRouting](./Get-AzWebAppTrafficRouting.md)

[Update-AzWebAppTrafficRouting](./Update-AzWebAppTrafficRouting.md)