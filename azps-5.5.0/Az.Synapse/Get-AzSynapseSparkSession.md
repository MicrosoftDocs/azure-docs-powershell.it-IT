---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209051"
---
# <span data-ttu-id="dbfb4-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="dbfb4-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="dbfb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbfb4-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfb4-103">Ottiene una sessione synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="dbfb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbfb4-104">SYNTAX</span></span>

### <span data-ttu-id="dbfb4-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dbfb4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbfb4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbfb4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbfb4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbfb4-107">DESCRIPTION</span></span>
<span data-ttu-id="dbfb4-108">Il cmdlet **Get-AzSynapseSparkSession** ottiene informazioni su una sessione di Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="dbfb4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbfb4-109">EXAMPLES</span></span>

### <span data-ttu-id="dbfb4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbfb4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="dbfb4-111">Questo comando recupera tutte le sessioni Spark nel pool di grafici spark specificato.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="dbfb4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dbfb4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="dbfb4-113">Questo comando recupera la sessione di Spark con l'ID del livy specificato.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="dbfb4-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dbfb4-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="dbfb4-115">Questo comando recupera tutte le sessioni spark nel pool spark specificato tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="dbfb4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbfb4-116">PARAMETERS</span></span>

### <span data-ttu-id="dbfb4-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dbfb4-117">-ApplicationId</span></span>
<span data-ttu-id="dbfb4-118">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="dbfb4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfb4-119">-DefaultProfile</span></span>
<span data-ttu-id="dbfb4-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbfb4-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="dbfb4-121">-LivyId</span></span>
<span data-ttu-id="dbfb4-122">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="dbfb4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dbfb4-123">-Name</span></span>
<span data-ttu-id="dbfb4-124">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="dbfb4-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="dbfb4-125">-SparkPoolName</span></span>
<span data-ttu-id="dbfb4-126">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="dbfb4-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="dbfb4-127">-SparkPoolObject</span></span>
<span data-ttu-id="dbfb4-128">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dbfb4-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbfb4-129">-WorkspaceName</span></span>
<span data-ttu-id="dbfb4-130">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dbfb4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfb4-131">CommonParameters</span></span>
<span data-ttu-id="dbfb4-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfb4-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfb4-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbfb4-134">INPUTS</span></span>

### <span data-ttu-id="dbfb4-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="dbfb4-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="dbfb4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbfb4-136">OUTPUTS</span></span>

### <span data-ttu-id="dbfb4-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="dbfb4-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="dbfb4-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbfb4-138">NOTES</span></span>

## <span data-ttu-id="dbfb4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbfb4-139">RELATED LINKS</span></span>
