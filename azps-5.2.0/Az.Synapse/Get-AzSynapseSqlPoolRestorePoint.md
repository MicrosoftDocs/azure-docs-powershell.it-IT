---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359362"
---
# <span data-ttu-id="f7477-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f7477-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="f7477-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7477-102">SYNOPSIS</span></span>
<span data-ttu-id="f7477-103">Recupera i punti di ripristino distinti da cui può essere ripristinato un pool SQL di analisi delle sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f7477-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="f7477-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7477-104">SYNTAX</span></span>

### <span data-ttu-id="f7477-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7477-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7477-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7477-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7477-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7477-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7477-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7477-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7477-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7477-109">DESCRIPTION</span></span>
<span data-ttu-id="f7477-110">Il cmdlet **Get-AzSynapseSqlPoolRestorePoint** recupera i punti di ripristino distinti a cui può essere ripristinato un pool di analisi SQL di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f7477-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="f7477-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7477-111">EXAMPLES</span></span>

### <span data-ttu-id="f7477-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7477-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f7477-113">Questo comando restituisce tutti i punti di ripristino disponibili per il pool SQL sinapsi di analisi di Azure denominato ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="f7477-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="f7477-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7477-114">PARAMETERS</span></span>

### <span data-ttu-id="f7477-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7477-115">-DefaultProfile</span></span>
<span data-ttu-id="f7477-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7477-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7477-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7477-117">-InputObject</span></span>
<span data-ttu-id="f7477-118">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7477-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7477-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7477-119">-Name</span></span>
<span data-ttu-id="f7477-120">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="f7477-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f7477-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7477-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7477-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7477-122">Resource group name.</span></span>

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

### <span data-ttu-id="f7477-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7477-123">-ResourceId</span></span>
<span data-ttu-id="f7477-124">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="f7477-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f7477-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7477-125">-WorkspaceName</span></span>
<span data-ttu-id="f7477-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="f7477-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7477-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f7477-127">-WorkspaceObject</span></span>
<span data-ttu-id="f7477-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f7477-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7477-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7477-129">CommonParameters</span></span>
<span data-ttu-id="f7477-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7477-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7477-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7477-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7477-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7477-132">INPUTS</span></span>

### <span data-ttu-id="f7477-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7477-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f7477-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f7477-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f7477-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7477-135">OUTPUTS</span></span>

### <span data-ttu-id="f7477-136">Microsoft. Azure. Management. sinapsi. Models. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="f7477-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="f7477-137">Note</span><span class="sxs-lookup"><span data-stu-id="f7477-137">NOTES</span></span>

## <span data-ttu-id="f7477-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7477-138">RELATED LINKS</span></span>
