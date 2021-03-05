---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 49b4a02210105529dff2aae2b895d4059ced97f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009997"
---
# Remove-AzAutomationAccount

## SYNOPSIS
Rimuove un account di automazione.

## SINTASSI

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Remove-AzAutomationAccount** rimuove un account di automazione di Azure da un gruppo di risorse.
Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.

## ESEMPI

### Esempio 1: Rimuovere un account di automazione
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

Questo comando rimuove un account di automazione denominato ContosoAutomationAccount senza richiedere la convalida dell'utente.

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

### -Force
ps_force

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
Specifica il nome dell'account di automazione rimosso dal cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove un account di automazione.

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

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Automation.Model.AutomationAccount

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzAutomationAccount](./Get-AzAutomationAccount.md)

[New-AzAutomationAccount](./New-AzAutomationAccount.md)

[Set-AzAutomationAccount](./Set-AzAutomationAccount.md)


