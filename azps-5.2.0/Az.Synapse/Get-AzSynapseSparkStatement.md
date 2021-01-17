---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359446"
---
# <span data-ttu-id="e3c8b-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e3c8b-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="e3c8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c8b-103">Ottiene un'istruzione Spark di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e3c8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c8b-104">SYNTAX</span></span>

### <span data-ttu-id="e3c8b-105">GetSparkStatementsByIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3c8b-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3c8b-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c8b-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3c8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="e3c8b-108">Il cmdlet **Get-AzSynapseSparkStatement** ottiene le informazioni su un'istruzione Spark di Azure sinapsi analitica.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e3c8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c8b-109">EXAMPLES</span></span>

### <span data-ttu-id="e3c8b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3c8b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="e3c8b-111">Questo comando ottiene tutte le istruzioni Spark in una sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="e3c8b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e3c8b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="e3c8b-113">Questo comando ottiene l'istruzione Spark con l'ID Livio specificato.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="e3c8b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e3c8b-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="e3c8b-115">Questo comando consente di ottenere tutte le istruzioni Spark in una sessione di Spark tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="e3c8b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3c8b-116">PARAMETERS</span></span>

### <span data-ttu-id="e3c8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c8b-117">-DefaultProfile</span></span>
<span data-ttu-id="e3c8b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c8b-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="e3c8b-119">-LivyId</span></span>
<span data-ttu-id="e3c8b-120">Identificatore dell'istruzione Spark.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="e3c8b-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="e3c8b-121">-SessionId</span></span>
<span data-ttu-id="e3c8b-122">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c8b-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="e3c8b-123">-SessionObject</span></span>
<span data-ttu-id="e3c8b-124">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c8b-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e3c8b-125">-SparkPoolName</span></span>
<span data-ttu-id="e3c8b-126">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c8b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e3c8b-127">-WorkspaceName</span></span>
<span data-ttu-id="e3c8b-128">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c8b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c8b-129">CommonParameters</span></span>
<span data-ttu-id="e3c8b-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c8b-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3c8b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c8b-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3c8b-132">INPUTS</span></span>

### <span data-ttu-id="e3c8b-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e3c8b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="e3c8b-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c8b-134">OUTPUTS</span></span>

### <span data-ttu-id="e3c8b-135">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e3c8b-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="e3c8b-136">Note</span><span class="sxs-lookup"><span data-stu-id="e3c8b-136">NOTES</span></span>

## <span data-ttu-id="e3c8b-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c8b-137">RELATED LINKS</span></span>
