---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191121"
---
# <span data-ttu-id="a72c4-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a72c4-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a72c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a72c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a72c4-103">Ottiene un pool SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a72c4-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a72c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a72c4-104">SYNTAX</span></span>

### <span data-ttu-id="a72c4-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a72c4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72c4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a72c4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72c4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a72c4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a72c4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a72c4-108">DESCRIPTION</span></span>
<span data-ttu-id="a72c4-109">Il cmdlet **Get-AzSynapseSqlPool** ottiene le informazioni su un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a72c4-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a72c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a72c4-110">EXAMPLES</span></span>

### <span data-ttu-id="a72c4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a72c4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a72c4-112">Questo comando consente di ottenere tutti i pool SQL in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a72c4-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="a72c4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a72c4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a72c4-114">Questo comando consente di ottenere il pool SQL in area di lavoro ContosoWorkspace con nome ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a72c4-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="a72c4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a72c4-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="a72c4-116">Questo comando consente di ottenere tutti i pool SQL in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="a72c4-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="a72c4-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a72c4-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="a72c4-118">Questo comando consente di ottenere il pool SQL con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="a72c4-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="a72c4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a72c4-119">PARAMETERS</span></span>

### <span data-ttu-id="a72c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72c4-120">-DefaultProfile</span></span>
<span data-ttu-id="a72c4-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a72c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a72c4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a72c4-122">-Name</span></span>
<span data-ttu-id="a72c4-123">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="a72c4-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a72c4-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a72c4-125">Resource group name.</span></span>

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

### <span data-ttu-id="a72c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72c4-126">-ResourceId</span></span>
<span data-ttu-id="a72c4-127">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="a72c4-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a72c4-128">-Versione</span><span class="sxs-lookup"><span data-stu-id="a72c4-128">-Version</span></span>
<span data-ttu-id="a72c4-129">[Questa caratteristica è in un'anteprima limitata, inizialmente accessibile solo a determinati abbonamenti.] Versione del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="a72c4-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="a72c4-130">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="a72c4-130">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72c4-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a72c4-131">-WorkspaceName</span></span>
<span data-ttu-id="a72c4-132">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="a72c4-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a72c4-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a72c4-133">-WorkspaceObject</span></span>
<span data-ttu-id="a72c4-134">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a72c4-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a72c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72c4-135">CommonParameters</span></span>
<span data-ttu-id="a72c4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a72c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72c4-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a72c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72c4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a72c4-138">INPUTS</span></span>

### <span data-ttu-id="a72c4-139">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a72c4-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a72c4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a72c4-140">OUTPUTS</span></span>

### <span data-ttu-id="a72c4-141">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a72c4-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a72c4-142">Note</span><span class="sxs-lookup"><span data-stu-id="a72c4-142">NOTES</span></span>

## <span data-ttu-id="a72c4-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a72c4-143">RELATED LINKS</span></span>
