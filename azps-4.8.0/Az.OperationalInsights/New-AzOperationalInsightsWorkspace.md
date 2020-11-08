---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: feac2aa9c5dd92c0d76090c6fc28353d56f9647c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191991"
---
# <span data-ttu-id="c112e-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c112e-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c112e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c112e-102">SYNOPSIS</span></span>
<span data-ttu-id="c112e-103">Crea un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-103">Creates a workspace.</span></span>

## <span data-ttu-id="c112e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c112e-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c112e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c112e-105">DESCRIPTION</span></span>
<span data-ttu-id="c112e-106">Il cmdlet **New-AzOperationalInsightsWorkspace** crea un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="c112e-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="c112e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c112e-107">EXAMPLES</span></span>

### <span data-ttu-id="c112e-108">Esempio 1: creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="c112e-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="c112e-109">Questo comando crea un'area di lavoro SKU standard denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c112e-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c112e-110">Esempio 2: creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="c112e-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="c112e-111">Il primo comando usa il cmdlet Get-AzOperationalInsightsLinkTargets per ottenere le destinazioni operative per l'account Insights link e li archivia nella variabile $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="c112e-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="c112e-112">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzOperationalInsightsWorkspace** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="c112e-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c112e-113">Il comando crea un'area di lavoro SKU standard denominata area di lavoro collegata al primo account di approfondimenti operativi in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="c112e-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="c112e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c112e-114">PARAMETERS</span></span>

### <span data-ttu-id="c112e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c112e-115">-DefaultProfile</span></span>
<span data-ttu-id="c112e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c112e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c112e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c112e-117">-Force</span></span>
<span data-ttu-id="c112e-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c112e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c112e-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c112e-119">-Location</span></span>
<span data-ttu-id="c112e-120">Specifica la posizione in cui creare l'area di lavoro, ad esempio est degli Stati Uniti o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="c112e-120">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="c112e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c112e-121">-Name</span></span>
<span data-ttu-id="c112e-122">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-122">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c112e-123">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c112e-123">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c112e-124">Tipo di accesso alla rete per l'accesso all'ingestione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-124">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="c112e-125">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="c112e-125">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="c112e-126">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c112e-126">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c112e-127">Tipo di accesso alla rete per l'accesso alla query dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-127">The network access type for accessing workspace query.</span></span> <span data-ttu-id="c112e-128">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="c112e-128">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="c112e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c112e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c112e-130">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c112e-130">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c112e-131">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c112e-131">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="c112e-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c112e-132">-RetentionInDays</span></span>
<span data-ttu-id="c112e-133">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="c112e-133">The workspace data retention in days.</span></span> <span data-ttu-id="c112e-134">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="c112e-134">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="c112e-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="c112e-135">-Sku</span></span>
<span data-ttu-id="c112e-136">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-136">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="c112e-137">Per altre informazioni sul valore da usare https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers , consulta.</span><span class="sxs-lookup"><span data-stu-id="c112e-137">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="c112e-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c112e-138">Valid values are:</span></span>
- <span data-ttu-id="c112e-139">gratuito</span><span class="sxs-lookup"><span data-stu-id="c112e-139">free</span></span>
- <span data-ttu-id="c112e-140">pergb2018</span><span class="sxs-lookup"><span data-stu-id="c112e-140">pergb2018</span></span>
- <span data-ttu-id="c112e-141">pernode</span><span class="sxs-lookup"><span data-stu-id="c112e-141">pernode</span></span>
- <span data-ttu-id="c112e-142">Premium</span><span class="sxs-lookup"><span data-stu-id="c112e-142">premium</span></span>
- <span data-ttu-id="c112e-143">standalone</span><span class="sxs-lookup"><span data-stu-id="c112e-143">standalone</span></span>
- <span data-ttu-id="c112e-144">standard</span><span class="sxs-lookup"><span data-stu-id="c112e-144">standard</span></span>

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

### <span data-ttu-id="c112e-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="c112e-145">-Tag</span></span>
<span data-ttu-id="c112e-146">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c112e-146">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="c112e-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c112e-147">-Confirm</span></span>
<span data-ttu-id="c112e-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c112e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c112e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c112e-149">-WhatIf</span></span>
<span data-ttu-id="c112e-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c112e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c112e-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c112e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c112e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c112e-152">CommonParameters</span></span>
<span data-ttu-id="c112e-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c112e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c112e-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c112e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c112e-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c112e-155">INPUTS</span></span>

### <span data-ttu-id="c112e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c112e-156">System.String</span></span>

### <span data-ttu-id="c112e-157">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c112e-157">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c112e-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c112e-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c112e-159">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c112e-159">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c112e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c112e-160">OUTPUTS</span></span>

### <span data-ttu-id="c112e-161">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c112e-161">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c112e-162">Note</span><span class="sxs-lookup"><span data-stu-id="c112e-162">NOTES</span></span>

<span data-ttu-id="c112e-163">È stato rilasciato un nuovo modello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="c112e-163">A new pricing model has been released.</span></span> <span data-ttu-id="c112e-164">Se si è un CSP che indica che è necessario usare "standalone" per l'USK.</span><span class="sxs-lookup"><span data-stu-id="c112e-164">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="c112e-165">Dietro le quinte, l'USK verrà modificata in pergb2018.</span><span class="sxs-lookup"><span data-stu-id="c112e-165">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="c112e-166">Per altre informazioni, vedere quanto segue: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="c112e-166">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="c112e-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c112e-167">RELATED LINKS</span></span>

[<span data-ttu-id="c112e-168">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="c112e-168">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="c112e-169">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="c112e-169">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


