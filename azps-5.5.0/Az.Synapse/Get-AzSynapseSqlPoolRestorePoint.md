---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207642"
---
# <span data-ttu-id="1c95a-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="1c95a-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="1c95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c95a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c95a-103">Recupera i diversi punti di ripristino da cui è possibile ripristinare un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c95a-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="1c95a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c95a-104">SYNTAX</span></span>

### <span data-ttu-id="1c95a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c95a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c95a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c95a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c95a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c95a-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c95a-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c95a-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c95a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c95a-109">DESCRIPTION</span></span>
<span data-ttu-id="1c95a-110">Il cmdlet **Get-AzSynapseSqlPoolRestorePoint** recupera i distinti punti di ripristino da cui è possibile ripristinare un SQL azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c95a-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="1c95a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c95a-111">EXAMPLES</span></span>

### <span data-ttu-id="1c95a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c95a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1c95a-113">Questo comando restituisce tutti i punti di ripristino disponibili per il pool di SQL Azure Synapse Analytics denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="1c95a-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="1c95a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c95a-114">PARAMETERS</span></span>

### <span data-ttu-id="1c95a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c95a-115">-DefaultProfile</span></span>
<span data-ttu-id="1c95a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c95a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c95a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c95a-117">-InputObject</span></span>
<span data-ttu-id="1c95a-118">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1c95a-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1c95a-119">-Name</span></span>
<span data-ttu-id="1c95a-120">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1c95a-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c95a-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c95a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c95a-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c95a-123">-ResourceId</span></span>
<span data-ttu-id="1c95a-124">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="1c95a-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c95a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c95a-125">-WorkspaceName</span></span>
<span data-ttu-id="1c95a-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="1c95a-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1c95a-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1c95a-127">-WorkspaceObject</span></span>
<span data-ttu-id="1c95a-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="1c95a-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c95a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c95a-129">CommonParameters</span></span>
<span data-ttu-id="1c95a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c95a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c95a-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c95a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c95a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c95a-132">INPUTS</span></span>

### <span data-ttu-id="1c95a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1c95a-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1c95a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1c95a-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1c95a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c95a-135">OUTPUTS</span></span>

### <span data-ttu-id="1c95a-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="1c95a-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="1c95a-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c95a-137">NOTES</span></span>

## <span data-ttu-id="1c95a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c95a-138">RELATED LINKS</span></span>
