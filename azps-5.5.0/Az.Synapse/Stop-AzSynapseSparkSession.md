---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195535"
---
# <span data-ttu-id="9767d-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9767d-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="9767d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9767d-102">SYNOPSIS</span></span>
<span data-ttu-id="9767d-103">Interrompe una sessione di Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9767d-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9767d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9767d-104">SYNTAX</span></span>

### <span data-ttu-id="9767d-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9767d-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9767d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9767d-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9767d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9767d-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9767d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9767d-108">DESCRIPTION</span></span>
<span data-ttu-id="9767d-109">Il cmdlet **Stop-AzSynapseSparkSession** interrompe una sessione synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9767d-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="9767d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9767d-110">EXAMPLES</span></span>

### <span data-ttu-id="9767d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9767d-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="9767d-112">Questo comando interrompe una sessione di Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="9767d-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="9767d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9767d-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="9767d-114">Questo comando interrompe una sessione di Synapse Analytics Spark tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9767d-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="9767d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9767d-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="9767d-116">Questo comando interrompe una sessione di Synapse Analytics Spark tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="9767d-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="9767d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9767d-117">PARAMETERS</span></span>

### <span data-ttu-id="9767d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9767d-118">-AsJob</span></span>
<span data-ttu-id="9767d-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9767d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9767d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9767d-120">-DefaultProfile</span></span>
<span data-ttu-id="9767d-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9767d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9767d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9767d-122">-InputObject</span></span>
<span data-ttu-id="9767d-123">Oggetto di input della sessione Spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9767d-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9767d-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="9767d-124">-LivyId</span></span>
<span data-ttu-id="9767d-125">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="9767d-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9767d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9767d-126">-PassThru</span></span>
<span data-ttu-id="9767d-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9767d-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9767d-128">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9767d-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9767d-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="9767d-129">-SparkPoolName</span></span>
<span data-ttu-id="9767d-130">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="9767d-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9767d-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="9767d-131">-SparkPoolObject</span></span>
<span data-ttu-id="9767d-132">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="9767d-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9767d-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9767d-133">-WorkspaceName</span></span>
<span data-ttu-id="9767d-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="9767d-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9767d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9767d-135">-Confirm</span></span>
<span data-ttu-id="9767d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9767d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9767d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9767d-137">-WhatIf</span></span>
<span data-ttu-id="9767d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9767d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9767d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9767d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9767d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9767d-140">CommonParameters</span></span>
<span data-ttu-id="9767d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9767d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9767d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9767d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9767d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="9767d-143">INPUTS</span></span>

### <span data-ttu-id="9767d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="9767d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="9767d-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="9767d-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="9767d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9767d-146">OUTPUTS</span></span>

### <span data-ttu-id="9767d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9767d-147">System.Boolean</span></span>

## <span data-ttu-id="9767d-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="9767d-148">NOTES</span></span>

## <span data-ttu-id="9767d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9767d-149">RELATED LINKS</span></span>
