---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182135"
---
# Set-AzAutomationModule

## SYNOPSIS
Aggiorna un modulo nell'automazione.

## SINTASSI

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIZIONE
Il **cmdlet Set-AzAutomationModule** aggiorna un modulo nell'automazione di Azure.
Questo comando accetta un file compresso con estensione zip.
Il file contiene una cartella che include un file di uno dei tipi seguenti: 
- wps_2 modulo, con estensione psm1 o dll 
- wps_2 manifesto del modulo, con estensione psd1, Il nome del file ZIP, il nome della cartella e il nome del file nella cartella devono essere uguali.
Specificare il file ZIP come URL a cui il servizio di automazione può accedere.
Se si importa un modulo wps_2'automazione usando questo cmdlet o il cmdlet New-AzAutomationModule, l'operazione è asincrona.
Il comando termina se l'importazione riesce o meno.
Per verificare se l'operazione ha avuto esito positivo, eseguire il comando seguente: ModuleName Controllare la proprietà ProvisioningState per il valore `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Succeeded. 

## ESEMPI

### Esempio 1: Aggiornare un modulo
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

Questo comando importa una versione aggiornata di un modulo esistente denominato ContosoModule nell'account di automazione denominato Contoso17.  Il modulo viene archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e in un contenitore denominato modules.

## PARAMETERS

### -AutomationAccountName
Specifica il nome dell'account di automazione per cui questo cmdlet aggiorna un modulo.

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
Specifica l'URL del file ZIP che contiene la nuova versione di un modulo importato dal cmdlet.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Specifica la versione del modulo a cui questo cmdlet aggiorna l'automazione.

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
Specifica il nome di un gruppo di risorse per cui questo cmdlet aggiorna un modulo.

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

[New-AzAutomationModule](./New-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)


