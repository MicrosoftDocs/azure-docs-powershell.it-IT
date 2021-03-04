---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: efe733250c43d79aa8296db380ac453d44231c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011310"
---
# <span data-ttu-id="feed8-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="feed8-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="feed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feed8-102">SYNOPSIS</span></span>
<span data-ttu-id="feed8-103">Ottiene una sessione synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="feed8-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="feed8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="feed8-104">SYNTAX</span></span>

### <span data-ttu-id="feed8-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="feed8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feed8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feed8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feed8-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="feed8-107">DESCRIPTION</span></span>
<span data-ttu-id="feed8-108">Il cmdlet **Get-AzSynapseSparkSession** ottiene informazioni su una sessione di Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="feed8-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="feed8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="feed8-109">EXAMPLES</span></span>

### <span data-ttu-id="feed8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="feed8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="feed8-111">Questo comando recupera tutte le sessioni Spark nel pool di grafici spark specificato.</span><span class="sxs-lookup"><span data-stu-id="feed8-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="feed8-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="feed8-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="feed8-113">Questo comando recupera la sessione di Spark con l'ID del livy specificato.</span><span class="sxs-lookup"><span data-stu-id="feed8-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="feed8-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="feed8-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="feed8-115">Questo comando recupera tutte le sessioni spark nel pool spark specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="feed8-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="feed8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feed8-116">PARAMETERS</span></span>

### <span data-ttu-id="feed8-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="feed8-117">-ApplicationId</span></span>
<span data-ttu-id="feed8-118">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="feed8-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="feed8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feed8-119">-DefaultProfile</span></span>
<span data-ttu-id="feed8-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="feed8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feed8-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="feed8-121">-LivyId</span></span>
<span data-ttu-id="feed8-122">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="feed8-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="feed8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="feed8-123">-Name</span></span>
<span data-ttu-id="feed8-124">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="feed8-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="feed8-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="feed8-125">-SparkPoolName</span></span>
<span data-ttu-id="feed8-126">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="feed8-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feed8-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="feed8-127">-SparkPoolObject</span></span>
<span data-ttu-id="feed8-128">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="feed8-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feed8-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="feed8-129">-WorkspaceName</span></span>
<span data-ttu-id="feed8-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="feed8-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feed8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feed8-131">CommonParameters</span></span>
<span data-ttu-id="feed8-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feed8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feed8-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="feed8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feed8-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="feed8-134">INPUTS</span></span>

### <span data-ttu-id="feed8-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="feed8-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="feed8-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="feed8-136">OUTPUTS</span></span>

### <span data-ttu-id="feed8-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="feed8-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="feed8-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="feed8-138">NOTES</span></span>

## <span data-ttu-id="feed8-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="feed8-139">RELATED LINKS</span></span>
