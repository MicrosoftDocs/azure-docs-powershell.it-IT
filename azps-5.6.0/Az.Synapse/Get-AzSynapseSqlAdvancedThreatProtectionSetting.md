---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015709"
---
# <span data-ttu-id="e9bd0-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e9bd0-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e9bd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bd0-103">Ottiene le impostazioni di Protezione avanzata dalle minacce per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="e9bd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9bd0-104">SYNTAX</span></span>

### <span data-ttu-id="e9bd0-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9bd0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9bd0-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9bd0-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9bd0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9bd0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9bd0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9bd0-108">DESCRIPTION</span></span>
<span data-ttu-id="e9bd0-109">Il cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** ottiene le impostazioni avanzate di protezione dalle minacce di un'area di lavoro analisi di Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e9bd0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9bd0-110">EXAMPLES</span></span>

### <span data-ttu-id="e9bd0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9bd0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e9bd0-112">Questo comando recupera le impostazioni di protezione dalle minacce avanzate per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e9bd0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9bd0-113">PARAMETERS</span></span>

### <span data-ttu-id="e9bd0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bd0-114">-DefaultProfile</span></span>
<span data-ttu-id="e9bd0-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bd0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9bd0-116">-InputObject</span></span>
<span data-ttu-id="e9bd0-117">Oggetto di input dell'area di lavoro, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9bd0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bd0-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9bd0-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-119">Resource group name.</span></span>

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

### <span data-ttu-id="e9bd0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9bd0-120">-ResourceId</span></span>
<span data-ttu-id="e9bd0-121">Identificatore di risorsa dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9bd0-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9bd0-122">-WorkspaceName</span></span>
<span data-ttu-id="e9bd0-123">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9bd0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bd0-124">CommonParameters</span></span>
<span data-ttu-id="e9bd0-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bd0-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9bd0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bd0-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9bd0-127">INPUTS</span></span>

### <span data-ttu-id="e9bd0-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9bd0-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9bd0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9bd0-129">OUTPUTS</span></span>

### <span data-ttu-id="e9bd0-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="e9bd0-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="e9bd0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9bd0-131">NOTES</span></span>

## <span data-ttu-id="e9bd0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9bd0-132">RELATED LINKS</span></span>
