---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015694"
---
# <span data-ttu-id="a2c69-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a2c69-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a2c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c69-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c69-103">Recupera le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2c69-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a2c69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2c69-104">SYNTAX</span></span>

### <span data-ttu-id="a2c69-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2c69-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2c69-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c69-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c69-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c69-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2c69-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2c69-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c69-109">Il cmdlet **Get-AzSynapseSqlAuditSetting** ottiene le impostazioni di controllo di un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2c69-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a2c69-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2c69-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c69-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2c69-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a2c69-112">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a2c69-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a2c69-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a2c69-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="a2c69-114">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2c69-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a2c69-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c69-115">PARAMETERS</span></span>

### <span data-ttu-id="a2c69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c69-116">-DefaultProfile</span></span>
<span data-ttu-id="a2c69-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c69-118">-InputObject</span></span>
<span data-ttu-id="a2c69-119">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2c69-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c69-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2c69-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2c69-121">Resource group name.</span></span>

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

### <span data-ttu-id="a2c69-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c69-122">-ResourceId</span></span>
<span data-ttu-id="a2c69-123">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2c69-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2c69-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2c69-124">-WorkspaceName</span></span>
<span data-ttu-id="a2c69-125">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2c69-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2c69-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c69-126">CommonParameters</span></span>
<span data-ttu-id="a2c69-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c69-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c69-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2c69-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c69-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2c69-129">INPUTS</span></span>

### <span data-ttu-id="a2c69-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2c69-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a2c69-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2c69-131">OUTPUTS</span></span>

### <span data-ttu-id="a2c69-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="a2c69-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="a2c69-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2c69-133">NOTES</span></span>

## <span data-ttu-id="a2c69-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2c69-134">RELATED LINKS</span></span>
