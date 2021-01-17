---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359435"
---
# <span data-ttu-id="66cea-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="66cea-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="66cea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66cea-102">SYNOPSIS</span></span>
<span data-ttu-id="66cea-103">Ottiene le impostazioni avanzate per la protezione delle minacce per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="66cea-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="66cea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66cea-104">SYNTAX</span></span>

### <span data-ttu-id="66cea-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66cea-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66cea-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66cea-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66cea-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66cea-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66cea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66cea-108">DESCRIPTION</span></span>
<span data-ttu-id="66cea-109">Il cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** ottiene le impostazioni avanzate per la protezione delle minacce di un'area di lavoro di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="66cea-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="66cea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66cea-110">EXAMPLES</span></span>

### <span data-ttu-id="66cea-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="66cea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="66cea-112">Questo comando consente di ottenere le impostazioni avanzate di protezione dalle minacce per un'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="66cea-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="66cea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66cea-113">PARAMETERS</span></span>

### <span data-ttu-id="66cea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66cea-114">-DefaultProfile</span></span>
<span data-ttu-id="66cea-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66cea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66cea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66cea-116">-InputObject</span></span>
<span data-ttu-id="66cea-117">oggetto di input dell'area di lavoro, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="66cea-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="66cea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66cea-118">-ResourceGroupName</span></span>
<span data-ttu-id="66cea-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cea-119">Resource group name.</span></span>

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

### <span data-ttu-id="66cea-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66cea-120">-ResourceId</span></span>
<span data-ttu-id="66cea-121">Identificatore delle risorse dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="66cea-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="66cea-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66cea-122">-WorkspaceName</span></span>
<span data-ttu-id="66cea-123">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="66cea-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="66cea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66cea-124">CommonParameters</span></span>
<span data-ttu-id="66cea-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66cea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66cea-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66cea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66cea-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66cea-127">INPUTS</span></span>

### <span data-ttu-id="66cea-128">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="66cea-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="66cea-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66cea-129">OUTPUTS</span></span>

### <span data-ttu-id="66cea-130">Microsoft. Azure. Commands. sinapsi. Models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="66cea-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="66cea-131">Note</span><span class="sxs-lookup"><span data-stu-id="66cea-131">NOTES</span></span>

## <span data-ttu-id="66cea-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66cea-132">RELATED LINKS</span></span>
