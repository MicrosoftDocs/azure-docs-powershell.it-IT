---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 50920451ca96d21875352ff2ef460a5dcc989a20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475811"
---
# <span data-ttu-id="00bc0-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="00bc0-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="00bc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="00bc0-103">Crea un'area di lavoro o ripristina un'area di lavoro eliminata in modo soft.</span><span class="sxs-lookup"><span data-stu-id="00bc0-103">Creates a workspace, or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="00bc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00bc0-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [[-PublicNetworkAccessForIngestion] <String>]
 [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00bc0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="00bc0-106">Il cmdlet **New-AzOperationalInsightsWorkspace** crea un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="00bc0-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span> <span data-ttu-id="00bc0-107">O ripristinare un'area di lavoro eliminata in un piano.</span><span class="sxs-lookup"><span data-stu-id="00bc0-107">Or restore a soft-deleted workspace.</span></span>

## <span data-ttu-id="00bc0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00bc0-108">EXAMPLES</span></span>

### <span data-ttu-id="00bc0-109">Esempio 1: creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="00bc0-109">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="00bc0-110">Questo comando crea un'area di lavoro SKU standard denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="00bc0-110">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="00bc0-111">Esempio 2: creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="00bc0-111">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="00bc0-112">Il primo comando usa il cmdlet Get-AzOperationalInsightsLinkTargets per ottenere le destinazioni operative per l'account Insights link e li archivia nella variabile $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="00bc0-112">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="00bc0-113">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzOperationalInsightsWorkspace** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="00bc0-113">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="00bc0-114">Il comando crea un'area di lavoro SKU standard denominata area di lavoro collegata al primo account di approfondimenti operativi in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="00bc0-114">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="00bc0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00bc0-115">PARAMETERS</span></span>

### <span data-ttu-id="00bc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bc0-116">-DefaultProfile</span></span>
<span data-ttu-id="00bc0-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00bc0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00bc0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="00bc0-118">-Force</span></span>
<span data-ttu-id="00bc0-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="00bc0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00bc0-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="00bc0-120">-Location</span></span>
<span data-ttu-id="00bc0-121">Specifica la posizione in cui creare l'area di lavoro, ad esempio est degli Stati Uniti o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="00bc0-121">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="00bc0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="00bc0-122">-Name</span></span>
<span data-ttu-id="00bc0-123">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="00bc0-123">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="00bc0-124">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="00bc0-124">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="00bc0-125">Tipo di accesso alla rete per l'accesso all'ingestione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="00bc0-125">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="00bc0-126">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="00bc0-126">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="00bc0-127">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="00bc0-127">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="00bc0-128">Tipo di accesso alla rete per l'accesso alla query dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="00bc0-128">The network access type for accessing workspace query.</span></span> <span data-ttu-id="00bc0-129">Il valore deve essere "Enabled" o "disabled"</span><span class="sxs-lookup"><span data-stu-id="00bc0-129">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="00bc0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bc0-130">-ResourceGroupName</span></span>
<span data-ttu-id="00bc0-131">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="00bc0-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="00bc0-132">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00bc0-132">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="00bc0-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="00bc0-133">-RetentionInDays</span></span>
<span data-ttu-id="00bc0-134">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="00bc0-134">The workspace data retention in days.</span></span> <span data-ttu-id="00bc0-135">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="00bc0-135">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="00bc0-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="00bc0-136">-Sku</span></span>
<span data-ttu-id="00bc0-137">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="00bc0-137">Specifies the service tier of the workspace.</span></span> <span data-ttu-id="00bc0-138">Per altre informazioni sul valore da usare https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers , consulta.</span><span class="sxs-lookup"><span data-stu-id="00bc0-138">For more information regarding which value to use please check https://docs.microsoft.com/en-us/azure/azure-monitor/platform/manage-cost-storage#legacy-pricing-tiers.</span></span>
<span data-ttu-id="00bc0-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="00bc0-139">Valid values are:</span></span>
- <span data-ttu-id="00bc0-140">gratuito</span><span class="sxs-lookup"><span data-stu-id="00bc0-140">free</span></span>
- <span data-ttu-id="00bc0-141">pergb2018</span><span class="sxs-lookup"><span data-stu-id="00bc0-141">pergb2018</span></span>
- <span data-ttu-id="00bc0-142">pernode</span><span class="sxs-lookup"><span data-stu-id="00bc0-142">pernode</span></span>
- <span data-ttu-id="00bc0-143">Premium</span><span class="sxs-lookup"><span data-stu-id="00bc0-143">premium</span></span>
- <span data-ttu-id="00bc0-144">standalone</span><span class="sxs-lookup"><span data-stu-id="00bc0-144">standalone</span></span>
- <span data-ttu-id="00bc0-145">standard</span><span class="sxs-lookup"><span data-stu-id="00bc0-145">standard</span></span>

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

### <span data-ttu-id="00bc0-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="00bc0-146">-Tag</span></span>
<span data-ttu-id="00bc0-147">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="00bc0-147">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="00bc0-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00bc0-148">-Confirm</span></span>
<span data-ttu-id="00bc0-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00bc0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00bc0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00bc0-150">-WhatIf</span></span>
<span data-ttu-id="00bc0-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00bc0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00bc0-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00bc0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00bc0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bc0-153">CommonParameters</span></span>
<span data-ttu-id="00bc0-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bc0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bc0-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00bc0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bc0-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00bc0-156">INPUTS</span></span>

### <span data-ttu-id="00bc0-157">System. String</span><span class="sxs-lookup"><span data-stu-id="00bc0-157">System.String</span></span>

### <span data-ttu-id="00bc0-158">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00bc0-158">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="00bc0-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="00bc0-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="00bc0-160">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00bc0-160">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="00bc0-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00bc0-161">OUTPUTS</span></span>

### <span data-ttu-id="00bc0-162">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="00bc0-162">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="00bc0-163">Note</span><span class="sxs-lookup"><span data-stu-id="00bc0-163">NOTES</span></span>

<span data-ttu-id="00bc0-164">È stato rilasciato un nuovo modello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="00bc0-164">A new pricing model has been released.</span></span> <span data-ttu-id="00bc0-165">Se si è un CSP che indica che è necessario usare "standalone" per l'USK.</span><span class="sxs-lookup"><span data-stu-id="00bc0-165">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="00bc0-166">Dietro le quinte, l'USK verrà modificata in pergb2018.</span><span class="sxs-lookup"><span data-stu-id="00bc0-166">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="00bc0-167">Per altre informazioni, vedere quanto segue: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="00bc0-167">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="00bc0-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00bc0-168">RELATED LINKS</span></span>

[<span data-ttu-id="00bc0-169">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="00bc0-169">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="00bc0-170">Get-AzOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="00bc0-170">Get-AzOperationalInsightsLinkTargets</span></span>](./Get-AzOperationalInsightsLinkTargets.md)


