---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198398"
---
# <span data-ttu-id="278c9-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="278c9-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="278c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278c9-102">SYNOPSIS</span></span>
<span data-ttu-id="278c9-103">Ottiene i criteri di Sicurezza avanzata dei dati di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="278c9-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="278c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="278c9-104">SYNTAX</span></span>

### <span data-ttu-id="278c9-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="278c9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278c9-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="278c9-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="278c9-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="278c9-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="278c9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="278c9-108">DESCRIPTION</span></span>
<span data-ttu-id="278c9-109">Il cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** recupera i criteri di Advanced Data Security di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="278c9-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="278c9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="278c9-110">EXAMPLES</span></span>

### <span data-ttu-id="278c9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="278c9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="278c9-112">Questo comando recupera Advanced Data Security nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="278c9-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="278c9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="278c9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="278c9-114">Questo comando recupera Advanced Data Security nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="278c9-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="278c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="278c9-115">PARAMETERS</span></span>

### <span data-ttu-id="278c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278c9-116">-DefaultProfile</span></span>
<span data-ttu-id="278c9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="278c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278c9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="278c9-118">-InputObject</span></span>
<span data-ttu-id="278c9-119">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="278c9-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="278c9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278c9-120">-ResourceGroupName</span></span>
<span data-ttu-id="278c9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="278c9-121">Resource group name.</span></span>

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

### <span data-ttu-id="278c9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="278c9-122">-ResourceId</span></span>
<span data-ttu-id="278c9-123">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="278c9-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="278c9-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="278c9-124">-WorkspaceName</span></span>
<span data-ttu-id="278c9-125">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="278c9-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="278c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278c9-126">CommonParameters</span></span>
<span data-ttu-id="278c9-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="278c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278c9-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="278c9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278c9-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="278c9-129">INPUTS</span></span>

### <span data-ttu-id="278c9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="278c9-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="278c9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="278c9-131">OUTPUTS</span></span>

### <span data-ttu-id="278c9-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="278c9-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="278c9-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="278c9-133">NOTES</span></span>

## <span data-ttu-id="278c9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="278c9-134">RELATED LINKS</span></span>
