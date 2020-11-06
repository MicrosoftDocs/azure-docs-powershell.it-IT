---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 8c884e69dd13b96925940f467633baf515d88eda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513551"
---
# <span data-ttu-id="1f98c-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f98c-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1f98c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f98c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f98c-103">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f98c-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f98c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f98c-104">SYNTAX</span></span>

### <span data-ttu-id="1f98c-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f98c-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f98c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1f98c-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f98c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f98c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f98c-108">Il cmdlet **set-AzureRmOperationalInsightsWorkspace** modifica la configurazione di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f98c-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="1f98c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f98c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f98c-110">Esempio 1: modificare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="1f98c-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="1f98c-111">Questo comando consente di modificare i SKU e i tag dell'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f98c-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1f98c-112">Esempio 2: aggiornare un'area di lavoro usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="1f98c-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="1f98c-113">Questo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **set-AzureRmOperationalInsightsWorkspace** usando l'operatore pipeline per impostare l'USK su Premium.</span><span class="sxs-lookup"><span data-stu-id="1f98c-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="1f98c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f98c-114">PARAMETERS</span></span>

### <span data-ttu-id="1f98c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f98c-115">-DefaultProfile</span></span>
<span data-ttu-id="1f98c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f98c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f98c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f98c-117">-Name</span></span>
<span data-ttu-id="1f98c-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f98c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1f98c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f98c-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f98c-120">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1f98c-120">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="1f98c-121">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1f98c-121">-RetentionInDays</span></span>
<span data-ttu-id="1f98c-122">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="1f98c-122">The workspace data retention in days.</span></span> <span data-ttu-id="1f98c-123">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="1f98c-123">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="1f98c-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="1f98c-124">-Sku</span></span>
<span data-ttu-id="1f98c-125">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f98c-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="1f98c-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1f98c-126">Valid values are:</span></span> 
- <span data-ttu-id="1f98c-127">gratuito</span><span class="sxs-lookup"><span data-stu-id="1f98c-127">free</span></span>
- <span data-ttu-id="1f98c-128">standard</span><span class="sxs-lookup"><span data-stu-id="1f98c-128">standard</span></span>
- <span data-ttu-id="1f98c-129">Premium</span><span class="sxs-lookup"><span data-stu-id="1f98c-129">premium</span></span>

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

### <span data-ttu-id="1f98c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f98c-130">-Tag</span></span>
<span data-ttu-id="1f98c-131">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1f98c-131">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="1f98c-132">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1f98c-132">-Workspace</span></span>
<span data-ttu-id="1f98c-133">Specifica l'area di lavoro da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1f98c-133">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="1f98c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f98c-134">CommonParameters</span></span>
<span data-ttu-id="1f98c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f98c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f98c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f98c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f98c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f98c-137">INPUTS</span></span>

### <span data-ttu-id="1f98c-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f98c-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="1f98c-139">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f98c-139">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="1f98c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f98c-140">System.String</span></span>

### <span data-ttu-id="1f98c-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f98c-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f98c-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1f98c-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1f98c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f98c-143">OUTPUTS</span></span>

### <span data-ttu-id="1f98c-144">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f98c-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1f98c-145">Note</span><span class="sxs-lookup"><span data-stu-id="1f98c-145">NOTES</span></span>

## <span data-ttu-id="1f98c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f98c-146">RELATED LINKS</span></span>

[<span data-ttu-id="1f98c-147">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="1f98c-147">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1f98c-148">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1f98c-148">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


