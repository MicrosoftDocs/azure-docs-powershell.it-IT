---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cee34e8437048f0cc59df3463b0b7f3cf2de6ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985486"
---
# <span data-ttu-id="aa0aa-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="aa0aa-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="aa0aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0aa-103">Ottiene lo stato TDE per un SQL pool.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="aa0aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa0aa-104">SYNTAX</span></span>

### <span data-ttu-id="aa0aa-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa0aa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa0aa-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa0aa-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa0aa-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa0aa-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa0aa-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa0aa-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa0aa-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa0aa-109">DESCRIPTION</span></span>
<span data-ttu-id="aa0aa-110">Il cmdlet **Get-AzSynapseSqlPoolTransparentDataEncryption** ottiene lo stato di Transparent Data Encryption (TDE) per un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="aa0aa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa0aa-111">EXAMPLES</span></span>

### <span data-ttu-id="aa0aa-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa0aa-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="aa0aa-113">Questo comando recupera lo stato di TDE per il pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="aa0aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa0aa-114">PARAMETERS</span></span>

### <span data-ttu-id="aa0aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0aa-115">-DefaultProfile</span></span>
<span data-ttu-id="aa0aa-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa0aa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa0aa-117">-InputObject</span></span>
<span data-ttu-id="aa0aa-118">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="aa0aa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aa0aa-119">-Name</span></span>
<span data-ttu-id="aa0aa-120">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="aa0aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa0aa-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-122">Resource group name.</span></span>

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

### <span data-ttu-id="aa0aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0aa-123">-ResourceId</span></span>
<span data-ttu-id="aa0aa-124">Identificatore di risorsa del pool SQL synapse.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="aa0aa-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aa0aa-125">-WorkspaceName</span></span>
<span data-ttu-id="aa0aa-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="aa0aa-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aa0aa-127">-WorkspaceObject</span></span>
<span data-ttu-id="aa0aa-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="aa0aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0aa-129">CommonParameters</span></span>
<span data-ttu-id="aa0aa-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0aa-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa0aa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0aa-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa0aa-132">INPUTS</span></span>

### <span data-ttu-id="aa0aa-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="aa0aa-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="aa0aa-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="aa0aa-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="aa0aa-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa0aa-135">OUTPUTS</span></span>

### <span data-ttu-id="aa0aa-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="aa0aa-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="aa0aa-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa0aa-137">NOTES</span></span>

## <span data-ttu-id="aa0aa-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa0aa-138">RELATED LINKS</span></span>
