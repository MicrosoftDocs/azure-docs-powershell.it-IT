---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383977"
---
# <span data-ttu-id="bb91e-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="bb91e-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="bb91e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb91e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb91e-103">Ottiene una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="bb91e-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="bb91e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb91e-104">SYNTAX</span></span>

### <span data-ttu-id="bb91e-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb91e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb91e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb91e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb91e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb91e-107">DESCRIPTION</span></span>
<span data-ttu-id="bb91e-108">Il cmdlet **Get-AzSynapseSparkSession** ottiene le informazioni su una sessione di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="bb91e-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="bb91e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb91e-109">EXAMPLES</span></span>

### <span data-ttu-id="bb91e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb91e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="bb91e-111">Questo comando consente di ottenere tutte le sessioni Spark sotto il pool di scintille specificato.</span><span class="sxs-lookup"><span data-stu-id="bb91e-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="bb91e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bb91e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="bb91e-113">Questo comando consente di ottenere la sessione Spark con l'ID Livio specificato.</span><span class="sxs-lookup"><span data-stu-id="bb91e-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="bb91e-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="bb91e-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="bb91e-115">Questo comando consente di ottenere tutte le sessioni Spark sotto il pool di scintille specificato tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb91e-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="bb91e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb91e-116">PARAMETERS</span></span>

### <span data-ttu-id="bb91e-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bb91e-117">-ApplicationId</span></span>
<span data-ttu-id="bb91e-118">Identificatore dell'applicazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="bb91e-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="bb91e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb91e-119">-DefaultProfile</span></span>
<span data-ttu-id="bb91e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb91e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb91e-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="bb91e-121">-LivyId</span></span>
<span data-ttu-id="bb91e-122">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="bb91e-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="bb91e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb91e-123">-Name</span></span>
<span data-ttu-id="bb91e-124">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="bb91e-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="bb91e-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="bb91e-125">-SparkPoolName</span></span>
<span data-ttu-id="bb91e-126">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="bb91e-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="bb91e-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="bb91e-127">-SparkPoolObject</span></span>
<span data-ttu-id="bb91e-128">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb91e-128">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="bb91e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bb91e-129">-WorkspaceName</span></span>
<span data-ttu-id="bb91e-130">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="bb91e-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bb91e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb91e-131">CommonParameters</span></span>
<span data-ttu-id="bb91e-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb91e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb91e-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb91e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb91e-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb91e-134">INPUTS</span></span>

### <span data-ttu-id="bb91e-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="bb91e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="bb91e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb91e-136">OUTPUTS</span></span>

### <span data-ttu-id="bb91e-137">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="bb91e-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="bb91e-138">Note</span><span class="sxs-lookup"><span data-stu-id="bb91e-138">NOTES</span></span>

## <span data-ttu-id="bb91e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb91e-139">RELATED LINKS</span></span>
