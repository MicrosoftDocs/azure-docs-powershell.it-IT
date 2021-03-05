---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 967b50b024e02d4a88fa2a1d91905acad5385b6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984884"
---
# <span data-ttu-id="76d72-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76d72-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="76d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d72-102">SYNOPSIS</span></span>
<span data-ttu-id="76d72-103">Aggiornare i metadati di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="76d72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76d72-104">SYNTAX</span></span>

### <span data-ttu-id="76d72-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76d72-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76d72-106">Aggiorna</span><span class="sxs-lookup"><span data-stu-id="76d72-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76d72-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76d72-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76d72-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="76d72-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76d72-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="76d72-109">DESCRIPTION</span></span>
<span data-ttu-id="76d72-110">Aggiornare i metadati di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="76d72-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76d72-111">EXAMPLES</span></span>

### <span data-ttu-id="76d72-112">Esempio 1: UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76d72-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="76d72-113">Aggiornare l'istanza di DigitalTwinsInstance specificata in base a ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d72-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="76d72-114">Esempio 2: Aggiornare AzDigitalTwinsInstance da un altro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76d72-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="76d72-115">Aggiornare AzDigitalTwinsInstance da un altro AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="76d72-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="76d72-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76d72-116">PARAMETERS</span></span>

### <span data-ttu-id="76d72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d72-117">-DefaultProfile</span></span>
<span data-ttu-id="76d72-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76d72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d72-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="76d72-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="76d72-120">Descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="76d72-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="76d72-121">Per creare, vedere la sezione NOTE per le proprietà DIGITALTWINSPATCHDESCRIPTION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="76d72-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76d72-122">-InputObject</span></span>
<span data-ttu-id="76d72-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="76d72-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d72-124">-ResourceGroupName</span></span>
<span data-ttu-id="76d72-125">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="76d72-126">-ResourceName</span></span>
<span data-ttu-id="76d72-127">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76d72-128">-SubscriptionId</span></span>
<span data-ttu-id="76d72-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="76d72-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="76d72-130">-Tag</span></span>
<span data-ttu-id="76d72-131">Tag di istanza</span><span class="sxs-lookup"><span data-stu-id="76d72-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d72-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76d72-132">-Confirm</span></span>
<span data-ttu-id="76d72-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76d72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d72-134">-WhatIf</span></span>
<span data-ttu-id="76d72-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76d72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d72-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76d72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d72-137">CommonParameters</span></span>
<span data-ttu-id="76d72-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d72-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76d72-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d72-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="76d72-140">INPUTS</span></span>

### <span data-ttu-id="76d72-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="76d72-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="76d72-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="76d72-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="76d72-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76d72-143">OUTPUTS</span></span>

### <span data-ttu-id="76d72-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="76d72-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="76d72-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="76d72-145">NOTES</span></span>

<span data-ttu-id="76d72-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="76d72-146">ALIASES</span></span>

<span data-ttu-id="76d72-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="76d72-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76d72-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="76d72-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76d72-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76d72-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76d72-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> descrizione del servizio DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="76d72-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="76d72-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: tag di istanza</span><span class="sxs-lookup"><span data-stu-id="76d72-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="76d72-152">`[(Any) <String>]`: indica che è possibile aggiungere qualsiasi proprietà all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="76d72-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="76d72-153">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="76d72-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76d72-154">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="76d72-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="76d72-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="76d72-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76d72-156">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76d72-157">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76d72-158">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="76d72-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="76d72-159">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="76d72-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="76d72-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76d72-160">RELATED LINKS</span></span>

