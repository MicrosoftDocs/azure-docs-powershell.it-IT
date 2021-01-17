---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383795"
---
# <span data-ttu-id="72128-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="72128-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="72128-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72128-102">SYNOPSIS</span></span>
<span data-ttu-id="72128-103">Ottiene lo stato di Transparence per un pool SQL.</span><span class="sxs-lookup"><span data-stu-id="72128-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="72128-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72128-104">SYNTAX</span></span>

### <span data-ttu-id="72128-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72128-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72128-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72128-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72128-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72128-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72128-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72128-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72128-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72128-109">DESCRIPTION</span></span>
<span data-ttu-id="72128-110">Il cmdlet **Get-AzSynapseSqlPoolTransparentDataEncryption** ottiene lo stato della crittografia dei dati trasparente (Transparent Data Encryption) per un pool SQL di analisi delle sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="72128-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="72128-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72128-111">EXAMPLES</span></span>

### <span data-ttu-id="72128-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72128-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="72128-113">Questo comando ottiene lo stato di Transparent per il pool SQL denominato ContosoSqlPool sotto l'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="72128-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="72128-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72128-114">PARAMETERS</span></span>

### <span data-ttu-id="72128-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72128-115">-DefaultProfile</span></span>
<span data-ttu-id="72128-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72128-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72128-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72128-117">-InputObject</span></span>
<span data-ttu-id="72128-118">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="72128-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="72128-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="72128-119">-Name</span></span>
<span data-ttu-id="72128-120">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="72128-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="72128-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72128-121">-ResourceGroupName</span></span>
<span data-ttu-id="72128-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72128-122">Resource group name.</span></span>

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

### <span data-ttu-id="72128-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72128-123">-ResourceId</span></span>
<span data-ttu-id="72128-124">Identificatore delle risorse del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="72128-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="72128-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72128-125">-WorkspaceName</span></span>
<span data-ttu-id="72128-126">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="72128-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="72128-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="72128-127">-WorkspaceObject</span></span>
<span data-ttu-id="72128-128">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="72128-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="72128-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72128-129">CommonParameters</span></span>
<span data-ttu-id="72128-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72128-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72128-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72128-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72128-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72128-132">INPUTS</span></span>

### <span data-ttu-id="72128-133">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="72128-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="72128-134">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="72128-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="72128-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72128-135">OUTPUTS</span></span>

### <span data-ttu-id="72128-136">Microsoft. Azure. Commands. sinapsi. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="72128-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="72128-137">Note</span><span class="sxs-lookup"><span data-stu-id="72128-137">NOTES</span></span>

## <span data-ttu-id="72128-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72128-138">RELATED LINKS</span></span>
