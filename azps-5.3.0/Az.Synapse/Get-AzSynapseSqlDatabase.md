---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383890"
---
# <span data-ttu-id="27717-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27717-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="27717-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27717-102">SYNOPSIS</span></span>
<span data-ttu-id="27717-103">Ottiene un database SQL di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27717-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="27717-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27717-104">SYNTAX</span></span>

### <span data-ttu-id="27717-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27717-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27717-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27717-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27717-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27717-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27717-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27717-108">DESCRIPTION</span></span>
<span data-ttu-id="27717-109">[Questa caratteristica è in un'anteprima limitata, inizialmente accessibile solo a determinati abbonamenti.] Il cmdlet **Get-AzSynapseSqlDatabase** ottiene le informazioni su un database SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="27717-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="27717-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27717-110">EXAMPLES</span></span>

### <span data-ttu-id="27717-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27717-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="27717-112">Questo comando consente di ottenere tutti i database SQL in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="27717-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="27717-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="27717-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="27717-114">Questo comando ottiene il database SQL in area di lavoro ContosoWorkspace con nome ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="27717-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="27717-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="27717-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="27717-116">Questo comando consente di ottenere tutti i database SQL in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="27717-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="27717-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="27717-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="27717-118">Questo comando ottiene il database SQL con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="27717-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="27717-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27717-119">PARAMETERS</span></span>

### <span data-ttu-id="27717-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27717-120">-DefaultProfile</span></span>
<span data-ttu-id="27717-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27717-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27717-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="27717-122">-Name</span></span>
<span data-ttu-id="27717-123">Nome del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27717-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="27717-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27717-124">-ResourceGroupName</span></span>
<span data-ttu-id="27717-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27717-125">Resource group name.</span></span>

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

### <span data-ttu-id="27717-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27717-126">-ResourceId</span></span>
<span data-ttu-id="27717-127">Identificatore delle risorse del database SQL di sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27717-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="27717-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27717-128">-WorkspaceName</span></span>
<span data-ttu-id="27717-129">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="27717-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="27717-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="27717-130">-WorkspaceObject</span></span>
<span data-ttu-id="27717-131">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="27717-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="27717-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27717-132">CommonParameters</span></span>
<span data-ttu-id="27717-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27717-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27717-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27717-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27717-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27717-135">INPUTS</span></span>

### <span data-ttu-id="27717-136">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27717-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="27717-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27717-137">OUTPUTS</span></span>

### <span data-ttu-id="27717-138">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27717-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="27717-139">Note</span><span class="sxs-lookup"><span data-stu-id="27717-139">NOTES</span></span>

## <span data-ttu-id="27717-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27717-140">RELATED LINKS</span></span>
