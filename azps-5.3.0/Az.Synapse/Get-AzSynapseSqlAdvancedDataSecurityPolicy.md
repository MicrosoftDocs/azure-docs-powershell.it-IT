---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383935"
---
# <span data-ttu-id="3871c-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="3871c-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="3871c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3871c-102">SYNOPSIS</span></span>
<span data-ttu-id="3871c-103">Ottiene i criteri avanzati per la sicurezza dei dati di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3871c-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="3871c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3871c-104">SYNTAX</span></span>

### <span data-ttu-id="3871c-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3871c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3871c-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3871c-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3871c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3871c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3871c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3871c-108">DESCRIPTION</span></span>
<span data-ttu-id="3871c-109">Il cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** recupera i criteri avanzati per la sicurezza dei dati di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3871c-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="3871c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3871c-110">EXAMPLES</span></span>

### <span data-ttu-id="3871c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3871c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3871c-112">Questo comando consente di ottenere la sicurezza dei dati avanzata nell'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3871c-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3871c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3871c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="3871c-114">Questo comando consente di ottenere la sicurezza dei dati avanzata nell'area di lavoro denominata ContosoWorkspace tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="3871c-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="3871c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3871c-115">PARAMETERS</span></span>

### <span data-ttu-id="3871c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3871c-116">-DefaultProfile</span></span>
<span data-ttu-id="3871c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3871c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3871c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3871c-118">-InputObject</span></span>
<span data-ttu-id="3871c-119">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="3871c-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3871c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3871c-120">-ResourceGroupName</span></span>
<span data-ttu-id="3871c-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3871c-121">Resource group name.</span></span>

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

### <span data-ttu-id="3871c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3871c-122">-ResourceId</span></span>
<span data-ttu-id="3871c-123">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3871c-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="3871c-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3871c-124">-WorkspaceName</span></span>
<span data-ttu-id="3871c-125">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="3871c-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3871c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3871c-126">CommonParameters</span></span>
<span data-ttu-id="3871c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3871c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3871c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3871c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3871c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3871c-129">INPUTS</span></span>

### <span data-ttu-id="3871c-130">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3871c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3871c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3871c-131">OUTPUTS</span></span>

### <span data-ttu-id="3871c-132">Microsoft. Azure. Commands. sinapsi. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="3871c-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="3871c-133">Note</span><span class="sxs-lookup"><span data-stu-id="3871c-133">NOTES</span></span>

## <span data-ttu-id="3871c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3871c-134">RELATED LINKS</span></span>
