---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8d46c16afe8041181916eb25affed58e072798ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989881"
---
# <span data-ttu-id="e1c96-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1c96-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="e1c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1c96-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c96-103">Crea un'area di lavoro o ripristina un'area di lavoro eliminata in modo ].</span><span class="sxs-lookup"><span data-stu-id="e1c96-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="e1c96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1c96-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1c96-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1c96-105">DESCRIPTION</span></span>
<span data-ttu-id="e1c96-106">Il cmdlet **New-AzOperationalInsightsWorkspace crea** un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="e1c96-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="e1c96-107">Oppure ripristinare un'area di lavoro eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e1c96-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="e1c96-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1c96-108">EXAMPLES</span></span>

### <span data-ttu-id="e1c96-109">Esempio 1: Creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="e1c96-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="e1c96-110">Questo comando crea un'area di lavoro SKU standard denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e1c96-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e1c96-111">Esempio 2: Creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="e1c96-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="e1c96-112">Il primo comando usa il cmdlet Get-AzOperationalInsightsLinkTargets per ottenere i target dei collegamenti dell'account di Operational Insights e quindi li archivia nella $OILinkTargets variabile.</span><span class="sxs-lookup"><span data-stu-id="e1c96-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="e1c96-113">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzOperationalInsightsWorkspace** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1c96-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e1c96-114">Il comando crea un'area di lavoro SKU standard denominata MyWorkspace collegata al primo account di Analisi operativa in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="e1c96-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="e1c96-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1c96-115">PARAMETERS</span></span>

### <span data-ttu-id="e1c96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c96-116">-DefaultProfile</span></span>
<span data-ttu-id="e1c96-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e1c96-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1c96-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e1c96-118">-Force</span></span>
<span data-ttu-id="e1c96-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="e1c96-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e1c96-120">-Location</span></span>
<span data-ttu-id="e1c96-121">Specifica la posizione in cui creare l'area di lavoro, ad esempio Stati Uniti orientali o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="e1c96-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1c96-122">-Name</span></span>
<span data-ttu-id="e1c96-123">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1c96-123">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="e1c96-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="e1c96-125">Tipo di accesso di rete per l'accesso all'inserimento nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1c96-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="e1c96-126">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="e1c96-126">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="e1c96-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="e1c96-128">Tipo di accesso di rete per accedere alla query dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1c96-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="e1c96-129">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="e1c96-129">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1c96-130">-ResourceGroupName</span></span>
<span data-ttu-id="e1c96-131">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="e1c96-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e1c96-132">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1c96-132">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e1c96-133">-RetentionInDays</span></span>
<span data-ttu-id="e1c96-134">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="e1c96-134">The workspace data retention in days.</span></span> <span data-ttu-id="e1c96-135">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="e1c96-135">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="e1c96-136">-Sku</span></span>
<span data-ttu-id="e1c96-137">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1c96-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="e1c96-138">Per altre informazioni sul valore da usare, https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers controlla.</span><span class="sxs-lookup"><span data-stu-id="e1c96-138">For more information regarding which value to use please check https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="e1c96-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e1c96-139">Valid values are:</span></span>
- <span data-ttu-id="e1c96-140">gratis</span><span class="sxs-lookup"><span data-stu-id="e1c96-140">free</span></span>
- <span data-ttu-id="e1c96-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="e1c96-141">pergb2018</span></span>
- <span data-ttu-id="e1c96-142">pernode</span><span class="sxs-lookup"><span data-stu-id="e1c96-142">pernode</span></span>
- <span data-ttu-id="e1c96-143">premium</span><span class="sxs-lookup"><span data-stu-id="e1c96-143">premium</span></span>
- <span data-ttu-id="e1c96-144">autonomo</span><span class="sxs-lookup"><span data-stu-id="e1c96-144">standalone</span></span>
- <span data-ttu-id="e1c96-145">standard</span><span class="sxs-lookup"><span data-stu-id="e1c96-145">standard</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1c96-146">-Tag</span></span>
<span data-ttu-id="e1c96-147">Tag di risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="e1c96-147">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1c96-148">-Confirm</span></span>
<span data-ttu-id="e1c96-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1c96-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1c96-150">-WhatIf</span></span>
<span data-ttu-id="e1c96-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1c96-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1c96-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1c96-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c96-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c96-153">CommonParameters</span></span>
<span data-ttu-id="e1c96-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c96-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c96-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1c96-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c96-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1c96-156">INPUTS</span></span>

### <span data-ttu-id="e1c96-157">System.String</span><span class="sxs-lookup"><span data-stu-id="e1c96-157">System.String</span></span>

### <span data-ttu-id="e1c96-158">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1c96-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e1c96-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1c96-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e1c96-160">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e1c96-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e1c96-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1c96-161">OUTPUTS</span></span>

### <span data-ttu-id="e1c96-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e1c96-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="e1c96-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1c96-163">NOTES</span></span>

<span data-ttu-id="e1c96-164">È stato rilasciato un nuovo modello di prezzi.</span><span class="sxs-lookup"><span data-stu-id="e1c96-164">A new pricing model has been released.</span></span> <span data-ttu-id="e1c96-165">Se si è un CSP, è necessario usare la versione "autonoma" per la SKU.</span><span class="sxs-lookup"><span data-stu-id="e1c96-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="e1c96-166">Dietro le quinte, la SKU verrà cambiata in pergb2018.</span><span class="sxs-lookup"><span data-stu-id="e1c96-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="e1c96-167">Per altre informazioni, vedere: https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="e1c96-167">For more information, please see the following: https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="e1c96-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1c96-168">RELATED LINKS</span></span>

[<span data-ttu-id="e1c96-169">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="e1c96-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="e1c96-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="e1c96-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


