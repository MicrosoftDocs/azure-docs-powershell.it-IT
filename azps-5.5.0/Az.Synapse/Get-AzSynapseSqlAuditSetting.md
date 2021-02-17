---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207650"
---
# <span data-ttu-id="a931c-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a931c-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="a931c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a931c-102">SYNOPSIS</span></span>
<span data-ttu-id="a931c-103">Recupera le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a931c-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a931c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a931c-104">SYNTAX</span></span>

### <span data-ttu-id="a931c-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a931c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a931c-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a931c-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a931c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a931c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a931c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a931c-108">DESCRIPTION</span></span>
<span data-ttu-id="a931c-109">Il cmdlet **Get-AzSynapseSqlAuditSetting** ottiene le impostazioni di controllo di un'area di lavoro di analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="a931c-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="a931c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a931c-110">EXAMPLES</span></span>

### <span data-ttu-id="a931c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a931c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a931c-112">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a931c-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a931c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a931c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="a931c-114">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a931c-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a931c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a931c-115">PARAMETERS</span></span>

### <span data-ttu-id="a931c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a931c-116">-DefaultProfile</span></span>
<span data-ttu-id="a931c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a931c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a931c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a931c-118">-InputObject</span></span>
<span data-ttu-id="a931c-119">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a931c-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a931c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a931c-120">-ResourceGroupName</span></span>
<span data-ttu-id="a931c-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a931c-121">Resource group name.</span></span>

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

### <span data-ttu-id="a931c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a931c-122">-ResourceId</span></span>
<span data-ttu-id="a931c-123">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a931c-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a931c-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a931c-124">-WorkspaceName</span></span>
<span data-ttu-id="a931c-125">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a931c-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a931c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a931c-126">CommonParameters</span></span>
<span data-ttu-id="a931c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a931c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a931c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a931c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a931c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a931c-129">INPUTS</span></span>

### <span data-ttu-id="a931c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a931c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a931c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a931c-131">OUTPUTS</span></span>

### <span data-ttu-id="a931c-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="a931c-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="a931c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="a931c-133">NOTES</span></span>

## <span data-ttu-id="a931c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a931c-134">RELATED LINKS</span></span>
