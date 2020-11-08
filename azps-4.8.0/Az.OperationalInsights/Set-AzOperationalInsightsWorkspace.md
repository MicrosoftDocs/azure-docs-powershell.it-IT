---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190900"
---
# <span data-ttu-id="19b1a-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b1a-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="19b1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="19b1a-103">Aggiorna un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-103">Updates a workspace.</span></span>

## <span data-ttu-id="19b1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19b1a-104">SYNTAX</span></span>

### <span data-ttu-id="19b1a-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19b1a-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="19b1a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="19b1a-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="19b1a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19b1a-107">DESCRIPTION</span></span>
<span data-ttu-id="19b1a-108">Il cmdlet **set-AzOperationalInsightsWorkspace** modifica la configurazione di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="19b1a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19b1a-109">EXAMPLES</span></span>

### <span data-ttu-id="19b1a-110">Esempio 1: modificare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="19b1a-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="19b1a-111">Questo comando consente di modificare i SKU e i tag dell'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19b1a-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="19b1a-112">Esempio 2: aggiornare un'area di lavoro usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="19b1a-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="19b1a-113">Questo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo passa al cmdlet **set-AzOperationalInsightsWorkspace** usando l'operatore pipeline per impostare l'USK su Premium.</span><span class="sxs-lookup"><span data-stu-id="19b1a-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="19b1a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19b1a-114">PARAMETERS</span></span>

### <span data-ttu-id="19b1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b1a-115">-DefaultProfile</span></span>
<span data-ttu-id="19b1a-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19b1a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19b1a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="19b1a-117">-Name</span></span>
<span data-ttu-id="19b1a-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="19b1a-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="19b1a-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="19b1a-120">Tipo di accesso alla rete per l'accesso all'ingestione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="19b1a-121">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="19b1a-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1a-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="19b1a-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="19b1a-123">Tipo di accesso alla rete per l'accesso alla query dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="19b1a-124">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="19b1a-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="19b1a-126">Specifica il nome del gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="19b1a-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="19b1a-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="19b1a-127">-RetentionInDays</span></span>
<span data-ttu-id="19b1a-128">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="19b1a-128">The workspace data retention in days.</span></span> <span data-ttu-id="19b1a-129">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="19b1a-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="19b1a-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="19b1a-130">-Sku</span></span>
<span data-ttu-id="19b1a-131">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="19b1a-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="19b1a-132">Valid values are:</span></span> 
- <span data-ttu-id="19b1a-133">gratuito</span><span class="sxs-lookup"><span data-stu-id="19b1a-133">free</span></span>
- <span data-ttu-id="19b1a-134">standard</span><span class="sxs-lookup"><span data-stu-id="19b1a-134">standard</span></span>
- <span data-ttu-id="19b1a-135">Premium</span><span class="sxs-lookup"><span data-stu-id="19b1a-135">premium</span></span>
- <span data-ttu-id="19b1a-136">pernode</span><span class="sxs-lookup"><span data-stu-id="19b1a-136">pernode</span></span>
- <span data-ttu-id="19b1a-137">standalone</span><span class="sxs-lookup"><span data-stu-id="19b1a-137">standalone</span></span>
- <span data-ttu-id="19b1a-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="19b1a-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19b1a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="19b1a-139">-Tag</span></span>
<span data-ttu-id="19b1a-140">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="19b1a-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="19b1a-141">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="19b1a-141">-Workspace</span></span>
<span data-ttu-id="19b1a-142">Specifica l'area di lavoro da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="19b1a-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="19b1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b1a-143">CommonParameters</span></span>
<span data-ttu-id="19b1a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b1a-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19b1a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b1a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19b1a-146">INPUTS</span></span>

### <span data-ttu-id="19b1a-147">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b1a-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="19b1a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="19b1a-148">System.String</span></span>

### <span data-ttu-id="19b1a-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19b1a-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="19b1a-150">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="19b1a-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="19b1a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19b1a-151">OUTPUTS</span></span>

### <span data-ttu-id="19b1a-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b1a-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="19b1a-153">Note</span><span class="sxs-lookup"><span data-stu-id="19b1a-153">NOTES</span></span>

## <span data-ttu-id="19b1a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19b1a-154">RELATED LINKS</span></span>

[<span data-ttu-id="19b1a-155">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="19b1a-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="19b1a-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="19b1a-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


