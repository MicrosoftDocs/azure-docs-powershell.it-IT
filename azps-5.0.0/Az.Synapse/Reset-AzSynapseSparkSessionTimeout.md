---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202749"
---
# <span data-ttu-id="ccc6d-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="ccc6d-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="ccc6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc6d-103">Reimposta il timeout di una sessione di scintilla di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ccc6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccc6d-104">SYNTAX</span></span>

### <span data-ttu-id="ccc6d-105">ResetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccc6d-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccc6d-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc6d-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccc6d-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc6d-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccc6d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccc6d-108">DESCRIPTION</span></span>
<span data-ttu-id="ccc6d-109">Il cmdlet **Remove-AzSynapseSparkSessionTimeout** Reimposta il timeout di una sessione di Spark di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="ccc6d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccc6d-110">EXAMPLES</span></span>

### <span data-ttu-id="ccc6d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ccc6d-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="ccc6d-112">Questo comando Reimposta il timeout della sessione di Spark Analytics con l'ID Livio specificato.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="ccc6d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ccc6d-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="ccc6d-114">Questo comando Reimposta il timeout della sessione di Spark Analytics con l'ID Livio specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="ccc6d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ccc6d-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="ccc6d-116">Questo comando Reimposta il timeout della sessione di Spark Analytics con l'ID Livio specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="ccc6d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccc6d-117">PARAMETERS</span></span>

### <span data-ttu-id="ccc6d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccc6d-118">-AsJob</span></span>
<span data-ttu-id="ccc6d-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ccc6d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccc6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc6d-120">-DefaultProfile</span></span>
<span data-ttu-id="ccc6d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccc6d-122">-InputObject</span></span>
<span data-ttu-id="ccc6d-123">Oggetto di input della sessione Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc6d-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="ccc6d-124">-LivyId</span></span>
<span data-ttu-id="ccc6d-125">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc6d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccc6d-126">-PassThru</span></span>
<span data-ttu-id="ccc6d-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ccc6d-128">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ccc6d-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="ccc6d-129">-SparkPoolName</span></span>
<span data-ttu-id="ccc6d-130">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc6d-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="ccc6d-131">-SparkPoolObject</span></span>
<span data-ttu-id="ccc6d-132">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc6d-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ccc6d-133">-WorkspaceName</span></span>
<span data-ttu-id="ccc6d-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc6d-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccc6d-135">-Confirm</span></span>
<span data-ttu-id="ccc6d-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccc6d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccc6d-137">-WhatIf</span></span>
<span data-ttu-id="ccc6d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccc6d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccc6d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc6d-140">CommonParameters</span></span>
<span data-ttu-id="ccc6d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc6d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc6d-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccc6d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc6d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccc6d-143">INPUTS</span></span>

### <span data-ttu-id="ccc6d-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ccc6d-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="ccc6d-145">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="ccc6d-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="ccc6d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccc6d-146">OUTPUTS</span></span>

### <span data-ttu-id="ccc6d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccc6d-147">System.Boolean</span></span>

## <span data-ttu-id="ccc6d-148">Note</span><span class="sxs-lookup"><span data-stu-id="ccc6d-148">NOTES</span></span>

## <span data-ttu-id="ccc6d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccc6d-149">RELATED LINKS</span></span>
