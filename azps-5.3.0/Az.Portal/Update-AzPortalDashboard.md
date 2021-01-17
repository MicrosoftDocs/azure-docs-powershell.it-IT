---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378531"
---
# <span data-ttu-id="6c4f6-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="6c4f6-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="6c4f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4f6-103">Aggiorna un dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="6c4f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-104">SYNTAX</span></span>

### <span data-ttu-id="6c4f6-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c4f6-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6c4f6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6c4f6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c4f6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c4f6-107">DESCRIPTION</span></span>
<span data-ttu-id="6c4f6-108">Aggiorna un dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="6c4f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-109">EXAMPLES</span></span>

### <span data-ttu-id="6c4f6-110">Esempio 1: aggiornare i tag di un dashboard</span><span class="sxs-lookup"><span data-stu-id="6c4f6-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="6c4f6-111">Aggiornare i tag in un dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="6c4f6-112">I tag sono rappresentati come Hashtable inline.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="6c4f6-113">Esempio 2: aggiornare i tag del dashboard usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="6c4f6-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="6c4f6-114">Aggiornare i tag in un dashboard riprovati usando Get-AzPortalDashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="6c4f6-115">Può essere usato per aggiornare i tag in un singolo dashboard o in più dashboardfs.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="6c4f6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-116">PARAMETERS</span></span>

### <span data-ttu-id="6c4f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4f6-117">-DefaultProfile</span></span>
<span data-ttu-id="6c4f6-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4f6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c4f6-119">-InputObject</span></span>
<span data-ttu-id="6c4f6-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6c4f6-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="6c4f6-121">-Lens</span></span>
<span data-ttu-id="6c4f6-122">Obiettivi del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="6c4f6-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6c4f6-123">-Metadata</span></span>
<span data-ttu-id="6c4f6-124">Metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="6c4f6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c4f6-125">-Name</span></span>
<span data-ttu-id="6c4f6-126">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="6c4f6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4f6-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c4f6-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c4f6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c4f6-129">-SubscriptionId</span></span>
<span data-ttu-id="6c4f6-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-130">The Azure subscription ID.</span></span>
<span data-ttu-id="6c4f6-131">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6c4f6-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6c4f6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c4f6-132">-Tag</span></span>
<span data-ttu-id="6c4f6-133">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="6c4f6-133">Resource tags</span></span>

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

### <span data-ttu-id="6c4f6-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c4f6-134">-Confirm</span></span>
<span data-ttu-id="6c4f6-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4f6-136">-WhatIf</span></span>
<span data-ttu-id="6c4f6-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4f6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4f6-139">CommonParameters</span></span>
<span data-ttu-id="6c4f6-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4f6-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c4f6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4f6-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-142">INPUTS</span></span>

### <span data-ttu-id="6c4f6-143">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="6c4f6-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="6c4f6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c4f6-144">OUTPUTS</span></span>

### <span data-ttu-id="6c4f6-145">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="6c4f6-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="6c4f6-146">Note</span><span class="sxs-lookup"><span data-stu-id="6c4f6-146">NOTES</span></span>

<span data-ttu-id="6c4f6-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6c4f6-147">ALIASES</span></span>

<span data-ttu-id="6c4f6-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6c4f6-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6c4f6-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6c4f6-151">INPUTOBJECT <IPortalIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6c4f6-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6c4f6-152">`[DashboardName <String>]`: Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="6c4f6-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6c4f6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6c4f6-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6c4f6-155">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4f6-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6c4f6-156">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="6c4f6-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6c4f6-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c4f6-157">RELATED LINKS</span></span>

