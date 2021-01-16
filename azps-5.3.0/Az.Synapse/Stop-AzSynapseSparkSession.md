---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383109"
---
# <span data-ttu-id="99519-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="99519-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="99519-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99519-102">SYNOPSIS</span></span>
<span data-ttu-id="99519-103">Interrompe una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="99519-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="99519-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99519-104">SYNTAX</span></span>

### <span data-ttu-id="99519-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99519-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99519-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99519-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99519-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99519-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99519-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99519-108">DESCRIPTION</span></span>
<span data-ttu-id="99519-109">Il cmdlet **Stop-AzSynapseSparkSession** interrompe una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="99519-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="99519-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99519-110">EXAMPLES</span></span>

### <span data-ttu-id="99519-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99519-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="99519-112">Questo comando interrompe una sessione di scintilla di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="99519-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="99519-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="99519-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="99519-114">Questo comando interrompe una sessione di Spark analisi sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="99519-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="99519-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="99519-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="99519-116">Questo comando interrompe una sessione di Spark analisi sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="99519-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="99519-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99519-117">PARAMETERS</span></span>

### <span data-ttu-id="99519-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99519-118">-AsJob</span></span>
<span data-ttu-id="99519-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="99519-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99519-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99519-120">-DefaultProfile</span></span>
<span data-ttu-id="99519-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99519-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99519-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99519-122">-InputObject</span></span>
<span data-ttu-id="99519-123">Oggetto di input della sessione Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="99519-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="99519-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="99519-124">-LivyId</span></span>
<span data-ttu-id="99519-125">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="99519-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="99519-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99519-126">-PassThru</span></span>
<span data-ttu-id="99519-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="99519-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="99519-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="99519-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="99519-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="99519-129">-SparkPoolName</span></span>
<span data-ttu-id="99519-130">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="99519-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="99519-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="99519-131">-SparkPoolObject</span></span>
<span data-ttu-id="99519-132">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="99519-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="99519-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99519-133">-WorkspaceName</span></span>
<span data-ttu-id="99519-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="99519-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="99519-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99519-135">-Confirm</span></span>
<span data-ttu-id="99519-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99519-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99519-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99519-137">-WhatIf</span></span>
<span data-ttu-id="99519-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99519-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99519-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99519-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99519-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99519-140">CommonParameters</span></span>
<span data-ttu-id="99519-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99519-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99519-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99519-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99519-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99519-143">INPUTS</span></span>

### <span data-ttu-id="99519-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="99519-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="99519-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="99519-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="99519-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99519-146">OUTPUTS</span></span>

### <span data-ttu-id="99519-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99519-147">System.Boolean</span></span>

## <span data-ttu-id="99519-148">Note</span><span class="sxs-lookup"><span data-stu-id="99519-148">NOTES</span></span>

## <span data-ttu-id="99519-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99519-149">RELATED LINKS</span></span>
