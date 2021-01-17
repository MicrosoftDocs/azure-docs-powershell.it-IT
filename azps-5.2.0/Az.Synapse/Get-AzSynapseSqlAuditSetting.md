---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359421"
---
# <span data-ttu-id="09036-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="09036-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="09036-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09036-102">SYNOPSIS</span></span>
<span data-ttu-id="09036-103">Ottiene le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="09036-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="09036-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09036-104">SYNTAX</span></span>

### <span data-ttu-id="09036-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09036-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09036-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09036-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09036-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09036-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09036-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09036-108">DESCRIPTION</span></span>
<span data-ttu-id="09036-109">Il cmdlet **Get-AzSynapseSqlAuditSetting** ottiene le impostazioni di controllo di un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="09036-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="09036-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09036-110">EXAMPLES</span></span>

### <span data-ttu-id="09036-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09036-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="09036-112">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="09036-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="09036-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="09036-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="09036-114">Ottiene le impostazioni di controllo di un'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="09036-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="09036-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09036-115">PARAMETERS</span></span>

### <span data-ttu-id="09036-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09036-116">-DefaultProfile</span></span>
<span data-ttu-id="09036-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09036-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09036-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09036-118">-InputObject</span></span>
<span data-ttu-id="09036-119">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="09036-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09036-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09036-120">-ResourceGroupName</span></span>
<span data-ttu-id="09036-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09036-121">Resource group name.</span></span>

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

### <span data-ttu-id="09036-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09036-122">-ResourceId</span></span>
<span data-ttu-id="09036-123">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="09036-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="09036-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09036-124">-WorkspaceName</span></span>
<span data-ttu-id="09036-125">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="09036-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09036-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09036-126">CommonParameters</span></span>
<span data-ttu-id="09036-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09036-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09036-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09036-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09036-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09036-129">INPUTS</span></span>

### <span data-ttu-id="09036-130">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09036-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="09036-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09036-131">OUTPUTS</span></span>

### <span data-ttu-id="09036-132">Microsoft. Azure. Commands. sinapsi. Models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="09036-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="09036-133">Note</span><span class="sxs-lookup"><span data-stu-id="09036-133">NOTES</span></span>

## <span data-ttu-id="09036-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09036-134">RELATED LINKS</span></span>
