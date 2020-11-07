---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: e6aec3bc5d19cc89d6d2e854815fd78c5788fdb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685028"
---
# New-AzAutomationModule

## Sinossi
Importa un modulo in automazione.

## SINTASSI

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzAutomationModule** importa un modulo in Azure Automation.
Questo comando accetta un file compresso con estensione zip.
Il file contiene una cartella che include un file che è uno dei tipi seguenti: 
- modulo wps_2, con estensione di file psm1 o dll 
- wps_2 manifesto del modulo, con estensione psd1, il nome del file zip, il nome della cartella e il nome del file nella cartella devono essere identici.
Specificare il file zip come URL a cui può accedere il servizio di automazione.
Se si importa un modulo di wps_2 in automazione tramite questo cmdlet o il cmdlet Set-AzAutomationModule, l'operazione è asincrona.
Il comando termina se l'importazione ha esito positivo o negativo.
Per verificare se è riuscito, eseguire il comando seguente: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName verificare la proprietà **ProvisioningState** per un valore di succeeded.

## ESEMPI

### Esempio 1: importare un modulo
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.
Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.

## PARAMETRI

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
URL di un pacchetto zip di un modulo

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

### -Nome
Specifica il nome del modulo importato da questo cmdlet.

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String

### System. Uri

## OUTPUT

### Microsoft. Azure. Commands. Automation. Model. Module

## Note

## COLLEGAMENTI CORRELATI

[Get-AzAutomationModule](./Get-AzAutomationModule.md)

[Remove-AzAutomationModule](./Remove-AzAutomationModule.md)

[Set-AzAutomationModule](./Set-AzAutomationModule.md)


