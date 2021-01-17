---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370898"
---
# <span data-ttu-id="f05c1-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f05c1-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="f05c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f05c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f05c1-103">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f05c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f05c1-104">SYNTAX</span></span>

### <span data-ttu-id="f05c1-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f05c1-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f05c1-106">Creare</span><span class="sxs-lookup"><span data-stu-id="f05c1-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f05c1-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="f05c1-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f05c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f05c1-108">DESCRIPTION</span></span>
<span data-ttu-id="f05c1-109">Crea o aggiorna un dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="f05c1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f05c1-110">EXAMPLES</span></span>

### <span data-ttu-id="f05c1-111">Esempio 1: creare un dashboard usando un file modello di dashboard</span><span class="sxs-lookup"><span data-stu-id="f05c1-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="f05c1-112">Creare un nuovo dashboard usando il file del modello di dashboard specificato.</span><span class="sxs-lookup"><span data-stu-id="f05c1-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="f05c1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f05c1-113">PARAMETERS</span></span>

### <span data-ttu-id="f05c1-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="f05c1-114">-Dashboard</span></span>
<span data-ttu-id="f05c1-115">Definizione della risorsa dashboard condivisa.</span><span class="sxs-lookup"><span data-stu-id="f05c1-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="f05c1-116">Per costruire, vedere la sezione Note per le proprietà del DASHBOARD e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f05c1-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="f05c1-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="f05c1-117">-DashboardPath</span></span>
<span data-ttu-id="f05c1-118">Il percorso di un modello di dashboard esistente.</span><span class="sxs-lookup"><span data-stu-id="f05c1-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="f05c1-119">I modelli di dashboard possono essere scaricati dal portale.</span><span class="sxs-lookup"><span data-stu-id="f05c1-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="f05c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05c1-120">-DefaultProfile</span></span>
<span data-ttu-id="f05c1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f05c1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05c1-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="f05c1-122">-Lens</span></span>
<span data-ttu-id="f05c1-123">Obiettivi del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="f05c1-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f05c1-124">-Location</span></span>
<span data-ttu-id="f05c1-125">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="f05c1-125">Resource location</span></span>

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

### <span data-ttu-id="f05c1-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f05c1-126">-Metadata</span></span>
<span data-ttu-id="f05c1-127">Metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="f05c1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f05c1-128">-Name</span></span>
<span data-ttu-id="f05c1-129">Nome del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="f05c1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05c1-130">-ResourceGroupName</span></span>
<span data-ttu-id="f05c1-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f05c1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="f05c1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f05c1-132">-SubscriptionId</span></span>
<span data-ttu-id="f05c1-133">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="f05c1-133">The Azure subscription ID.</span></span>
<span data-ttu-id="f05c1-134">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f05c1-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="f05c1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f05c1-135">-Tag</span></span>
<span data-ttu-id="f05c1-136">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="f05c1-136">Resource tags</span></span>

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

### <span data-ttu-id="f05c1-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f05c1-137">-Confirm</span></span>
<span data-ttu-id="f05c1-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f05c1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f05c1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05c1-139">-WhatIf</span></span>
<span data-ttu-id="f05c1-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f05c1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05c1-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f05c1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f05c1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05c1-142">CommonParameters</span></span>
<span data-ttu-id="f05c1-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05c1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05c1-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f05c1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05c1-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f05c1-145">INPUTS</span></span>

### <span data-ttu-id="f05c1-146">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="f05c1-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f05c1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f05c1-147">OUTPUTS</span></span>

### <span data-ttu-id="f05c1-148">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="f05c1-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f05c1-149">Note</span><span class="sxs-lookup"><span data-stu-id="f05c1-149">NOTES</span></span>

<span data-ttu-id="f05c1-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f05c1-150">ALIASES</span></span>

<span data-ttu-id="f05c1-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f05c1-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f05c1-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f05c1-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f05c1-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f05c1-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f05c1-154">DASHBOARD <IDashboard> : definizione della risorsa dashboard condivisa.</span><span class="sxs-lookup"><span data-stu-id="f05c1-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="f05c1-155">`Location <String>`: Percorso delle risorse</span><span class="sxs-lookup"><span data-stu-id="f05c1-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="f05c1-156">`[Lens <IDashboardPropertiesLenses>]`: Gli obiettivi del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="f05c1-157">`[(Any) <IDashboardLens>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f05c1-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f05c1-158">`[Metadata <IDashboardPropertiesMetadata>]`: I metadati del dashboard.</span><span class="sxs-lookup"><span data-stu-id="f05c1-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="f05c1-159">`[(Any) <Object>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f05c1-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f05c1-160">`[Tag <IDashboardTags>]`: Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="f05c1-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="f05c1-161">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="f05c1-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="f05c1-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f05c1-162">RELATED LINKS</span></span>

