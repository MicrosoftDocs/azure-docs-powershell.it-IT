---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 863b83cbab64d791e55f8cfc2719d66be64fcac6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865655"
---
# <span data-ttu-id="d6861-101">New-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6861-101">New-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="d6861-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6861-102">SYNOPSIS</span></span>
<span data-ttu-id="d6861-103">Crea un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d6861-103">Creates a workspace.</span></span>

## <span data-ttu-id="d6861-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6861-104">SYNTAX</span></span>

```
New-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6861-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6861-105">DESCRIPTION</span></span>
<span data-ttu-id="d6861-106">Il cmdlet **New-AzOperationalInsightsWorkspace** crea un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="d6861-106">The **New-AzOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="d6861-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6861-107">EXAMPLES</span></span>

### <span data-ttu-id="d6861-108">Esempio 1: creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="d6861-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="d6861-109">Questo comando crea un'area di lavoro SKU standard denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d6861-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="d6861-110">Esempio 2: creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="d6861-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="d6861-111">Il primo comando usa il cmdlet Get-AzOperationalInsightsLinkTargets per ottenere le destinazioni operative per l'account Insights link e li archivia nella variabile $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="d6861-111">The first command uses the Get-AzOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="d6861-112">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzOperationalInsightsWorkspace** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6861-112">The second command passes the first account link target in $OILinkTargets to the **New-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d6861-113">Il comando crea un'area di lavoro SKU standard denominata area di lavoro collegata al primo account di approfondimenti operativi in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="d6861-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="d6861-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6861-114">PARAMETERS</span></span>

### <span data-ttu-id="d6861-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="d6861-115">-CustomerId</span></span>
<span data-ttu-id="d6861-116">Specifica l'account a cui verrà collegata l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d6861-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="d6861-117">Il cmdlet Get-AzOperationalInsightsLinkTargets può essere usato anche per elencare gli account potenziali.</span><span class="sxs-lookup"><span data-stu-id="d6861-117">The Get-AzOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6861-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6861-118">-DefaultProfile</span></span>
<span data-ttu-id="d6861-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6861-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6861-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d6861-120">-Force</span></span>
<span data-ttu-id="d6861-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d6861-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6861-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d6861-122">-Location</span></span>
<span data-ttu-id="d6861-123">Specifica la posizione in cui creare l'area di lavoro, ad esempio est degli Stati Uniti o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="d6861-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="d6861-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6861-124">-Name</span></span>
<span data-ttu-id="d6861-125">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d6861-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="d6861-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6861-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6861-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="d6861-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d6861-128">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6861-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="d6861-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d6861-129">-RetentionInDays</span></span>
<span data-ttu-id="d6861-130">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="d6861-130">The workspace data retention in days.</span></span> <span data-ttu-id="d6861-131">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="d6861-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="d6861-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="d6861-132">-Sku</span></span>
<span data-ttu-id="d6861-133">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d6861-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="d6861-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="d6861-134">Valid values are:</span></span>
- <span data-ttu-id="d6861-135">gratuito</span><span class="sxs-lookup"><span data-stu-id="d6861-135">free</span></span>
- <span data-ttu-id="d6861-136">standard</span><span class="sxs-lookup"><span data-stu-id="d6861-136">standard</span></span>
- <span data-ttu-id="d6861-137">standalone</span><span class="sxs-lookup"><span data-stu-id="d6861-137">standalone</span></span>
- <span data-ttu-id="d6861-138">Premium</span><span class="sxs-lookup"><span data-stu-id="d6861-138">premium</span></span>

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

### <span data-ttu-id="d6861-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d6861-139">-Tag</span></span>
<span data-ttu-id="d6861-140">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d6861-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="d6861-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6861-141">-Confirm</span></span>
<span data-ttu-id="d6861-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6861-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6861-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6861-143">-WhatIf</span></span>
<span data-ttu-id="d6861-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6861-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6861-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6861-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6861-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6861-146">CommonParameters</span></span>
<span data-ttu-id="d6861-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6861-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6861-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6861-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6861-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6861-149">INPUTS</span></span>

### <span data-ttu-id="d6861-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d6861-150">System.String</span></span>

### <span data-ttu-id="d6861-151">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6861-151">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d6861-152">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d6861-152">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d6861-153">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6861-153">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d6861-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6861-154">OUTPUTS</span></span>

### <span data-ttu-id="d6861-155">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d6861-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="d6861-156">Note</span><span class="sxs-lookup"><span data-stu-id="d6861-156">NOTES</span></span>

<span data-ttu-id="d6861-157">È stato rilasciato un nuovo modello di prezzo.</span><span class="sxs-lookup"><span data-stu-id="d6861-157">A new pricing model has been released.</span></span> <span data-ttu-id="d6861-158">Se si è un CSP che indica che è necessario usare "standalone" per l'USK.</span><span class="sxs-lookup"><span data-stu-id="d6861-158">If you are a CSP that means that you have to use "standalone" for the sku.</span></span> <span data-ttu-id="d6861-159">Dietro le quinte, l'USK verrà modificata in pergb2018.</span><span class="sxs-lookup"><span data-stu-id="d6861-159">Behind the scenes, the sku will be changed to pergb2018.</span></span> <span data-ttu-id="d6861-160">Per altre informazioni, vedere quanto segue: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span><span class="sxs-lookup"><span data-stu-id="d6861-160">For more information, please see the following: https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitoring-usage-and-estimated-costs#new-pricing-model</span></span>

## <span data-ttu-id="d6861-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6861-161">RELATED LINKS</span></span>

[<span data-ttu-id="d6861-162">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="d6861-162">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)
