---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988944"
---
# <span data-ttu-id="34141-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="34141-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="34141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34141-102">SYNOPSIS</span></span>
<span data-ttu-id="34141-103">Aggiorna un dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="34141-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="34141-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34141-104">SYNTAX</span></span>

### <span data-ttu-id="34141-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34141-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="34141-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="34141-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="34141-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34141-107">DESCRIPTION</span></span>
<span data-ttu-id="34141-108">Aggiorna un dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="34141-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="34141-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34141-109">EXAMPLES</span></span>

### <span data-ttu-id="34141-110">Esempio 1: Aggiornare i tag di un dashboard</span><span class="sxs-lookup"><span data-stu-id="34141-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="34141-111">Aggiornare i tag in un dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="34141-112">I tag sono rappresentati come tabella hash in linea.</span><span class="sxs-lookup"><span data-stu-id="34141-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="34141-113">Esempio 2: Aggiornare i tag del dashboard usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="34141-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="34141-114">Aggiornare i tag in un dashboard di nuovo usando Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="34141-115">Questa opzione può essere usata per aggiornare i tag in un singolo dashboard o in più dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="34141-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34141-116">PARAMETERS</span></span>

### <span data-ttu-id="34141-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34141-117">-DefaultProfile</span></span>
<span data-ttu-id="34141-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34141-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34141-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34141-119">-InputObject</span></span>
<span data-ttu-id="34141-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="34141-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34141-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="34141-121">-Lens</span></span>
<span data-ttu-id="34141-122">Lenti del dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="34141-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="34141-123">-Metadata</span></span>
<span data-ttu-id="34141-124">Metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="34141-125">-Name</span><span class="sxs-lookup"><span data-stu-id="34141-125">-Name</span></span>
<span data-ttu-id="34141-126">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34141-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34141-127">-ResourceGroupName</span></span>
<span data-ttu-id="34141-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34141-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="34141-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34141-129">-SubscriptionId</span></span>
<span data-ttu-id="34141-130">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34141-130">The Azure subscription ID.</span></span>
<span data-ttu-id="34141-131">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="34141-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34141-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="34141-132">-Tag</span></span>
<span data-ttu-id="34141-133">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="34141-133">Resource tags</span></span>

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

### <span data-ttu-id="34141-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34141-134">-Confirm</span></span>
<span data-ttu-id="34141-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34141-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34141-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34141-136">-WhatIf</span></span>
<span data-ttu-id="34141-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34141-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34141-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34141-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34141-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34141-139">CommonParameters</span></span>
<span data-ttu-id="34141-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34141-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34141-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34141-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34141-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="34141-142">INPUTS</span></span>

### <span data-ttu-id="34141-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="34141-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="34141-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34141-144">OUTPUTS</span></span>

### <span data-ttu-id="34141-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="34141-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="34141-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="34141-146">NOTES</span></span>

<span data-ttu-id="34141-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="34141-147">ALIASES</span></span>

<span data-ttu-id="34141-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="34141-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34141-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="34141-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34141-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34141-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34141-151">INPUTOBJECT <IPortalIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="34141-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34141-152">`[DashboardName <String>]`: nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="34141-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="34141-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="34141-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34141-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34141-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="34141-155">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="34141-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="34141-156">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-000000000000000.</span><span class="sxs-lookup"><span data-stu-id="34141-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="34141-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34141-157">RELATED LINKS</span></span>

