---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: 185f01f31f8cae62e51b7b28909f66fbf37884e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992808"
---
# <span data-ttu-id="613b3-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="613b3-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="613b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="613b3-102">SYNOPSIS</span></span>
<span data-ttu-id="613b3-103">Aggiungere la risorsa flusso di dati e le dipendenze in una specifica sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="613b3-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="613b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="613b3-104">SYNTAX</span></span>

### <span data-ttu-id="613b3-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="613b3-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="613b3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="613b3-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="613b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="613b3-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="613b3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="613b3-108">DESCRIPTION</span></span>
<span data-ttu-id="613b3-109">Questo comando collega la risorsa del flusso di dati e le dipendenze alla specifica sessione di debug La sequenza di comandi di PowerShell per il flusso di lavoro di debug del flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="613b3-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="613b3-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="613b3-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="613b3-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="613b3-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="613b3-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per i diversi comandi/destinazioni oppure ripetere i passaggi da 2 a 3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="613b3-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="613b3-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="613b3-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="613b3-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="613b3-114">EXAMPLES</span></span>

### <span data-ttu-id="613b3-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="613b3-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="613b3-116">Aggiungere il pacchetto del flusso di dati nella sessione di debug "550effe4-93a3-485c-8525-eaf25259efbd" del data factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="613b3-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="613b3-117">Il file Pakcage contiene le risorse di debug del flusso di dati, l'elenco del resouce di debug del set di dati, l'elenco delle risorse di debug del servizio collegate, l'impostazione di debug e l'ID sessione.</span><span class="sxs-lookup"><span data-stu-id="613b3-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="613b3-118">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="613b3-118">For instance:</span></span>

<span data-ttu-id="613b3-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "più": \ "trasformazioni": \ "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedText Output", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": \ "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/dataset } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": \ "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } }, "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="613b3-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="613b3-120">Il parametro SessionID viene usato per sostituire la proprietà sessionId esistente nel file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="613b3-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="613b3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="613b3-121">PARAMETERS</span></span>

### <span data-ttu-id="613b3-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="613b3-122">-DataFactory</span></span>
<span data-ttu-id="613b3-123">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="613b3-123">The data factory object.</span></span>

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

### <span data-ttu-id="613b3-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="613b3-124">-DataFactoryName</span></span>
<span data-ttu-id="613b3-125">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="613b3-125">The data factory name.</span></span>

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

### <span data-ttu-id="613b3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613b3-126">-DefaultProfile</span></span>
<span data-ttu-id="613b3-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="613b3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="613b3-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="613b3-128">-PackageFile</span></span>
<span data-ttu-id="613b3-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="613b3-129">The JSON file path.</span></span>

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

### <span data-ttu-id="613b3-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="613b3-130">-PassThru</span></span>
<span data-ttu-id="613b3-131">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="613b3-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="613b3-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="613b3-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="613b3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="613b3-133">-ResourceGroupName</span></span>
<span data-ttu-id="613b3-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="613b3-134">The resource group name.</span></span>

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

### <span data-ttu-id="613b3-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="613b3-135">-ResourceId</span></span>
<span data-ttu-id="613b3-136">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="613b3-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="613b3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="613b3-137">-Confirm</span></span>
<span data-ttu-id="613b3-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="613b3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="613b3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="613b3-139">-WhatIf</span></span>
<span data-ttu-id="613b3-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="613b3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="613b3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="613b3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="613b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613b3-142">CommonParameters</span></span>
<span data-ttu-id="613b3-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613b3-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="613b3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613b3-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="613b3-145">INPUTS</span></span>

### <span data-ttu-id="613b3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="613b3-146">System.String</span></span>

### <span data-ttu-id="613b3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="613b3-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="613b3-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="613b3-148">OUTPUTS</span></span>

### <span data-ttu-id="613b3-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="613b3-149">System.Void</span></span>

### <span data-ttu-id="613b3-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="613b3-150">System.Boolean</span></span>

## <span data-ttu-id="613b3-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="613b3-151">NOTES</span></span>
<span data-ttu-id="613b3-152">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="613b3-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="613b3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="613b3-153">RELATED LINKS</span></span>

[<span data-ttu-id="613b3-154">Start-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="613b3-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="613b3-155">Get-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="613b3-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="613b3-156">Invoke-AzDataSessionV2DataFlowSessionCommand</span><span class="sxs-lookup"><span data-stu-id="613b3-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="613b3-157">Stop-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="613b3-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
