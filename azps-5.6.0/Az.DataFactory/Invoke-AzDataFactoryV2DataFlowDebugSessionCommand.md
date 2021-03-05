---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: e54823cc6dff1f58b594604841c1d37bf249b7ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975102"
---
# <span data-ttu-id="38174-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="38174-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="38174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38174-102">SYNOPSIS</span></span>
<span data-ttu-id="38174-103">Richiamare l'azione di debug nella sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="38174-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38174-104">SYNTAX</span></span>

### <span data-ttu-id="38174-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="38174-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38174-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="38174-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38174-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="38174-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38174-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38174-108">DESCRIPTION</span></span>
<span data-ttu-id="38174-109">Questo comando esegue l'anteprima dei dati, l'anteprima delle statistiche o l'anteprima dell'espressione per diversi flussi di dati nella sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="38174-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="38174-110">La sequenza di comandi di PowerShell per il flusso di lavoro di debug del flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="38174-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="38174-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="38174-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="38174-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="38174-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="38174-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per i diversi comandi/destinazioni oppure ripetere i passaggi da 2 a 3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="38174-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="38174-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="38174-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="38174-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38174-115">EXAMPLES</span></span>

### <span data-ttu-id="38174-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38174-116">Example 1</span></span>
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

<span data-ttu-id="38174-117">Questo esempio richiama il comando anteprima dati per la sessione di debug "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" nel data factory "WiKiADF" e quindi converte l'output JSON in una stringa leggibile.</span><span class="sxs-lookup"><span data-stu-id="38174-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="38174-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38174-118">PARAMETERS</span></span>

### <span data-ttu-id="38174-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38174-119">-AsJob</span></span>
<span data-ttu-id="38174-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38174-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38174-121">-Columns</span><span class="sxs-lookup"><span data-stu-id="38174-121">-Columns</span></span>
<span data-ttu-id="38174-122">Elenco di colonne per l'anteprima delle statistiche del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-122">The columns list for data flow statistics preview.</span></span>

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

### <span data-ttu-id="38174-123">-Command</span><span class="sxs-lookup"><span data-stu-id="38174-123">-Command</span></span>
<span data-ttu-id="38174-124">Comando di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-124">The data flow debug command.</span></span> <span data-ttu-id="38174-125">Gli elementi facoltativi sono executePreviewQuery, executeStatisticsQuery e executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="38174-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="38174-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="38174-126">-DataFactory</span></span>
<span data-ttu-id="38174-127">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="38174-127">The data factory object.</span></span>

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

### <span data-ttu-id="38174-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="38174-128">-DataFactoryName</span></span>
<span data-ttu-id="38174-129">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="38174-129">The data factory name.</span></span>

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

### <span data-ttu-id="38174-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38174-130">-DefaultProfile</span></span>
<span data-ttu-id="38174-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38174-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38174-132">-Expression</span><span class="sxs-lookup"><span data-stu-id="38174-132">-Expression</span></span>
<span data-ttu-id="38174-133">Espressione per l'anteprima dell'espressione del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-133">The expression for data flow expression preview.</span></span>

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

### <span data-ttu-id="38174-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38174-134">-ResourceGroupName</span></span>
<span data-ttu-id="38174-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38174-135">The resource group name.</span></span>

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

### <span data-ttu-id="38174-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38174-136">-ResourceId</span></span>
<span data-ttu-id="38174-137">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="38174-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="38174-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="38174-138">-RowLimits</span></span>
<span data-ttu-id="38174-139">Limite di righe per l'anteprima dei dati del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-139">The row limit for data flow data preview.</span></span>

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

### <span data-ttu-id="38174-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="38174-140">-SessionId</span></span>
<span data-ttu-id="38174-141">ID sessione di debug del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="38174-141">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="38174-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="38174-142">-StreamName</span></span>
<span data-ttu-id="38174-143">Il nome del flusso di dati per il debug.</span><span class="sxs-lookup"><span data-stu-id="38174-143">The stream name of data flow for debugging.</span></span>

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

### <span data-ttu-id="38174-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38174-144">-Confirm</span></span>
<span data-ttu-id="38174-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38174-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38174-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38174-146">-WhatIf</span></span>
<span data-ttu-id="38174-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38174-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38174-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38174-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38174-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38174-149">CommonParameters</span></span>
<span data-ttu-id="38174-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38174-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38174-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38174-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38174-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="38174-152">INPUTS</span></span>

### <span data-ttu-id="38174-153">System.String</span><span class="sxs-lookup"><span data-stu-id="38174-153">System.String</span></span>

### <span data-ttu-id="38174-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="38174-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="38174-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38174-155">OUTPUTS</span></span>

### <span data-ttu-id="38174-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="38174-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="38174-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="38174-157">NOTES</span></span>
<span data-ttu-id="38174-158">Parole chiave: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="38174-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="38174-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38174-159">RELATED LINKS</span></span>

[<span data-ttu-id="38174-160">Start-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="38174-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="38174-161">Get-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="38174-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="38174-162">Add-AzDataSessionV2DataFlowSessionPackage</span><span class="sxs-lookup"><span data-stu-id="38174-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="38174-163">Stop-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="38174-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
