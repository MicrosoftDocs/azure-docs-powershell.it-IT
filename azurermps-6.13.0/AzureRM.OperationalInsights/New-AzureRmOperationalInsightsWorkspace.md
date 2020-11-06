---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 97f8cba0641ed576cb187f3b995d400bc7f521a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517380"
---
# <span data-ttu-id="1e162-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e162-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1e162-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e162-102">SYNOPSIS</span></span>
<span data-ttu-id="1e162-103">Crea un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1e162-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e162-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e162-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e162-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e162-105">DESCRIPTION</span></span>
<span data-ttu-id="1e162-106">Il cmdlet **New-AzureRmOperationalInsightsWorkspace** crea un'area di lavoro nel gruppo di risorse e nella posizione specificati.</span><span class="sxs-lookup"><span data-stu-id="1e162-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="1e162-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e162-107">EXAMPLES</span></span>

### <span data-ttu-id="1e162-108">Esempio 1: creare un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="1e162-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="1e162-109">Questo comando crea un'area di lavoro SKU standard denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e162-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="1e162-110">Esempio 2: creare un'area di lavoro e collegarla a un account esistente</span><span class="sxs-lookup"><span data-stu-id="1e162-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="1e162-111">Il primo comando usa il cmdlet Get-AzureRmOperationalInsightsLinkTargets per ottenere le destinazioni operative per l'account Insights link e li archivia nella variabile $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="1e162-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="1e162-112">Il secondo comando passa la prima destinazione del collegamento dell'account in $OILinkTargets al cmdlet **New-AzureRmOperationalInsightsWorkspace** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e162-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1e162-113">Il comando crea un'area di lavoro SKU standard denominata area di lavoro collegata al primo account di approfondimenti operativi in $OILinkTargets.</span><span class="sxs-lookup"><span data-stu-id="1e162-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="1e162-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e162-114">PARAMETERS</span></span>

### <span data-ttu-id="1e162-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="1e162-115">-CustomerId</span></span>
<span data-ttu-id="1e162-116">Specifica l'account a cui verrà collegata l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1e162-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="1e162-117">Il cmdlet Get-AzureRmOperationalInsightsLinkTargets può essere usato anche per elencare gli account potenziali.</span><span class="sxs-lookup"><span data-stu-id="1e162-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

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

### <span data-ttu-id="1e162-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e162-118">-DefaultProfile</span></span>
<span data-ttu-id="1e162-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1e162-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e162-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1e162-120">-Force</span></span>
<span data-ttu-id="1e162-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1e162-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e162-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1e162-122">-Location</span></span>
<span data-ttu-id="1e162-123">Specifica la posizione in cui creare l'area di lavoro, ad esempio est degli Stati Uniti o Europa occidentale.</span><span class="sxs-lookup"><span data-stu-id="1e162-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

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

### <span data-ttu-id="1e162-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e162-124">-Name</span></span>
<span data-ttu-id="1e162-125">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1e162-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="1e162-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e162-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e162-127">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1e162-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1e162-128">L'area di lavoro viene creata in questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e162-128">The workspace is created in this resource group.</span></span>

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

### <span data-ttu-id="1e162-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1e162-129">-RetentionInDays</span></span>
<span data-ttu-id="1e162-130">Conservazione dei dati dell'area di lavoro in giorni.</span><span class="sxs-lookup"><span data-stu-id="1e162-130">The workspace data retention in days.</span></span> <span data-ttu-id="1e162-131">730 giorni è il massimo consentito per tutte le altre SKU</span><span class="sxs-lookup"><span data-stu-id="1e162-131">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="1e162-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="1e162-132">-Sku</span></span>
<span data-ttu-id="1e162-133">Specifica il livello di servizio dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1e162-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="1e162-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1e162-134">Valid values are:</span></span> 
- <span data-ttu-id="1e162-135">gratuito</span><span class="sxs-lookup"><span data-stu-id="1e162-135">free</span></span>
- <span data-ttu-id="1e162-136">standard</span><span class="sxs-lookup"><span data-stu-id="1e162-136">standard</span></span>
- <span data-ttu-id="1e162-137">Premium</span><span class="sxs-lookup"><span data-stu-id="1e162-137">premium</span></span>

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

### <span data-ttu-id="1e162-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e162-138">-Tag</span></span>
<span data-ttu-id="1e162-139">Tag delle risorse per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1e162-139">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="1e162-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e162-140">-Confirm</span></span>
<span data-ttu-id="1e162-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e162-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e162-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e162-142">-WhatIf</span></span>
<span data-ttu-id="1e162-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e162-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e162-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e162-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e162-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e162-145">CommonParameters</span></span>
<span data-ttu-id="1e162-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e162-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e162-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e162-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e162-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e162-148">INPUTS</span></span>

### <span data-ttu-id="1e162-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1e162-149">System.String</span></span>

### <span data-ttu-id="1e162-150">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1e162-150">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1e162-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e162-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1e162-152">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1e162-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1e162-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e162-153">OUTPUTS</span></span>

### <span data-ttu-id="1e162-154">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e162-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1e162-155">Note</span><span class="sxs-lookup"><span data-stu-id="1e162-155">NOTES</span></span>

## <span data-ttu-id="1e162-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e162-156">RELATED LINKS</span></span>

[<span data-ttu-id="1e162-157">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="1e162-157">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="1e162-158">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="1e162-158">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


