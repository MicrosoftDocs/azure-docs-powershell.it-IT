---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195615"
---
# <span data-ttu-id="2cdae-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="2cdae-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="2cdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cdae-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdae-103">Recupera le impostazioni di controllo di un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2cdae-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2cdae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cdae-104">SYNTAX</span></span>

### <span data-ttu-id="2cdae-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cdae-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdae-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdae-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdae-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdae-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cdae-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cdae-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cdae-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cdae-109">DESCRIPTION</span></span>
<span data-ttu-id="2cdae-110">Il cmdlet **Get-AzSynapseSqlPoolAuditSetting** ottiene le impostazioni di controllo di un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2cdae-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2cdae-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cdae-111">EXAMPLES</span></span>

### <span data-ttu-id="2cdae-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cdae-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2cdae-113">Questo comando recupera le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2cdae-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2cdae-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2cdae-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="2cdae-115">Questo comando recupera le impostazioni di controllo di un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cdae-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2cdae-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cdae-116">PARAMETERS</span></span>

### <span data-ttu-id="2cdae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdae-117">-DefaultProfile</span></span>
<span data-ttu-id="2cdae-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cdae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cdae-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cdae-119">-InputObject</span></span>
<span data-ttu-id="2cdae-120">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cdae-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2cdae-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2cdae-121">-Name</span></span>
<span data-ttu-id="2cdae-122">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2cdae-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="2cdae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdae-123">-ResourceGroupName</span></span>
<span data-ttu-id="2cdae-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2cdae-124">Resource group name.</span></span>

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

### <span data-ttu-id="2cdae-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cdae-125">-ResourceId</span></span>
<span data-ttu-id="2cdae-126">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="2cdae-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="2cdae-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2cdae-127">-WorkspaceName</span></span>
<span data-ttu-id="2cdae-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="2cdae-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2cdae-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2cdae-129">-WorkspaceObject</span></span>
<span data-ttu-id="2cdae-130">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cdae-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2cdae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdae-131">CommonParameters</span></span>
<span data-ttu-id="2cdae-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdae-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2cdae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdae-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cdae-134">INPUTS</span></span>

### <span data-ttu-id="2cdae-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2cdae-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2cdae-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2cdae-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2cdae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cdae-137">OUTPUTS</span></span>

### <span data-ttu-id="2cdae-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="2cdae-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="2cdae-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cdae-139">NOTES</span></span>

## <span data-ttu-id="2cdae-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cdae-140">RELATED LINKS</span></span>
