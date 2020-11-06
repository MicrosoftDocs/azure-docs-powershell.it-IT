---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521906"
---
# New-AzureRmMlWebService

## Sinossi
Crea un nuovo servizio Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### CreateFromFile
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromInstance
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Crea un servizio Web di apprendimento di Azure Machine in un gruppo di risorse esistente.
Se nel gruppo risorse esiste un servizio Web con lo stesso nome, la chiamata funge da operazione di aggiornamento e il servizio Web esistente viene sovrascritto.

## ESEMPI

### --------------------------Esempio 1: creare un nuovo servizio da una definizione basata su file JSON--------------------------
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

Crea un nuovo servizio Web di apprendimento di Azure Machine denominato "WebServiceName" nel gruppo "myresourcegroup" e nell'area sud centrale degli Stati Uniti, in base alla definizione presente nel file JSON a cui si fa riferimento.

### --------------------------Esempio 2: creare un nuovo servizio da un'istanza di oggetto--------------------------
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

Puoi ottenere un'istanza di un oggetto servizio Web per personalizzare prima della pubblicazione come risorsa usando il cmdlet Import-AzureRmMlWebService.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefinitionFile
Specifica il percorso del file che contiene la definizione del formato JSON del servizio Web.
Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .

```yaml
Type: String
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Area geografica del servizio Web.
Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".
Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.
Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.
I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.
Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzureRmResourceProvider con il cmdlet parametro ProviderNamespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome del servizio Web.
Il nome deve essere univoco nel gruppo risorse.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewWebServiceDefinition
La definizione per il nuovo servizio Web, contenente tutte le proprietà che costituiscono il servizio.
Questo parametro è obbligatorio e rappresenta un'istanza della classe Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.
Puoi trovare le specifiche più recenti per la definizione del servizio Web nella specifica spavalderia in https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .

```yaml
Type: WebService
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
Immettere un'area del centro dati di Azure, ad esempio "West US" o "Asia sud-orientale".
Puoi inserire un servizio Web in qualsiasi area geografica che supporti le risorse del tipo.
Il servizio Web non deve essere nella stessa area geografica dell'abbonamento a Azure o della stessa area geografica del gruppo di risorse.
I gruppi di risorse possono contenere servizi Web provenienti da aree geografiche diverse.
Per determinare quali aree geografiche supportano ogni tipo di risorsa, usare la Get-AzureRmResourceProvider con il cmdlet parametro ProviderNamespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Servizio
Il parametro ' NewWebServiceDefinition ' accetta il valore di tipo ' WebService ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService
Descrizione di riepilogo del servizio Web di Azure Machine Learning.
In modo analogo alla descrizione restituita chiamando il cmdlet Get-AzureRmMlWebService in un servizio Web esistente.
Questa descrizione non contiene proprietà riservate, ad esempio le credenziali dell'account di archiviazione e i tasti di scelta del servizio.

## Note
Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml

## COLLEGAMENTI CORRELATI

