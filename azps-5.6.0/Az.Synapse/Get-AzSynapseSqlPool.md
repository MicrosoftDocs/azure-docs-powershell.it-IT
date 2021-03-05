---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015678"
---
# <span data-ttu-id="6c49e-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6c49e-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="6c49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c49e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c49e-103">Ottiene un pool di SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6c49e-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6c49e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c49e-104">SYNTAX</span></span>

### <span data-ttu-id="6c49e-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c49e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c49e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c49e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c49e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c49e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c49e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c49e-108">DESCRIPTION</span></span>
<span data-ttu-id="6c49e-109">Il cmdlet **Get-AzSynapseSqlPool** ottiene informazioni su un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6c49e-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6c49e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c49e-110">EXAMPLES</span></span>

### <span data-ttu-id="6c49e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c49e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6c49e-112">Questo comando recupera tutti i pool SQL in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6c49e-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="6c49e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6c49e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6c49e-114">Questo comando recupera il pool SQL nell'area di lavoro ContosoWorkspace con il nome ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="6c49e-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="6c49e-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6c49e-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="6c49e-116">Questo comando recupera tutti i pool di SQL in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c49e-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="6c49e-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="6c49e-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="6c49e-118">Questo comando recupera il SQL di risorse con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="6c49e-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="6c49e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c49e-119">PARAMETERS</span></span>

### <span data-ttu-id="6c49e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c49e-120">-DefaultProfile</span></span>
<span data-ttu-id="6c49e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c49e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c49e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6c49e-122">-Name</span></span>
<span data-ttu-id="6c49e-123">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c49e-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c49e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c49e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c49e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c49e-125">Resource group name.</span></span>

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

### <span data-ttu-id="6c49e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c49e-126">-ResourceId</span></span>
<span data-ttu-id="6c49e-127">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="6c49e-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="6c49e-128">-Version</span><span class="sxs-lookup"><span data-stu-id="6c49e-128">-Version</span></span>
<span data-ttu-id="6c49e-129">[Questa funzionalità viene visualizzata in anteprima limitata, inizialmente accessibile solo a determinati abbonamenti.] Versione di Synapse SQL pool.</span><span class="sxs-lookup"><span data-stu-id="6c49e-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="6c49e-130">Ad esempio, 2 o 3.</span><span class="sxs-lookup"><span data-stu-id="6c49e-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="6c49e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c49e-131">-WorkspaceName</span></span>
<span data-ttu-id="6c49e-132">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="6c49e-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6c49e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6c49e-133">-WorkspaceObject</span></span>
<span data-ttu-id="6c49e-134">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c49e-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6c49e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c49e-135">CommonParameters</span></span>
<span data-ttu-id="6c49e-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c49e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c49e-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c49e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c49e-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c49e-138">INPUTS</span></span>

### <span data-ttu-id="6c49e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c49e-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6c49e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c49e-140">OUTPUTS</span></span>

### <span data-ttu-id="6c49e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6c49e-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6c49e-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c49e-142">NOTES</span></span>

## <span data-ttu-id="6c49e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c49e-143">RELATED LINKS</span></span>
