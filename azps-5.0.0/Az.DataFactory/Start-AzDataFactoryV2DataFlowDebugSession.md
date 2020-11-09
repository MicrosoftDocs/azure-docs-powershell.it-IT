---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 27a7f0ee401f044cc693cecf103f2bed1e8ce946
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298230"
---
# <span data-ttu-id="b0335-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b0335-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0335-102">SYNOPSIS</span></span>
<span data-ttu-id="b0335-103">Avvia una sessione di debug del flusso di dati in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="b0335-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="b0335-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0335-104">SYNTAX</span></span>

### <span data-ttu-id="b0335-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0335-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0335-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b0335-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0335-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0335-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0335-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0335-108">DESCRIPTION</span></span>
<span data-ttu-id="b0335-109">Questo comando a esecuzione prolungata avvia una sessione di debug del flusso di dati per i comandi di debug imminenti.</span><span class="sxs-lookup"><span data-stu-id="b0335-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="b0335-110">Questo comando può essere associato a una definizione di runtime di Integration per configurare le dimensioni e il tipo di cluster di sessione di debug.</span><span class="sxs-lookup"><span data-stu-id="b0335-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="b0335-111">La sequenza di comandi di PowerShell per il flusso di lavoro debug flusso di dati deve essere:</span><span class="sxs-lookup"><span data-stu-id="b0335-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="b0335-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="b0335-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b0335-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="b0335-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (ripetere questo passaggio per diversi comandi/destinazioni oppure ripetere il passaggio 2-3 per modificare il file del pacchetto)</span><span class="sxs-lookup"><span data-stu-id="b0335-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="b0335-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b0335-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0335-116">EXAMPLES</span></span>

### <span data-ttu-id="b0335-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0335-117">Example 1</span></span>
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

<span data-ttu-id="b0335-118">Avvia una sessione di debug con il contrassegno AsJob.</span><span class="sxs-lookup"><span data-stu-id="b0335-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="b0335-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0335-119">PARAMETERS</span></span>

### <span data-ttu-id="b0335-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0335-120">-AsJob</span></span>
<span data-ttu-id="b0335-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b0335-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0335-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b0335-122">-DataFactory</span></span>
<span data-ttu-id="b0335-123">Oggetto Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b0335-123">The data factory object.</span></span>

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

### <span data-ttu-id="b0335-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b0335-124">-DataFactoryName</span></span>
<span data-ttu-id="b0335-125">Nome della factory di dati.</span><span class="sxs-lookup"><span data-stu-id="b0335-125">The data factory name.</span></span>

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

### <span data-ttu-id="b0335-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0335-126">-DefaultProfile</span></span>
<span data-ttu-id="b0335-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0335-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0335-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="b0335-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="b0335-129">Percorso del file JSON.</span><span class="sxs-lookup"><span data-stu-id="b0335-129">The JSON file path.</span></span>

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

### <span data-ttu-id="b0335-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0335-130">-ResourceGroupName</span></span>
<span data-ttu-id="b0335-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0335-131">The resource group name.</span></span>

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

### <span data-ttu-id="b0335-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0335-132">-ResourceId</span></span>
<span data-ttu-id="b0335-133">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0335-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b0335-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0335-134">-Confirm</span></span>
<span data-ttu-id="b0335-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0335-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0335-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0335-136">-WhatIf</span></span>
<span data-ttu-id="b0335-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0335-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0335-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0335-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0335-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0335-139">CommonParameters</span></span>
<span data-ttu-id="b0335-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0335-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0335-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0335-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0335-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0335-142">INPUTS</span></span>

### <span data-ttu-id="b0335-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b0335-143">System.String</span></span>

### <span data-ttu-id="b0335-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b0335-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b0335-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0335-145">OUTPUTS</span></span>

### <span data-ttu-id="b0335-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="b0335-147">Note</span><span class="sxs-lookup"><span data-stu-id="b0335-147">NOTES</span></span>
<span data-ttu-id="b0335-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="b0335-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b0335-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0335-149">RELATED LINKS</span></span>

[<span data-ttu-id="b0335-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b0335-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b0335-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="b0335-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="b0335-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="b0335-153">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b0335-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)