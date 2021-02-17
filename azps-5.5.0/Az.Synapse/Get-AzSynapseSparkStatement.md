---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182783"
---
# <span data-ttu-id="0cc71-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="0cc71-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="0cc71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cc71-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc71-103">Ottiene un'istruzione Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="0cc71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cc71-104">SYNTAX</span></span>

### <span data-ttu-id="0cc71-105">GetSparkStatementsByIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0cc71-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc71-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cc71-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc71-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0cc71-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc71-108">Il cmdlet **Get-AzSynapseSparkStatement** ottiene informazioni su un'istruzione Azure Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="0cc71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cc71-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc71-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0cc71-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="0cc71-111">Questo comando recupera tutte le istruzioni Spark in una sessione Spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="0cc71-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0cc71-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="0cc71-113">Questo comando recupera l'istruzione Spark con l'ID livy specificato.</span><span class="sxs-lookup"><span data-stu-id="0cc71-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="0cc71-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0cc71-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="0cc71-115">Questo comando recupera tutte le istruzioni Spark in una sessione Spark tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cc71-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="0cc71-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cc71-116">PARAMETERS</span></span>

### <span data-ttu-id="0cc71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc71-117">-DefaultProfile</span></span>
<span data-ttu-id="0cc71-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0cc71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cc71-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="0cc71-119">-LivyId</span></span>
<span data-ttu-id="0cc71-120">Identificatore dell'istruzione Spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="0cc71-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="0cc71-121">-SessionId</span></span>
<span data-ttu-id="0cc71-122">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="0cc71-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="0cc71-123">-SessionObject</span></span>
<span data-ttu-id="0cc71-124">Oggetto di input del pool spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0cc71-124">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0cc71-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="0cc71-125">-SparkPoolName</span></span>
<span data-ttu-id="0cc71-126">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="0cc71-126">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="0cc71-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0cc71-127">-WorkspaceName</span></span>
<span data-ttu-id="0cc71-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="0cc71-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0cc71-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc71-129">CommonParameters</span></span>
<span data-ttu-id="0cc71-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc71-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc71-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0cc71-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc71-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="0cc71-132">INPUTS</span></span>

### <span data-ttu-id="0cc71-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="0cc71-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="0cc71-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cc71-134">OUTPUTS</span></span>

### <span data-ttu-id="0cc71-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="0cc71-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="0cc71-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="0cc71-136">NOTES</span></span>

## <span data-ttu-id="0cc71-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cc71-137">RELATED LINKS</span></span>
