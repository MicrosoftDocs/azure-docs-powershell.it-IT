---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201063"
---
# New-AzAutomationModule

## SYNOPSIS
Importa un modulo nell'automazione.

## SINTASSI

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzAutomationModule** importa un modulo nell'automazione di Azure.
Questo comando accetta un file compresso con estensione zip.
Il file contiene una cartella che include un file di uno dei tipi seguenti: 
- Windows PowerShell modulo, con estensione psm1 o dll 
- Windows PowerShell manifesto del modulo, con estensione psd1, Il nome del file ZIP, il nome della cartella e il nome del file nella cartella devono essere uguali.
Specificare il file ZIP come URL a cui il servizio di automazione può accedere.
Se si importa un modulo Windows PowerShell'automazione usando questo cmdlet o il cmdlet Set-AzAutomationModule, l'operazione è asincrona.
Il comando termina se l'importazione riesce o meno.
Per verificare se l'operazione ha avuto esito positivo, eseguire il comando seguente: ModuleName Controllare la proprietà ProvisioningState per il valore `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Succeeded. 

## ESEMPI

### Esempio 1: Importare un modulo
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.
Il modulo viene archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e in un contenitore denominato modules.

## PARAMETERS

### -AutomationAccountName
Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkUri
URL di un pacchetto ZIP del modulo

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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
Specifica il nome del modulo che questo cmdlet importa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.

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

### System.Uri

## OUTPUT

### Microsoft.Azure.Commands.Automation.Model.Module

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


