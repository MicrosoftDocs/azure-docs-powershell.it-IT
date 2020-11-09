---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298476"
---
# <span data-ttu-id="143c1-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="143c1-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="143c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="143c1-102">SYNOPSIS</span></span>
<span data-ttu-id="143c1-103">Richiamare l'azione di debug nella sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="143c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="143c1-104">SYNTAX</span></span>

### <span data-ttu-id="143c1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="143c1-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="143c1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="143c1-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="143c1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="143c1-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="143c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="143c1-108">DESCRIPTION</span></span>
<span data-ttu-id="143c1-109">Questo comando esegue Data Preview/stats Preview/Expression Preview per un flusso diverso di flusso di dati nella sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="143c1-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="143c1-110">La sequenza di comandi di PowerShell per il flusso di lavoro debug flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="143c1-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="143c1-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="143c1-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="143c1-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="143c1-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="143c1-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per diversi comandi/destinazioni oppure ripetere il passaggio 2-3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="143c1-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="143c1-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="143c1-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="143c1-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="143c1-115">EXAMPLES</span></span>

### <span data-ttu-id="143c1-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="143c1-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="143c1-117">Questo esempio richiama il comando Anteprima dati per la sessione di debug "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" in Factory di dati "WiKiADF" e quindi converte l'output JSON in una stringa leggibile.</span><span class="sxs-lookup"><span data-stu-id="143c1-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="143c1-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="143c1-118">PARAMETERS</span></span>

### <span data-ttu-id="143c1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="143c1-119">-AsJob</span></span>
<span data-ttu-id="143c1-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="143c1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="143c1-121">-Colonne</span><span class="sxs-lookup"><span data-stu-id="143c1-121">-Columns</span></span>
<span data-ttu-id="143c1-122">Elenco colonne per statistiche flusso di dati in anteprima.</span><span class="sxs-lookup"><span data-stu-id="143c1-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-123">-Comando</span><span class="sxs-lookup"><span data-stu-id="143c1-123">-Command</span></span>
<span data-ttu-id="143c1-124">Comando debug flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-124">The data flow debug command.</span></span> <span data-ttu-id="143c1-125">Le opzioni sono executePreviewQuery, executeStatisticsQuery e executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="143c1-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="143c1-126">-DataFactory</span></span>
<span data-ttu-id="143c1-127">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="143c1-127">The data factory object.</span></span>

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

### <span data-ttu-id="143c1-128">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="143c1-128">-DataFactoryName</span></span>
<span data-ttu-id="143c1-129">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-129">The data factory name.</span></span>

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

### <span data-ttu-id="143c1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143c1-130">-DefaultProfile</span></span>
<span data-ttu-id="143c1-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="143c1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="143c1-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="143c1-132">-Expression</span></span>
<span data-ttu-id="143c1-133">Espressione per l'anteprima dell'espressione flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143c1-134">-ResourceGroupName</span></span>
<span data-ttu-id="143c1-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="143c1-135">The resource group name.</span></span>

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

### <span data-ttu-id="143c1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="143c1-136">-ResourceId</span></span>
<span data-ttu-id="143c1-137">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="143c1-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="143c1-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="143c1-138">-RowLimits</span></span>
<span data-ttu-id="143c1-139">Limite di riga per l'anteprima dei dati del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="143c1-140">-SessionId</span></span>
<span data-ttu-id="143c1-141">ID sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="143c1-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="143c1-142">-StreamName</span></span>
<span data-ttu-id="143c1-143">Nome flusso del flusso di dati per il debug.</span><span class="sxs-lookup"><span data-stu-id="143c1-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143c1-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="143c1-144">-Confirm</span></span>
<span data-ttu-id="143c1-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="143c1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="143c1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143c1-146">-WhatIf</span></span>
<span data-ttu-id="143c1-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="143c1-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="143c1-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="143c1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="143c1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143c1-149">CommonParameters</span></span>
<span data-ttu-id="143c1-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="143c1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143c1-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="143c1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143c1-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="143c1-152">INPUTS</span></span>

### <span data-ttu-id="143c1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="143c1-153">System.String</span></span>

### <span data-ttu-id="143c1-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="143c1-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="143c1-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="143c1-155">OUTPUTS</span></span>

### <span data-ttu-id="143c1-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="143c1-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="143c1-157">Note</span><span class="sxs-lookup"><span data-stu-id="143c1-157">NOTES</span></span>
<span data-ttu-id="143c1-158">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, factoriesKeywords: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="143c1-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="143c1-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="143c1-159">RELATED LINKS</span></span>

[<span data-ttu-id="143c1-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="143c1-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="143c1-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="143c1-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="143c1-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="143c1-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="143c1-163">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="143c1-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
