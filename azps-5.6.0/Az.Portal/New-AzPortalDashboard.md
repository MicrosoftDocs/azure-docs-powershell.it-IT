---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 05627146c0b9984ea5222f70f85f801b374e1321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988999"
---
# <span data-ttu-id="17aa3-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="17aa3-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="17aa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="17aa3-103">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="17aa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17aa3-104">SYNTAX</span></span>

### <span data-ttu-id="17aa3-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17aa3-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17aa3-106">Crea</span><span class="sxs-lookup"><span data-stu-id="17aa3-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17aa3-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="17aa3-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17aa3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17aa3-108">DESCRIPTION</span></span>
<span data-ttu-id="17aa3-109">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="17aa3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17aa3-110">EXAMPLES</span></span>

### <span data-ttu-id="17aa3-111">Esempio 1: Creare un dashboard usando un file di modello di dashboard</span><span class="sxs-lookup"><span data-stu-id="17aa3-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="17aa3-112">Creare un nuovo dashboard usando il file del modello di dashboard fornito.</span><span class="sxs-lookup"><span data-stu-id="17aa3-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="17aa3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17aa3-113">PARAMETERS</span></span>

### <span data-ttu-id="17aa3-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="17aa3-114">-Dashboard</span></span>
<span data-ttu-id="17aa3-115">Definizione di risorsa del dashboard condiviso.</span><span class="sxs-lookup"><span data-stu-id="17aa3-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="17aa3-116">Per creare, vedere la sezione NOTE per le proprietà del DASHBOARD e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="17aa3-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="17aa3-117">-DashboardPath</span></span>
<span data-ttu-id="17aa3-118">Percorso di un modello di dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="17aa3-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="17aa3-119">I modelli di dashboard possono essere scaricati dal portale.</span><span class="sxs-lookup"><span data-stu-id="17aa3-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17aa3-120">-DefaultProfile</span></span>
<span data-ttu-id="17aa3-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17aa3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17aa3-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="17aa3-122">-Lens</span></span>
<span data-ttu-id="17aa3-123">Lenti del dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-124">-Location</span><span class="sxs-lookup"><span data-stu-id="17aa3-124">-Location</span></span>
<span data-ttu-id="17aa3-125">Luogo della risorsa</span><span class="sxs-lookup"><span data-stu-id="17aa3-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="17aa3-126">-Metadata</span></span>
<span data-ttu-id="17aa3-127">Metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="17aa3-128">-Name</span></span>
<span data-ttu-id="17aa3-129">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17aa3-130">-ResourceGroupName</span></span>
<span data-ttu-id="17aa3-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17aa3-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="17aa3-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17aa3-132">-SubscriptionId</span></span>
<span data-ttu-id="17aa3-133">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="17aa3-133">The Azure subscription ID.</span></span>
<span data-ttu-id="17aa3-134">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="17aa3-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="17aa3-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="17aa3-135">-Tag</span></span>
<span data-ttu-id="17aa3-136">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="17aa3-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17aa3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17aa3-137">-Confirm</span></span>
<span data-ttu-id="17aa3-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17aa3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17aa3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17aa3-139">-WhatIf</span></span>
<span data-ttu-id="17aa3-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17aa3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17aa3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17aa3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17aa3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17aa3-142">CommonParameters</span></span>
<span data-ttu-id="17aa3-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17aa3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17aa3-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17aa3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17aa3-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="17aa3-145">INPUTS</span></span>

### <span data-ttu-id="17aa3-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="17aa3-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="17aa3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17aa3-147">OUTPUTS</span></span>

### <span data-ttu-id="17aa3-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="17aa3-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="17aa3-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="17aa3-149">NOTES</span></span>

<span data-ttu-id="17aa3-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="17aa3-150">ALIASES</span></span>

<span data-ttu-id="17aa3-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="17aa3-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17aa3-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="17aa3-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17aa3-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17aa3-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17aa3-154">DASHBOARD: <IDashboard> definizione di risorsa del dashboard condiviso.</span><span class="sxs-lookup"><span data-stu-id="17aa3-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="17aa3-155">`Location <String>`: percorso della risorsa</span><span class="sxs-lookup"><span data-stu-id="17aa3-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="17aa3-156">`[Lens <IDashboardPropertiesLenses>]`: lenti del dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="17aa3-157">`[(Any) <IDashboardLens>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="17aa3-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="17aa3-158">`[Metadata <IDashboardPropertiesMetadata>]`: metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="17aa3-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="17aa3-159">`[(Any) <Object>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="17aa3-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="17aa3-160">`[Tag <IDashboardTags>]`: tag di risorse</span><span class="sxs-lookup"><span data-stu-id="17aa3-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="17aa3-161">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="17aa3-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="17aa3-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17aa3-162">RELATED LINKS</span></span>

