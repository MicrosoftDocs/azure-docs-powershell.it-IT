---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsplan
schema: 2.0.0
ms.openlocfilehash: 2e78b28705b625836d9020c5ddf1652f4bdc7a7d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023058"
---
# <span data-ttu-id="2f593-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="2f593-101">Set-AzsPlan</span></span>

## <span data-ttu-id="2f593-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f593-102">SYNOPSIS</span></span>
<span data-ttu-id="2f593-103">Creare o aggiornare il piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-103">Create or update the plan.</span></span>

## <span data-ttu-id="2f593-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f593-104">SYNTAX</span></span>

### <span data-ttu-id="2f593-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f593-105">UpdateExpanded (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>] [-PropertiesName <String>]
 [-QuotaIds <String[]>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2f593-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2f593-106">Update</span></span>
```
Set-AzsPlan -PlanDefinition <IPlan> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f593-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f593-107">DESCRIPTION</span></span>
<span data-ttu-id="2f593-108">Creare o aggiornare il piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-108">Create or update the plan.</span></span>

## <span data-ttu-id="2f593-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f593-109">EXAMPLES</span></span>

### <span data-ttu-id="2f593-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2f593-110">Example 1</span></span>
```powershell
PS C:\> $Plan = Get-AzsPlan | Select-Object -First 1
$Plan.Description = 'update plan'
$Plan | Set-AzsPlan

Description         : update plan
DisplayName         : DRPTestPlan5056-test-test-test
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056
Location            : redmond
Name                : DRPTestPlan5056
PropertiesName      : DRPTestPlan5056
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Storage.Admin/locations/redmond/quotas/Default Quota, 
                      /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Compute.Admin/locations/redmond/quotas/Default Quota}
SkuIds              : 
SubscriptionCount   : 5
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="2f593-111">Aggiorna il piano specificato</span><span class="sxs-lookup"><span data-stu-id="2f593-111">Updates the specified plan</span></span>

## <span data-ttu-id="2f593-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f593-112">PARAMETERS</span></span>

### <span data-ttu-id="2f593-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f593-113">-DefaultProfile</span></span>
<span data-ttu-id="2f593-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f593-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f593-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f593-115">-Description</span></span>
<span data-ttu-id="2f593-116">Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-116">Description of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f593-117">-DisplayName</span></span>
<span data-ttu-id="2f593-118">Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2f593-118">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2f593-119">-ExternalReferenceId</span></span>
<span data-ttu-id="2f593-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="2f593-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2f593-121">-Location</span></span>
<span data-ttu-id="2f593-122">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="2f593-122">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f593-123">-Name</span></span>
<span data-ttu-id="2f593-124">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-124">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="2f593-125">-PlanDefinition</span></span>
<span data-ttu-id="2f593-126">Un piano rappresenta un pacchetto di quote e funzionalità offerte dai tenant.</span><span class="sxs-lookup"><span data-stu-id="2f593-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="2f593-127">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="2f593-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="2f593-128">Per costruire, vedere la sezione Note per le proprietà di PLANDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2f593-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-129">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="2f593-129">-PropertiesName</span></span>
<span data-ttu-id="2f593-130">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-130">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="2f593-131">-QuotaIds</span></span>
<span data-ttu-id="2f593-132">Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f593-133">-ResourceGroupName</span></span>
<span data-ttu-id="2f593-134">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f593-134">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="2f593-135">-SkuIds</span></span>
<span data-ttu-id="2f593-136">Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="2f593-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="2f593-137">-SubscriptionCount</span></span>
<span data-ttu-id="2f593-138">Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="2f593-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f593-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f593-139">-SubscriptionId</span></span>
<span data-ttu-id="2f593-140">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2f593-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2f593-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2f593-141">-Confirm</span></span>
<span data-ttu-id="2f593-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f593-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f593-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f593-143">-WhatIf</span></span>
<span data-ttu-id="2f593-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f593-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f593-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f593-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f593-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f593-146">CommonParameters</span></span>
<span data-ttu-id="2f593-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f593-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f593-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f593-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f593-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f593-149">INPUTS</span></span>

### <span data-ttu-id="2f593-150">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="2f593-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="2f593-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f593-151">OUTPUTS</span></span>

### <span data-ttu-id="2f593-152">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="2f593-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="2f593-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2f593-153">ALIASES</span></span>

## <span data-ttu-id="2f593-154">Note</span><span class="sxs-lookup"><span data-stu-id="2f593-154">NOTES</span></span>

<span data-ttu-id="2f593-155">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2f593-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f593-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f593-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2f593-157">PLANDEFINITION <IPlan> : un piano rappresenta un pacchetto di quote e funzionalità disponibili per i tenant.</span><span class="sxs-lookup"><span data-stu-id="2f593-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="2f593-158">Un tenant può acquisire questo piano tramite un'offerta per aggiornare l'accesso ai servizi cloud sottostanti.</span><span class="sxs-lookup"><span data-stu-id="2f593-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="2f593-159">`[Location <String>]`: Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="2f593-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="2f593-160">`[Description <String>]`: Descrizione del piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="2f593-161">`[DisplayName <String>]`: Nome visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2f593-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="2f593-162">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="2f593-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="2f593-163">`[PropertiesName <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2f593-164">`[QuotaIds <String[]>]`: Identificatori di quota nel piano.</span><span class="sxs-lookup"><span data-stu-id="2f593-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="2f593-165">`[SkuIds <String[]>]`: Identificatori SKU.</span><span class="sxs-lookup"><span data-stu-id="2f593-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="2f593-166">`[SubscriptionCount <Int32?>]`: Conteggio abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="2f593-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="2f593-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f593-167">RELATED LINKS</span></span>

