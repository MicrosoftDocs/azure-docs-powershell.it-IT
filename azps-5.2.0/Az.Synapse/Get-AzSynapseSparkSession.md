---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359449"
---
# <span data-ttu-id="3cf14-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3cf14-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="3cf14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cf14-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf14-103">Ottiene una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3cf14-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3cf14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cf14-104">SYNTAX</span></span>

### <span data-ttu-id="3cf14-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cf14-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cf14-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf14-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cf14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cf14-107">DESCRIPTION</span></span>
<span data-ttu-id="3cf14-108">Il cmdlet **Get-AzSynapseSparkSession** ottiene le informazioni su una sessione di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3cf14-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3cf14-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cf14-109">EXAMPLES</span></span>

### <span data-ttu-id="3cf14-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cf14-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="3cf14-111">Questo comando consente di ottenere tutte le sessioni Spark sotto il pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="3cf14-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="3cf14-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3cf14-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="3cf14-113">Questo comando consente di ottenere la sessione Spark con l'ID Livio specificato.</span><span class="sxs-lookup"><span data-stu-id="3cf14-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="3cf14-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3cf14-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="3cf14-115">Questo comando consente di ottenere tutte le sessioni Spark sotto il pool di scintille specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cf14-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="3cf14-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cf14-116">PARAMETERS</span></span>

### <span data-ttu-id="3cf14-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3cf14-117">-ApplicationId</span></span>
<span data-ttu-id="3cf14-118">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="3cf14-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="3cf14-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf14-119">-DefaultProfile</span></span>
<span data-ttu-id="3cf14-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf14-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf14-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3cf14-121">-LivyId</span></span>
<span data-ttu-id="3cf14-122">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="3cf14-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="3cf14-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cf14-123">-Name</span></span>
<span data-ttu-id="3cf14-124">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3cf14-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="3cf14-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3cf14-125">-SparkPoolName</span></span>
<span data-ttu-id="3cf14-126">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3cf14-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="3cf14-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3cf14-127">-SparkPoolObject</span></span>
<span data-ttu-id="3cf14-128">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cf14-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3cf14-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3cf14-129">-WorkspaceName</span></span>
<span data-ttu-id="3cf14-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3cf14-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3cf14-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf14-131">CommonParameters</span></span>
<span data-ttu-id="3cf14-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf14-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf14-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cf14-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf14-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cf14-134">INPUTS</span></span>

### <span data-ttu-id="3cf14-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3cf14-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="3cf14-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cf14-136">OUTPUTS</span></span>

### <span data-ttu-id="3cf14-137">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3cf14-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3cf14-138">Note</span><span class="sxs-lookup"><span data-stu-id="3cf14-138">NOTES</span></span>

## <span data-ttu-id="3cf14-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cf14-139">RELATED LINKS</span></span>
