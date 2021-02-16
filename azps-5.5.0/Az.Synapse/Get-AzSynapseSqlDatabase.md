---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182775"
---
# <span data-ttu-id="473ec-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="473ec-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="473ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473ec-102">SYNOPSIS</span></span>
<span data-ttu-id="473ec-103">Ottiene un database SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="473ec-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="473ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="473ec-104">SYNTAX</span></span>

### <span data-ttu-id="473ec-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="473ec-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473ec-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="473ec-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="473ec-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="473ec-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="473ec-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="473ec-108">DESCRIPTION</span></span>
<span data-ttu-id="473ec-109">[Questa funzionalità viene visualizzata in anteprima limitata, inizialmente accessibile solo a determinati abbonamenti.] Il cmdlet **Get-AzSynapseSqlDatabase** ottiene informazioni su un database di Azure Synapse Analytics SQL database.</span><span class="sxs-lookup"><span data-stu-id="473ec-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="473ec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="473ec-110">EXAMPLES</span></span>

### <span data-ttu-id="473ec-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="473ec-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="473ec-112">Questo comando recupera tutti i SQL in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="473ec-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="473ec-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="473ec-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="473ec-114">Questo comando recupera il database SQL'area di lavoro ContosoWorkspace con il nome ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="473ec-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="473ec-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="473ec-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="473ec-116">Questo comando recupera tutti i database SQL in un'area di lavoro tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="473ec-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="473ec-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="473ec-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="473ec-118">Questo comando recupera il SQL di lavoro con l'ID risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="473ec-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="473ec-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="473ec-119">PARAMETERS</span></span>

### <span data-ttu-id="473ec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473ec-120">-DefaultProfile</span></span>
<span data-ttu-id="473ec-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="473ec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="473ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="473ec-122">-Name</span></span>
<span data-ttu-id="473ec-123">Nome del database SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="473ec-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="473ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="473ec-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="473ec-125">Resource group name.</span></span>

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

### <span data-ttu-id="473ec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="473ec-126">-ResourceId</span></span>
<span data-ttu-id="473ec-127">Identificatore di risorsa della SQL database.</span><span class="sxs-lookup"><span data-stu-id="473ec-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="473ec-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="473ec-128">-WorkspaceName</span></span>
<span data-ttu-id="473ec-129">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="473ec-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="473ec-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="473ec-130">-WorkspaceObject</span></span>
<span data-ttu-id="473ec-131">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="473ec-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="473ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473ec-132">CommonParameters</span></span>
<span data-ttu-id="473ec-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473ec-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="473ec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473ec-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="473ec-135">INPUTS</span></span>

### <span data-ttu-id="473ec-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="473ec-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="473ec-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="473ec-137">OUTPUTS</span></span>

### <span data-ttu-id="473ec-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="473ec-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="473ec-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="473ec-139">NOTES</span></span>

## <span data-ttu-id="473ec-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="473ec-140">RELATED LINKS</span></span>
