---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510388"
---
# <span data-ttu-id="82988-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="82988-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="82988-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82988-102">SYNOPSIS</span></span>
<span data-ttu-id="82988-103">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="82988-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82988-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82988-104">SYNTAX</span></span>

### <span data-ttu-id="82988-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82988-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82988-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="82988-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82988-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82988-107">DESCRIPTION</span></span>
<span data-ttu-id="82988-108">Il cmdlet **set-AzureRmOperationalInsightsWorkspace** modifica la configurazione di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="82988-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="82988-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82988-109">EXAMPLES</span></span>

### <span data-ttu-id="82988-110">Esempio 1: modificare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="82988-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="82988-111">Questo comando consente di modificare i SKU e i tag dell'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="82988-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="82988-112">Esempio 2: aggiornare un'area di lavoro usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="82988-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="82988-113">Questo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **set-AzureRmOperationalInsightsWorkspace** usando l'operatore pipeline per impostare l'USK su Premium.</span><span class="sxs-lookup"><span data-stu-id="82988-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="82988-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82988-114">PARAMETERS</span></span>

### <span data-ttu-id="82988-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="82988-115">-Name</span></span>
<span data-ttu-id="82988-116">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="82988-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="82988-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82988-117">-ResourceGroupName</span></span>
<span data-ttu-id="82988-118">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="82988-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="82988-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="82988-119">-Sku</span></span>
<span data-ttu-id="82988-120">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="82988-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="82988-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="82988-121">Valid values are:</span></span> 

- <span data-ttu-id="82988-122">gratuito</span><span class="sxs-lookup"><span data-stu-id="82988-122">free</span></span>
- <span data-ttu-id="82988-123">standard</span><span class="sxs-lookup"><span data-stu-id="82988-123">standard</span></span>
- <span data-ttu-id="82988-124">Premium</span><span class="sxs-lookup"><span data-stu-id="82988-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82988-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="82988-125">-Tags</span></span>
<span data-ttu-id="82988-126">Specifica i tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="82988-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="82988-127">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="82988-127">-Workspace</span></span>
<span data-ttu-id="82988-128">Specifica l'area di lavoro da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="82988-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="82988-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82988-129">-DefaultProfile</span></span>
<span data-ttu-id="82988-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82988-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82988-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="82988-131">-RetentionInDays</span></span>
<span data-ttu-id="82988-132">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="82988-132">The workspace data retention in days.</span></span> <span data-ttu-id="82988-133">730 days è il massimo consentito per tutte le altre SKU.</span><span class="sxs-lookup"><span data-stu-id="82988-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="82988-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82988-134">CommonParameters</span></span>
<span data-ttu-id="82988-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82988-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82988-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82988-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82988-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82988-137">INPUTS</span></span>

### <span data-ttu-id="82988-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="82988-138">PSWorkspace</span></span>
<span data-ttu-id="82988-139">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="82988-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="82988-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82988-140">OUTPUTS</span></span>

### <span data-ttu-id="82988-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="82988-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="82988-142">Note</span><span class="sxs-lookup"><span data-stu-id="82988-142">NOTES</span></span>

## <span data-ttu-id="82988-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82988-143">RELATED LINKS</span></span>

[<span data-ttu-id="82988-144">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="82988-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="82988-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="82988-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


