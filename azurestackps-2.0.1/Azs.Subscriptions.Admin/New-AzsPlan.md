---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023148"
---
# <span data-ttu-id="09357-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="09357-101">New-AzsPlan</span></span>

## <span data-ttu-id="09357-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09357-102">SYNOPSIS</span></span>
<span data-ttu-id="09357-103">Creare o aggiornare il piano.</span><span class="sxs-lookup"><span data-stu-id="09357-103">Create or update the plan.</span></span>

## <span data-ttu-id="09357-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09357-104">SYNTAX</span></span>

### <span data-ttu-id="09357-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09357-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09357-106">Creare</span><span class="sxs-lookup"><span data-stu-id="09357-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09357-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09357-107">DESCRIPTION</span></span>
<span data-ttu-id="09357-108">Creare o aggiornare il piano.</span><span class="sxs-lookup"><span data-stu-id="09357-108">Create or update the plan.</span></span>

## <span data-ttu-id="09357-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09357-109">EXAMPLES</span></span>

### <span data-ttu-id="09357-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09357-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="09357-111">Crea un nuovo piano</span><span class="sxs-lookup"><span data-stu-id="09357-111">Creates a new plan</span></span>

## <span data-ttu-id="09357-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09357-112">PARAMETERS</span></span>

### <span data-ttu-id="09357-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09357-113">-DefaultProfile</span></span>
<span data-ttu-id="09357-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09357-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09357-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="09357-115">-Description</span></span>
<span data-ttu-id="09357-116">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="09357-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09357-117">-DisplayName</span></span>
<span data-ttu-id="09357-118">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="09357-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="09357-119">-ExternalReferenceId</span></span>
<span data-ttu-id="09357-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="09357-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="09357-121">-Location</span></span>
<span data-ttu-id="09357-122">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="09357-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="09357-123">-Name</span></span>
<span data-ttu-id="09357-124">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="09357-124">Name of the plan.</span></span>

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

### <span data-ttu-id="09357-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="09357-125">-PlanDefinition</span></span>
<span data-ttu-id="09357-126">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="09357-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="09357-127">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="09357-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="09357-128">Per costruire, vedere la sezione Note per le proprietà di PLANDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09357-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="09357-129">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="09357-129">-PropertiesName</span></span>
<span data-ttu-id="09357-130">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="09357-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="09357-131">-QuotaIds</span></span>
<span data-ttu-id="09357-132">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="09357-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09357-133">-ResourceGroupName</span></span>
<span data-ttu-id="09357-134">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="09357-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="09357-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="09357-135">-SkuIds</span></span>
<span data-ttu-id="09357-136">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="09357-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="09357-137">-SubscriptionCount</span></span>
<span data-ttu-id="09357-138">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="09357-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09357-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09357-139">-SubscriptionId</span></span>
<span data-ttu-id="09357-140">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="09357-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09357-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09357-141">-Confirm</span></span>
<span data-ttu-id="09357-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09357-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09357-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09357-143">-WhatIf</span></span>
<span data-ttu-id="09357-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09357-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09357-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09357-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09357-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09357-146">CommonParameters</span></span>
<span data-ttu-id="09357-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09357-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09357-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09357-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09357-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09357-149">INPUTS</span></span>

### <span data-ttu-id="09357-150">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="09357-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="09357-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09357-151">OUTPUTS</span></span>

### <span data-ttu-id="09357-152">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="09357-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="09357-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="09357-153">ALIASES</span></span>

## <span data-ttu-id="09357-154">Note</span><span class="sxs-lookup"><span data-stu-id="09357-154">NOTES</span></span>

<span data-ttu-id="09357-155">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="09357-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09357-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09357-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="09357-157">PLANDEFINITION <IPlan> : un piano rappresenta un pacchetto di quote e funzionalità disponibili per i tenant.</span><span class="sxs-lookup"><span data-stu-id="09357-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="09357-158">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="09357-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="09357-159">`[Location <String>]`: Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="09357-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="09357-160">`[Description <String>]`: Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="09357-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="09357-161">`[DisplayName <String>]`: Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="09357-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="09357-162">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="09357-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="09357-163">`[PropertiesName <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="09357-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="09357-164">`[QuotaIds <String[]>]`: Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="09357-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="09357-165">`[SkuIds <String[]>]`: Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="09357-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="09357-166">`[SubscriptionCount <Int32?>]`: Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="09357-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="09357-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09357-167">RELATED LINKS</span></span>

