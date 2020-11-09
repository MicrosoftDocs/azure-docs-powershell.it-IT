---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: c319ee7fba1bddff8e93e56601c623658094253d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298639"
---
# <span data-ttu-id="4b4ef-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="4b4ef-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="4b4ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b4ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4ef-103">Aggiungere la risorsa flusso di dati e le relative dipendenze in una specifica sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="4b4ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b4ef-104">SYNTAX</span></span>

### <span data-ttu-id="4b4ef-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b4ef-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b4ef-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4b4ef-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b4ef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b4ef-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b4ef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b4ef-108">DESCRIPTION</span></span>
<span data-ttu-id="4b4ef-109">Questo comando associa la risorsa flusso di dati e le relative dipendenze alla sessione di debug specifica che la sequenza di comandi di PowerShell per il flusso di lavoro debug flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="4b4ef-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="4b4ef-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4b4ef-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="4b4ef-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="4b4ef-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="4b4ef-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per diversi comandi/destinazioni oppure ripetere il passaggio 2-3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="4b4ef-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="4b4ef-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4b4ef-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="4b4ef-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b4ef-114">EXAMPLES</span></span>

### <span data-ttu-id="4b4ef-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b4ef-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="4b4ef-116">Aggiungere il pacchetto flusso di dati alla sessione di debug "550effe4-93a3-485C-8525-eaf25259efbd" di "WikiADF" Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="4b4ef-117">Il file pakcage contiene la risorsa debug flusso di dati, l'elenco di resouce debug di DataSet, l'elenco di risorse di debug del servizio collegato, l'impostazione di debug e l'ID sessione.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="4b4ef-118">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4b4ef-118">For instance:</span></span>

<span data-ttu-id="4b4ef-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = nome; AccountKey = chiave; EndpointSuffix = core. Windows. NET "}}}]," debugSettings ": {" sourceSettings ": [{" SourceName ":" source1 "," rowLimit ": 1000}]}," sessionId ":" 4f988caf-e765-47d2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="4b4ef-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="4b4ef-120">Il parametro SessionID viene usato per sostituire la proprietà sessionId esistente nel file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="4b4ef-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b4ef-121">PARAMETERS</span></span>

### <span data-ttu-id="4b4ef-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4b4ef-122">-DataFactory</span></span>
<span data-ttu-id="4b4ef-123">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ef-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4b4ef-124">-DataFactoryName</span></span>
<span data-ttu-id="4b4ef-125">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-125">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4ef-126">-DefaultProfile</span></span>
<span data-ttu-id="4b4ef-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4ef-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="4b4ef-128">-PackageFile</span></span>
<span data-ttu-id="4b4ef-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ef-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b4ef-130">-PassThru</span></span>
<span data-ttu-id="4b4ef-131">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="4b4ef-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b4ef-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4ef-133">-ResourceGroupName</span></span>
<span data-ttu-id="4b4ef-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ef-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b4ef-135">-ResourceId</span></span>
<span data-ttu-id="4b4ef-136">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4ef-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b4ef-137">-Confirm</span></span>
<span data-ttu-id="4b4ef-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4ef-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4ef-139">-WhatIf</span></span>
<span data-ttu-id="4b4ef-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b4ef-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4ef-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4ef-142">CommonParameters</span></span>
<span data-ttu-id="4b4ef-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4ef-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4ef-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b4ef-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4ef-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b4ef-145">INPUTS</span></span>

### <span data-ttu-id="4b4ef-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4ef-146">System.String</span></span>

### <span data-ttu-id="4b4ef-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4b4ef-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4b4ef-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b4ef-148">OUTPUTS</span></span>

### <span data-ttu-id="4b4ef-149">System. void</span><span class="sxs-lookup"><span data-stu-id="4b4ef-149">System.Void</span></span>

### <span data-ttu-id="4b4ef-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b4ef-150">System.Boolean</span></span>

## <span data-ttu-id="4b4ef-151">Note</span><span class="sxs-lookup"><span data-stu-id="4b4ef-151">NOTES</span></span>
<span data-ttu-id="4b4ef-152">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="4b4ef-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4b4ef-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b4ef-153">RELATED LINKS</span></span>

[<span data-ttu-id="4b4ef-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4b4ef-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="4b4ef-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4b4ef-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="4b4ef-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="4b4ef-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="4b4ef-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="4b4ef-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
