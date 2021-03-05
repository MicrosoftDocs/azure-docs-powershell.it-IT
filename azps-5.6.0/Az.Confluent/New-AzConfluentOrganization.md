---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012573"
---
# <span data-ttu-id="13590-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="13590-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="13590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13590-102">SYNOPSIS</span></span>
<span data-ttu-id="13590-103">Creare una risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="13590-103">Create Organization resource</span></span>

## <span data-ttu-id="13590-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13590-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="13590-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13590-105">DESCRIPTION</span></span>
<span data-ttu-id="13590-106">Creare una risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="13590-106">Create Organization resource</span></span>

## <span data-ttu-id="13590-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13590-107">EXAMPLES</span></span>

### <span data-ttu-id="13590-108">Esempio 1: Creare un'organizzazione confluente</span><span class="sxs-lookup"><span data-stu-id="13590-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="13590-109">Questo comando crea un'organizzazione confluente.</span><span class="sxs-lookup"><span data-stu-id="13590-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="13590-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13590-110">PARAMETERS</span></span>

### <span data-ttu-id="13590-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13590-111">-AsJob</span></span>
<span data-ttu-id="13590-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="13590-112">Run the command as a job</span></span>

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

### <span data-ttu-id="13590-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13590-113">-DefaultProfile</span></span>
<span data-ttu-id="13590-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13590-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-115">-Location</span><span class="sxs-lookup"><span data-stu-id="13590-115">-Location</span></span>
<span data-ttu-id="13590-116">Posizione della risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="13590-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="13590-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13590-117">-Name</span></span>
<span data-ttu-id="13590-118">Nome risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="13590-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="13590-119">-NoWait</span></span>
<span data-ttu-id="13590-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="13590-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="13590-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="13590-121">-OfferDetailId</span></span>
<span data-ttu-id="13590-122">ID offerta</span><span class="sxs-lookup"><span data-stu-id="13590-122">Offer Id</span></span>

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

### <span data-ttu-id="13590-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="13590-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="13590-124">ID piano offerta</span><span class="sxs-lookup"><span data-stu-id="13590-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="13590-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="13590-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="13590-126">Nome piano offerta</span><span class="sxs-lookup"><span data-stu-id="13590-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="13590-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="13590-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="13590-128">ID autore</span><span class="sxs-lookup"><span data-stu-id="13590-128">Publisher Id</span></span>

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

### <span data-ttu-id="13590-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="13590-129">-OfferDetailStatus</span></span>
<span data-ttu-id="13590-130">Stato offerta SaaS</span><span class="sxs-lookup"><span data-stu-id="13590-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="13590-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="13590-132">Unità di durata piano offerta</span><span class="sxs-lookup"><span data-stu-id="13590-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="13590-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13590-133">-ResourceGroupName</span></span>
<span data-ttu-id="13590-134">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="13590-134">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13590-135">-SubscriptionId</span></span>
<span data-ttu-id="13590-136">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="13590-136">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="13590-137">-Tag</span></span>
<span data-ttu-id="13590-138">Tag di risorse dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="13590-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="13590-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="13590-140">Indirizzo e-mail</span><span class="sxs-lookup"><span data-stu-id="13590-140">Email address</span></span>

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

### <span data-ttu-id="13590-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="13590-141">-UserDetailFirstName</span></span>
<span data-ttu-id="13590-142">Nome</span><span class="sxs-lookup"><span data-stu-id="13590-142">First name</span></span>

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

### <span data-ttu-id="13590-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="13590-143">-UserDetailLastName</span></span>
<span data-ttu-id="13590-144">Cognome</span><span class="sxs-lookup"><span data-stu-id="13590-144">Last name</span></span>

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

### <span data-ttu-id="13590-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13590-145">-Confirm</span></span>
<span data-ttu-id="13590-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13590-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13590-147">-WhatIf</span></span>
<span data-ttu-id="13590-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13590-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13590-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="13590-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13590-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13590-150">CommonParameters</span></span>
<span data-ttu-id="13590-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13590-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13590-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13590-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13590-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="13590-153">INPUTS</span></span>

## <span data-ttu-id="13590-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13590-154">OUTPUTS</span></span>

### <span data-ttu-id="13590-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="13590-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="13590-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="13590-156">NOTES</span></span>

<span data-ttu-id="13590-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="13590-157">ALIASES</span></span>

## <span data-ttu-id="13590-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13590-158">RELATED LINKS</span></span>

