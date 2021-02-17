---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177142"
---
# <span data-ttu-id="84995-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="84995-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="84995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84995-102">SYNOPSIS</span></span>
<span data-ttu-id="84995-103">Avvia una sessione di debug del flusso di dati in Data factory di Azure</span><span class="sxs-lookup"><span data-stu-id="84995-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="84995-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84995-104">SYNTAX</span></span>

### <span data-ttu-id="84995-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="84995-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84995-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="84995-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84995-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84995-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84995-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84995-108">DESCRIPTION</span></span>
<span data-ttu-id="84995-109">Questo comando a esecuzione lunga avvia una sessione di debug del flusso di dati per i futuri comandi di debug.</span><span class="sxs-lookup"><span data-stu-id="84995-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="84995-110">Questo comando può essere associato a una definizione di runtime di integrazione per configurare le dimensioni/tipo del cluster di sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="84995-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="84995-111">La sequenza di comandi di PowerShell per il flusso di lavoro di debug del flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="84995-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="84995-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="84995-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="84995-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="84995-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="84995-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per i diversi comandi/destinazioni oppure ripetere i passaggi da 2 a 3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="84995-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="84995-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="84995-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="84995-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84995-116">EXAMPLES</span></span>

### <span data-ttu-id="84995-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84995-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="84995-118">Avvia una sessione di debug con il contrassegno AsJob.</span><span class="sxs-lookup"><span data-stu-id="84995-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="84995-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84995-119">PARAMETERS</span></span>

### <span data-ttu-id="84995-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84995-120">-AsJob</span></span>
<span data-ttu-id="84995-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="84995-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84995-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="84995-122">-DataFactory</span></span>
<span data-ttu-id="84995-123">Oggetto data factory.</span><span class="sxs-lookup"><span data-stu-id="84995-123">The data factory object.</span></span>

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

### <span data-ttu-id="84995-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84995-124">-DataFactoryName</span></span>
<span data-ttu-id="84995-125">Nome del data factory.</span><span class="sxs-lookup"><span data-stu-id="84995-125">The data factory name.</span></span>

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

### <span data-ttu-id="84995-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84995-126">-DefaultProfile</span></span>
<span data-ttu-id="84995-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84995-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84995-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="84995-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="84995-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="84995-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84995-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84995-130">-ResourceGroupName</span></span>
<span data-ttu-id="84995-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84995-131">The resource group name.</span></span>

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

### <span data-ttu-id="84995-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84995-132">-ResourceId</span></span>
<span data-ttu-id="84995-133">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="84995-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84995-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84995-134">-Confirm</span></span>
<span data-ttu-id="84995-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84995-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84995-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84995-136">-WhatIf</span></span>
<span data-ttu-id="84995-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84995-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84995-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84995-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84995-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84995-139">CommonParameters</span></span>
<span data-ttu-id="84995-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84995-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84995-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84995-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84995-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="84995-142">INPUTS</span></span>

### <span data-ttu-id="84995-143">System.String</span><span class="sxs-lookup"><span data-stu-id="84995-143">System.String</span></span>

### <span data-ttu-id="84995-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="84995-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="84995-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84995-145">OUTPUTS</span></span>

### <span data-ttu-id="84995-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowSession</span><span class="sxs-lookup"><span data-stu-id="84995-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="84995-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="84995-147">NOTES</span></span>
<span data-ttu-id="84995-148">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="84995-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84995-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84995-149">RELATED LINKS</span></span>

[<span data-ttu-id="84995-150">Get-AzDataSessionV2DataFlowSession</span><span class="sxs-lookup"><span data-stu-id="84995-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="84995-151">Add-AzDataSessionV2DataFlowSessionPackage</span><span class="sxs-lookup"><span data-stu-id="84995-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="84995-152">Invoke-AzDataSessionV2DataFlowSessionCommand</span><span class="sxs-lookup"><span data-stu-id="84995-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="84995-153">Stop-AzDataSessionV2DataFlowFlowSession</span><span class="sxs-lookup"><span data-stu-id="84995-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)