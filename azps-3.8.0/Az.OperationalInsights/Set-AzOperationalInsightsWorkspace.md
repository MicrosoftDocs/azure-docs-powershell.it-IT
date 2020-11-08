---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 3d85bcbf5352c06e379ac317cde052f3e744c10d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "94030741"
---
# <span data-ttu-id="5cfce-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5cfce-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="5cfce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cfce-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfce-103">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cfce-103">Updates a workspace.</span></span>

## <span data-ttu-id="5cfce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cfce-104">SYNTAX</span></span>

### <span data-ttu-id="5cfce-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5cfce-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5cfce-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="5cfce-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cfce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cfce-107">DESCRIPTION</span></span>
<span data-ttu-id="5cfce-108">Il cmdlet **set-AzOperationalInsightsWorkspace** modifica la configurazione di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cfce-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="5cfce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cfce-109">EXAMPLES</span></span>

### <span data-ttu-id="5cfce-110">Esempio 1: modificare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="5cfce-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="5cfce-111">Questo comando consente di modificare i SKU e i tag dell'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5cfce-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="5cfce-112">Esempio 2: aggiornare un'area di lavoro usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="5cfce-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="5cfce-113">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **set-AzOperationalInsightsWorkspace** usando l'operatore pipeline per impostare l'USK su Premium.</span><span class="sxs-lookup"><span data-stu-id="5cfce-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="5cfce-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cfce-114">PARAMETERS</span></span>

### <span data-ttu-id="5cfce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfce-115">-DefaultProfile</span></span>
<span data-ttu-id="5cfce-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5cfce-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cfce-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5cfce-117">-Name</span></span>
<span data-ttu-id="5cfce-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cfce-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cfce-119">-ResourceGroupName</span></span>
<span data-ttu-id="5cfce-120">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="5cfce-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5cfce-121">-RetentionInDays</span></span>
<span data-ttu-id="5cfce-122">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="5cfce-122">The workspace data retention in days.</span></span> <span data-ttu-id="5cfce-123">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="5cfce-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="5cfce-124">-Sku</span></span>
<span data-ttu-id="5cfce-125">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cfce-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="5cfce-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="5cfce-126">Valid values are:</span></span> 
- <span data-ttu-id="5cfce-127">gratuito</span><span class="sxs-lookup"><span data-stu-id="5cfce-127">free</span></span>
- <span data-ttu-id="5cfce-128">standard</span><span class="sxs-lookup"><span data-stu-id="5cfce-128">standard</span></span>
- <span data-ttu-id="5cfce-129">Premium</span><span class="sxs-lookup"><span data-stu-id="5cfce-129">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cfce-130">-Tag</span></span>
<span data-ttu-id="5cfce-131">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5cfce-131">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-132">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="5cfce-132">-Workspace</span></span>
<span data-ttu-id="5cfce-133">Specifica l'area di lavoro da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5cfce-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfce-134">CommonParameters</span></span>
<span data-ttu-id="5cfce-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cfce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfce-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cfce-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfce-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cfce-137">INPUTS</span></span>

### <span data-ttu-id="5cfce-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5cfce-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5cfce-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5cfce-139">System.String</span></span>

### <span data-ttu-id="5cfce-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5cfce-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5cfce-141">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5cfce-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5cfce-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cfce-142">OUTPUTS</span></span>

### <span data-ttu-id="5cfce-143">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5cfce-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="5cfce-144">Note</span><span class="sxs-lookup"><span data-stu-id="5cfce-144">NOTES</span></span>

## <span data-ttu-id="5cfce-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cfce-145">RELATED LINKS</span></span>

[<span data-ttu-id="5cfce-146">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="5cfce-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="5cfce-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5cfce-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


