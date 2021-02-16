---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209042"
---
# <span data-ttu-id="a1912-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a1912-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a1912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1912-102">SYNOPSIS</span></span>
<span data-ttu-id="a1912-103">Ottiene le impostazioni di Protezione avanzata dalle minacce per un SQL pool.</span><span class="sxs-lookup"><span data-stu-id="a1912-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="a1912-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1912-104">SYNTAX</span></span>

### <span data-ttu-id="a1912-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1912-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1912-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1912-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1912-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1912-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1912-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1912-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1912-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1912-109">DESCRIPTION</span></span>
<span data-ttu-id="a1912-110">Il cmdlet **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** ottiene le impostazioni di protezione dalle minacce avanzate di un pool di SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a1912-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a1912-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1912-111">EXAMPLES</span></span>

### <span data-ttu-id="a1912-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1912-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a1912-113">Questo comando recupera le impostazioni di protezione dalle minacce avanzate per un pool SQL denominato ContosoSqlPool nell'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a1912-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a1912-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1912-114">PARAMETERS</span></span>

### <span data-ttu-id="a1912-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1912-115">-DefaultProfile</span></span>
<span data-ttu-id="a1912-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1912-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1912-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1912-117">-InputObject</span></span>
<span data-ttu-id="a1912-118">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1912-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1912-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a1912-119">-Name</span></span>
<span data-ttu-id="a1912-120">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1912-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a1912-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1912-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1912-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1912-122">Resource group name.</span></span>

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

### <span data-ttu-id="a1912-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1912-123">-ResourceId</span></span>
<span data-ttu-id="a1912-124">Identificatore di risorsa dell'SQL pool.</span><span class="sxs-lookup"><span data-stu-id="a1912-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a1912-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1912-125">-WorkspaceName</span></span>
<span data-ttu-id="a1912-126">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="a1912-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a1912-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a1912-127">-WorkspaceObject</span></span>
<span data-ttu-id="a1912-128">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1912-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1912-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1912-129">CommonParameters</span></span>
<span data-ttu-id="a1912-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1912-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1912-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1912-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1912-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1912-132">INPUTS</span></span>

### <span data-ttu-id="a1912-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a1912-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a1912-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a1912-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a1912-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1912-135">OUTPUTS</span></span>

### <span data-ttu-id="a1912-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a1912-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="a1912-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1912-137">NOTES</span></span>

## <span data-ttu-id="a1912-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1912-138">RELATED LINKS</span></span>
