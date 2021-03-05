---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: ea330bad812c7718d464a2ee237aa8c20c1f653f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992150"
---
# <span data-ttu-id="c8c13-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="c8c13-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="c8c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c13-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c13-103">Ottiene un processo Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="c8c13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8c13-104">SYNTAX</span></span>

### <span data-ttu-id="c8c13-105">GetSparkJobsByIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8c13-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8c13-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c13-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c13-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8c13-107">DESCRIPTION</span></span>
<span data-ttu-id="c8c13-108">Il cmdlet **Get-AzSynapseSparkJob** ottiene un processo di Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="c8c13-109">Se non si specifica alcun processo, questo cmdlet ottiene tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="c8c13-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="c8c13-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8c13-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c13-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8c13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="c8c13-112">Questo comando recupera tutti i processi in un pool Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="c8c13-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c8c13-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="c8c13-114">Questo comando recupera il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="c8c13-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="c8c13-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c8c13-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="c8c13-116">Questo comando recupera il processo con l'ID applicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c8c13-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="c8c13-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c8c13-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="c8c13-118">Questo comando recupera tutti i processi in un pool Spark tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8c13-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="c8c13-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c13-119">PARAMETERS</span></span>

### <span data-ttu-id="c8c13-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c8c13-120">-ApplicationId</span></span>
<span data-ttu-id="c8c13-121">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="c8c13-121">The Application identifier of the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c13-122">-DefaultProfile</span></span>
<span data-ttu-id="c8c13-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c13-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c13-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="c8c13-124">-LivyId</span></span>
<span data-ttu-id="c8c13-125">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c8c13-126">-Name</span></span>
<span data-ttu-id="c8c13-127">Nome del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-127">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c8c13-128">-SparkPoolName</span></span>
<span data-ttu-id="c8c13-129">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="c8c13-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="c8c13-130">-SparkPoolObject</span></span>
<span data-ttu-id="c8c13-131">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8c13-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8c13-132">-WorkspaceName</span></span>
<span data-ttu-id="c8c13-133">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8c13-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c13-134">CommonParameters</span></span>
<span data-ttu-id="c8c13-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c13-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8c13-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c13-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8c13-137">INPUTS</span></span>

### <span data-ttu-id="c8c13-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c8c13-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c8c13-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8c13-139">OUTPUTS</span></span>

### <span data-ttu-id="c8c13-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="c8c13-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="c8c13-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8c13-141">NOTES</span></span>

## <span data-ttu-id="c8c13-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8c13-142">RELATED LINKS</span></span>
