---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195526"
---
# <span data-ttu-id="bbc2d-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="bbc2d-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="bbc2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc2d-103">Annulla un'istruzione Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbc2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbc2d-104">SYNTAX</span></span>

### <span data-ttu-id="bbc2d-105">StopSparkStatementByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbc2d-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc2d-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbc2d-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc2d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bbc2d-107">DESCRIPTION</span></span>
<span data-ttu-id="bbc2d-108">Il cmdlet **Stop-AzSynapseSparkStatement** annulla un'istruzione Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="bbc2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbc2d-109">EXAMPLES</span></span>

### <span data-ttu-id="bbc2d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bbc2d-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="bbc2d-111">Questo comando annulla l'istruzione Spark con l'ID riga specificato.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="bbc2d-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bbc2d-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="bbc2d-113">Questo comando annulla l'istruzione Spark con l'ID riga specificato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="bbc2d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbc2d-114">PARAMETERS</span></span>

### <span data-ttu-id="bbc2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc2d-115">-DefaultProfile</span></span>
<span data-ttu-id="bbc2d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc2d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bbc2d-117">-Force</span></span>
<span data-ttu-id="bbc2d-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bbc2d-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="bbc2d-119">-LivyId</span></span>
<span data-ttu-id="bbc2d-120">Identificatore dell'istruzione Spark.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc2d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbc2d-121">-PassThru</span></span>
<span data-ttu-id="bbc2d-122">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="bbc2d-123">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bbc2d-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="bbc2d-124">-SessionId</span></span>
<span data-ttu-id="bbc2d-125">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc2d-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="bbc2d-126">-SessionObject</span></span>
<span data-ttu-id="bbc2d-127">Oggetto di input della sessione Spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc2d-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="bbc2d-128">-SparkPoolName</span></span>
<span data-ttu-id="bbc2d-129">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc2d-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbc2d-130">-WorkspaceName</span></span>
<span data-ttu-id="bbc2d-131">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc2d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbc2d-132">-Confirm</span></span>
<span data-ttu-id="bbc2d-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc2d-134">-WhatIf</span></span>
<span data-ttu-id="bbc2d-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc2d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc2d-137">CommonParameters</span></span>
<span data-ttu-id="bbc2d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc2d-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbc2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc2d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="bbc2d-140">INPUTS</span></span>

### <span data-ttu-id="bbc2d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="bbc2d-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="bbc2d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbc2d-142">OUTPUTS</span></span>

### <span data-ttu-id="bbc2d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbc2d-143">System.Boolean</span></span>

## <span data-ttu-id="bbc2d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="bbc2d-144">NOTES</span></span>

## <span data-ttu-id="bbc2d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbc2d-145">RELATED LINKS</span></span>
