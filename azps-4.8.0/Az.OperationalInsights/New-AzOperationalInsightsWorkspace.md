---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 8515bf4085fcd03d87aa15c3da649fe318b94966
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405007"
---
# <span data-ttu-id="9dcdc-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9dcdc-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="9dcdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcdc-103">Crea un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-103">Creates a workspace.</span></span>

## <span data-ttu-id="9dcdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dcdc-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dcdc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9dcdc-105">DESCRIPTION</span></span>
<span data-ttu-id="9dcdc-106">Il cmdlet **New-AzOperationalInsightsWorkspace** crea un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="9dcdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dcdc-107">EXAMPLES</span></span>

### <span data-ttu-id="9dcdc-108">Esempio 1: Creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="9dcdc-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="9dcdc-109">Questo comando crea un'area di lavoro SKU standard denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="9dcdc-110">Esempio 2: Creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="9dcdc-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="9dcdc-111">Il primo comando usa il cmdlet Get-AzOperationalInsightsLinkTargets per ottenere i target dei collegamenti dell'account di Operational Insights e quindi li archivia nella $OILinkTargets variabile.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="9dcdc-112">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzOperationalInsightsWorkspace** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9dcdc-113">Il comando crea un'area di lavoro SKU standard denominata MyWorkspace collegata al primo account di Analisi operativa in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="9dcdc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dcdc-114">PARAMETERS</span></span>

### <span data-ttu-id="9dcdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dcdc-115">-DefaultProfile</span></span>
<span data-ttu-id="9dcdc-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9dcdc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dcdc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9dcdc-117">-Force</span></span>
<span data-ttu-id="9dcdc-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9dcdc-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9dcdc-119">-Location</span></span>
<span data-ttu-id="9dcdc-120">Specifica la posizione in cui creare l'area di lavoro, ad esempio Stati Uniti orientali o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="9dcdc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9dcdc-121">-Name</span></span>
<span data-ttu-id="9dcdc-122">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="9dcdc-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="9dcdc-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="9dcdc-124">Tipo di accesso di rete per l'accesso all'inserimento nell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="9dcdc-125">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="9dcdc-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="9dcdc-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="9dcdc-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="9dcdc-127">Tipo di accesso di rete per accedere alla query dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="9dcdc-128">Il valore deve essere "Abilitato" o "Disabilitato"</span><span class="sxs-lookup"><span data-stu-id="9dcdc-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="9dcdc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dcdc-129">-ResourceGroupName</span></span>
<span data-ttu-id="9dcdc-130">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9dcdc-131">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="9dcdc-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9dcdc-132">-RetentionInDays</span></span>
<span data-ttu-id="9dcdc-133">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-133">The workspace data retention in days.</span></span> <span data-ttu-id="9dcdc-134">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="9dcdc-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="9dcdc-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="9dcdc-135">-Sku</span></span>
<span data-ttu-id="9dcdc-136">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="9dcdc-137">Per altre informazioni sul valore da usare, https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers controlla.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="9dcdc-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9dcdc-138">Valid values are:</span></span>
- <span data-ttu-id="9dcdc-139">gratis</span><span class="sxs-lookup"><span data-stu-id="9dcdc-139">free</span></span>
- <span data-ttu-id="9dcdc-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="9dcdc-140">pergb2018</span></span>
- <span data-ttu-id="9dcdc-141">pernode</span><span class="sxs-lookup"><span data-stu-id="9dcdc-141">pernode</span></span>
- <span data-ttu-id="9dcdc-142">premium</span><span class="sxs-lookup"><span data-stu-id="9dcdc-142">premium</span></span>
- <span data-ttu-id="9dcdc-143">autonomo</span><span class="sxs-lookup"><span data-stu-id="9dcdc-143">standalone</span></span>
- <span data-ttu-id="9dcdc-144">standard</span><span class="sxs-lookup"><span data-stu-id="9dcdc-144">standard</span></span>

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

### <span data-ttu-id="9dcdc-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dcdc-145">-Tag</span></span>
<span data-ttu-id="9dcdc-146">Tag di risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="9dcdc-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dcdc-147">-Confirm</span></span>
<span data-ttu-id="9dcdc-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dcdc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dcdc-149">-WhatIf</span></span>
<span data-ttu-id="9dcdc-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dcdc-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dcdc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dcdc-152">CommonParameters</span></span>
<span data-ttu-id="9dcdc-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dcdc-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dcdc-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="9dcdc-155">INPUTS</span></span>

### <span data-ttu-id="9dcdc-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9dcdc-156">System.String</span></span>

### <span data-ttu-id="9dcdc-157">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dcdc-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9dcdc-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9dcdc-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9dcdc-159">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dcdc-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9dcdc-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dcdc-160">OUTPUTS</span></span>

### <span data-ttu-id="9dcdc-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9dcdc-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9dcdc-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="9dcdc-162">NOTES</span></span>

<span data-ttu-id="9dcdc-163">È stato rilasciato un nuovo modello di prezzi.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-163">A new pricing model has been released.</span></span> <span data-ttu-id="9dcdc-164">Se si è un CSP, è necessario usare la versione "autonoma" per la SKU.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="9dcdc-165">Dietro le quinte, la SKU verrà cambiata in pergb2018.</span><span class="sxs-lookup"><span data-stu-id="9dcdc-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="9dcdc-166">Per altre informazioni, vedere: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="9dcdc-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="9dcdc-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dcdc-167">RELATED LINKS</span></span>

[<span data-ttu-id="9dcdc-168">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="9dcdc-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



