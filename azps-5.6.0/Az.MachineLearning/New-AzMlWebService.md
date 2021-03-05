---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 1a48438d6cec1621361a00cefa2bfead28117b97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960558"
---
# New-AzMlWebService

## SYNOPSIS
Crea un nuovo servizio Web.

## SINTASSI

### CreateFromFile
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Crea un servizio Web Azure Machine Learning in un gruppo di risorse esistente.
Se nel gruppo di risorse è presente un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.

## ESEMPI

### Esempio 1: Creare un nuovo servizio da una definizione basata su file Json
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Crea un nuovo servizio Web Azure Machine Learning denominato "mywebservicename" nel gruppo "myresourcegroup" e nell'area Stati Uniti centro meridionale, in base alla definizione presente nel file JSON a cui viene fatto riferimento.

### Esempio 2: Creare un nuovo servizio da un'istanza di un oggetto
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

È possibile ottenere un'istanza dell'oggetto servizio Web da personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzMlWebService Web.

## PARAMETERS

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

### -DefinitionFile
Specifica il percorso del file che contiene la definizione in formato JSON del servizio Web.
La specifica più recente per la definizione del servizio Web è indicata nella specifica più recente in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Non chiedere conferma.

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

### -Location
Area geografica del servizio Web.
Immettere un'area geografica per il data center di Azure, ad esempio "Stati Uniti occidentali" o "Asia sud-orientale".
È possibile inserire un servizio Web in qualsiasi area geografica che supporti risorse di questo tipo.
Il servizio Web non deve essere nella stessa area geografica della sottoscrizione di Azure o nella stessa area geografica del relativo gruppo di risorse.
I gruppi di risorse possono contenere servizi Web da aree geografiche diverse.
Per determinare le aree geografiche che supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet del parametro ProviderNtassi.

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

### -Name
Nome del servizio Web.
Il nome deve essere univoco nel gruppo di risorse.

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

### -NewWebServiceDefinition
Definizione del nuovo servizio Web che contiene tutte le proprietà che costituiscono il servizio.
Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.
La specifica più recente per la definizione del servizio Web è indicata nella specifica più recente in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Gruppo di risorse in cui inserire il servizio Web.
Immettere un'area geografica per il data center di Azure, ad esempio "Stati Uniti occidentali" o "Asia sud-orientale".
È possibile inserire un servizio Web in qualsiasi area geografica che supporti risorse di questo tipo.
Il servizio Web non deve essere nella stessa area geografica della sottoscrizione di Azure o nella stessa area geografica del relativo gruppo di risorse.
I gruppi di risorse possono contenere servizi Web da aree geografiche diverse.
Per determinare le aree geografiche che supportano ogni tipo di risorsa, usare la Get-AzResourceProvider con il cmdlet del parametro ProviderNtassi.

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
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## OUTPUT

### Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService

## NOTE
Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml

## COLLEGAMENTI CORRELATI
