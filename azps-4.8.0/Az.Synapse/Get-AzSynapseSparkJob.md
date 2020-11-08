---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191123"
---
# <span data-ttu-id="082e8-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="082e8-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="082e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="082e8-102">SYNOPSIS</span></span>
<span data-ttu-id="082e8-103">Ottiene un processo Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="082e8-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="082e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="082e8-104">SYNTAX</span></span>

### <span data-ttu-id="082e8-105">GetSparkJobsByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="082e8-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="082e8-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="082e8-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="082e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="082e8-107">DESCRIPTION</span></span>
<span data-ttu-id="082e8-108">Il cmdlet **Get-AzSynapseSparkJob** ottiene un processo Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="082e8-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="082e8-109">Se non specifichi un processo, questo cmdlet ottiene tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="082e8-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="082e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="082e8-110">EXAMPLES</span></span>

### <span data-ttu-id="082e8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="082e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="082e8-112">Questo comando consente di ottenere tutti i processi in un pool di scintille.</span><span class="sxs-lookup"><span data-stu-id="082e8-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="082e8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="082e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="082e8-114">Questo comando ottiene il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="082e8-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="082e8-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="082e8-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="082e8-116">Questo comando ottiene il processo con l'ID applicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="082e8-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="082e8-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="082e8-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="082e8-118">Questo comando consente di ottenere tutti i processi sotto un pool di scintille tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="082e8-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="082e8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="082e8-119">PARAMETERS</span></span>

### <span data-ttu-id="082e8-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="082e8-120">-ApplicationId</span></span>
<span data-ttu-id="082e8-121">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="082e8-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="082e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082e8-122">-DefaultProfile</span></span>
<span data-ttu-id="082e8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="082e8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="082e8-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="082e8-124">-LivyId</span></span>
<span data-ttu-id="082e8-125">Identificatore del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="082e8-125">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="082e8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="082e8-126">-Name</span></span>
<span data-ttu-id="082e8-127">Nome del processo Spark.</span><span class="sxs-lookup"><span data-stu-id="082e8-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="082e8-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="082e8-128">-SparkPoolName</span></span>
<span data-ttu-id="082e8-129">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="082e8-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="082e8-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="082e8-130">-SparkPoolObject</span></span>
<span data-ttu-id="082e8-131">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="082e8-131">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="082e8-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="082e8-132">-WorkspaceName</span></span>
<span data-ttu-id="082e8-133">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="082e8-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="082e8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082e8-134">CommonParameters</span></span>
<span data-ttu-id="082e8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082e8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082e8-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="082e8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082e8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="082e8-137">INPUTS</span></span>

### <span data-ttu-id="082e8-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="082e8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="082e8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="082e8-139">OUTPUTS</span></span>

### <span data-ttu-id="082e8-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="082e8-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="082e8-141">Note</span><span class="sxs-lookup"><span data-stu-id="082e8-141">NOTES</span></span>

## <span data-ttu-id="082e8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="082e8-142">RELATED LINKS</span></span>
