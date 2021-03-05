---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973710"
---
# <span data-ttu-id="41ef9-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="41ef9-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="41ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="41ef9-103">Reimposta il timeout di una sessione di Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="41ef9-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="41ef9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41ef9-104">SYNTAX</span></span>

### <span data-ttu-id="41ef9-105">ResetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41ef9-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ef9-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ef9-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41ef9-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ef9-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ef9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41ef9-108">DESCRIPTION</span></span>
<span data-ttu-id="41ef9-109">Il cmdlet **Remove-AzSynapseSparkSessionTimeout** reimposta il timeout di una sessione di Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="41ef9-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="41ef9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41ef9-110">EXAMPLES</span></span>

### <span data-ttu-id="41ef9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41ef9-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="41ef9-112">Questo comando reimposta il timeout della sessione di Synapse Analytics Spark con l'ID livy specificato.</span><span class="sxs-lookup"><span data-stu-id="41ef9-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="41ef9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="41ef9-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="41ef9-114">Questo comando reimposta il timeout della sessione di Synapse Analytics Spark con l'ID flusso specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="41ef9-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="41ef9-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="41ef9-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="41ef9-116">Questo comando reimposta il timeout della sessione di Synapse Analytics Spark con l'ID flusso specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="41ef9-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="41ef9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41ef9-117">PARAMETERS</span></span>

### <span data-ttu-id="41ef9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41ef9-118">-AsJob</span></span>
<span data-ttu-id="41ef9-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41ef9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41ef9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ef9-120">-DefaultProfile</span></span>
<span data-ttu-id="41ef9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41ef9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41ef9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41ef9-122">-InputObject</span></span>
<span data-ttu-id="41ef9-123">Oggetto di input della sessione Spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="41ef9-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="41ef9-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="41ef9-124">-LivyId</span></span>
<span data-ttu-id="41ef9-125">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="41ef9-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="41ef9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41ef9-126">-PassThru</span></span>
<span data-ttu-id="41ef9-127">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="41ef9-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="41ef9-128">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="41ef9-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="41ef9-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="41ef9-129">-SparkPoolName</span></span>
<span data-ttu-id="41ef9-130">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="41ef9-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="41ef9-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="41ef9-131">-SparkPoolObject</span></span>
<span data-ttu-id="41ef9-132">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="41ef9-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="41ef9-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="41ef9-133">-WorkspaceName</span></span>
<span data-ttu-id="41ef9-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="41ef9-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="41ef9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41ef9-135">-Confirm</span></span>
<span data-ttu-id="41ef9-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41ef9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ef9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ef9-137">-WhatIf</span></span>
<span data-ttu-id="41ef9-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41ef9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41ef9-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41ef9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ef9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ef9-140">CommonParameters</span></span>
<span data-ttu-id="41ef9-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ef9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ef9-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41ef9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ef9-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="41ef9-143">INPUTS</span></span>

### <span data-ttu-id="41ef9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="41ef9-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="41ef9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="41ef9-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="41ef9-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41ef9-146">OUTPUTS</span></span>

### <span data-ttu-id="41ef9-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41ef9-147">System.Boolean</span></span>

## <span data-ttu-id="41ef9-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="41ef9-148">NOTES</span></span>

## <span data-ttu-id="41ef9-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41ef9-149">RELATED LINKS</span></span>
