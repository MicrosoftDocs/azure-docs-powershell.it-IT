---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204162"
---
# <span data-ttu-id="eee3b-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="eee3b-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="eee3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee3b-102">SYNOPSIS</span></span>
<span data-ttu-id="eee3b-103">Verificare se è disponibile un nome DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="eee3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eee3b-104">SYNTAX</span></span>

### <span data-ttu-id="eee3b-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eee3b-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eee3b-106">Controlla</span><span class="sxs-lookup"><span data-stu-id="eee3b-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eee3b-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eee3b-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="eee3b-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eee3b-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eee3b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eee3b-109">DESCRIPTION</span></span>
<span data-ttu-id="eee3b-110">Verificare se è disponibile un nome DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="eee3b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eee3b-111">EXAMPLES</span></span>

### <span data-ttu-id="eee3b-112">Esempio 1: Controllare il nome in base alla posizione e al nome.</span><span class="sxs-lookup"><span data-stu-id="eee3b-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="eee3b-113">Verificare la disponibilità del nome per posizione e nome.</span><span class="sxs-lookup"><span data-stu-id="eee3b-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="eee3b-114">Esempio 2: Controllare il nome di DigitalTwinsObject e CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="eee3b-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="eee3b-115">Ottenere A DigitalTwinsInstance e creare un oggetto Requset per testare la disponibilità del nome.</span><span class="sxs-lookup"><span data-stu-id="eee3b-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="eee3b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eee3b-116">PARAMETERS</span></span>

### <span data-ttu-id="eee3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee3b-117">-DefaultProfile</span></span>
<span data-ttu-id="eee3b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eee3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eee3b-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="eee3b-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="eee3b-120">Risultato restituito dalla richiesta di disponibilità di un nome di controllo del database.</span><span class="sxs-lookup"><span data-stu-id="eee3b-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="eee3b-121">Per creare, vedere la sezione NOTE per le proprietà DIGITALTWINSINSTANCECHECKNAME e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eee3b-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eee3b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eee3b-122">-InputObject</span></span>
<span data-ttu-id="eee3b-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eee3b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eee3b-124">-Location</span><span class="sxs-lookup"><span data-stu-id="eee3b-124">-Location</span></span>
<span data-ttu-id="eee3b-125">Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-125">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee3b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="eee3b-126">-Name</span></span>
<span data-ttu-id="eee3b-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eee3b-127">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee3b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eee3b-128">-SubscriptionId</span></span>
<span data-ttu-id="eee3b-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eee3b-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee3b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee3b-130">-Confirm</span></span>
<span data-ttu-id="eee3b-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee3b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee3b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee3b-132">-WhatIf</span></span>
<span data-ttu-id="eee3b-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee3b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee3b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee3b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee3b-135">CommonParameters</span></span>
<span data-ttu-id="eee3b-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee3b-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eee3b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee3b-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="eee3b-138">INPUTS</span></span>

### <span data-ttu-id="eee3b-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="eee3b-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="eee3b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="eee3b-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="eee3b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eee3b-141">OUTPUTS</span></span>

### <span data-ttu-id="eee3b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="eee3b-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="eee3b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="eee3b-143">NOTES</span></span>

<span data-ttu-id="eee3b-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eee3b-144">ALIASES</span></span>

<span data-ttu-id="eee3b-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="eee3b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eee3b-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="eee3b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eee3b-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eee3b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eee3b-148">DIGITALTWINSINSTANCECHECKNAME: risultato restituito dalla richiesta di disponibilità del nome del controllo <ICheckNameRequest> del database.</span><span class="sxs-lookup"><span data-stu-id="eee3b-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="eee3b-149">`Name <String>`: nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eee3b-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="eee3b-150">INPUTOBJECT <IDigitalTwinsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="eee3b-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eee3b-151">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="eee3b-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="eee3b-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="eee3b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eee3b-153">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="eee3b-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="eee3b-155">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="eee3b-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="eee3b-156">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eee3b-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="eee3b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eee3b-157">RELATED LINKS</span></span>

