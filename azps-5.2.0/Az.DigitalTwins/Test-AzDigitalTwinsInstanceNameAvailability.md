---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/test-azdigitaltwinsinstancenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Test-AzDigitalTwinsInstanceNameAvailability.md
ms.openlocfilehash: af911fc4eb4cccbd3f22e0d54a8aad2933b5db46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346927"
---
# <span data-ttu-id="36ae4-101">Test-AzDigitalTwinsInstanceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="36ae4-101">Test-AzDigitalTwinsInstanceNameAvailability</span></span>

## <span data-ttu-id="36ae4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="36ae4-103">Verificare se è disponibile un nome DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-103">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="36ae4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36ae4-104">SYNTAX</span></span>

### <span data-ttu-id="36ae4-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36ae4-105">CheckExpanded (Default)</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String> -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36ae4-106">Controllo</span><span class="sxs-lookup"><span data-stu-id="36ae4-106">Check</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -Location <String>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36ae4-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36ae4-107">CheckViaIdentity</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsInstanceCheckName <ICheckNameRequest> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="36ae4-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36ae4-108">CheckViaIdentityExpanded</span></span>
```
Test-AzDigitalTwinsInstanceNameAvailability -InputObject <IDigitalTwinsIdentity> -Name <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="36ae4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36ae4-109">DESCRIPTION</span></span>
<span data-ttu-id="36ae4-110">Verificare se è disponibile un nome DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-110">Check if a DigitalTwinsInstance name is available.</span></span>

## <span data-ttu-id="36ae4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36ae4-111">EXAMPLES</span></span>

### <span data-ttu-id="36ae4-112">Esempio 1: controllare il nome in base alla posizione e al nome.</span><span class="sxs-lookup"><span data-stu-id="36ae4-112">Example 1: Check the name by location and name.</span></span>
```powershell
PS C:\> Test-AzDigitalTwinsInstanceNameAvailability -Location eastus -name youriTestName

Message                       NameAvailable Reason
-------                       ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="36ae4-113">Verificare la disponibilità del nome in base alla posizione e al nome.</span><span class="sxs-lookup"><span data-stu-id="36ae4-113">Check the availability of the name by location and name.</span></span>

### <span data-ttu-id="36ae4-114">Esempio 2: controllare il nome di DigitalTwinsObject e CheckNameObject.</span><span class="sxs-lookup"><span data-stu-id="36ae4-114">Example 2: Check the name by DigitalTwinsObject and CheckNameObject.</span></span>
```powershell
PS C:\> $getAzDT =Get-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest 
$checkName = New-AzDigitalTwinsCheckNameRequestObject -name youriTestName
Test-AzDigitalTwinsInstanceNameAvailability -InputObject $getAzDT -DigitalTwinsInstanceCheckName $checkName

Message                     NameAvailable Reason
-------                     ------------- ------
'youriTestName' is available. True
```

<span data-ttu-id="36ae4-115">Ottieni un DigitalTwinsInstance e crea un oggetto requset per verificare la disponibilità del nome.</span><span class="sxs-lookup"><span data-stu-id="36ae4-115">Get A DigitalTwinsInstance and create a Requset Object to Test the availability of the name.</span></span>

## <span data-ttu-id="36ae4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36ae4-116">PARAMETERS</span></span>

### <span data-ttu-id="36ae4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ae4-117">-DefaultProfile</span></span>
<span data-ttu-id="36ae4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36ae4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ae4-119">-DigitalTwinsInstanceCheckName</span><span class="sxs-lookup"><span data-stu-id="36ae4-119">-DigitalTwinsInstanceCheckName</span></span>
<span data-ttu-id="36ae4-120">Risultato restituito da una richiesta di verifica della disponibilità dei nomi di database.</span><span class="sxs-lookup"><span data-stu-id="36ae4-120">The result returned from a database check name availability request.</span></span>
<span data-ttu-id="36ae4-121">Per costruire, vedere la sezione Note per le proprietà di DIGITALTWINSINSTANCECHECKNAME e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36ae4-121">To construct, see NOTES section for DIGITALTWINSINSTANCECHECKNAME properties and create a hash table.</span></span>

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

### <span data-ttu-id="36ae4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36ae4-122">-InputObject</span></span>
<span data-ttu-id="36ae4-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36ae4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36ae4-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="36ae4-124">-Location</span></span>
<span data-ttu-id="36ae4-125">Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-125">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="36ae4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="36ae4-126">-Name</span></span>
<span data-ttu-id="36ae4-127">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="36ae4-127">Resource name.</span></span>

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

### <span data-ttu-id="36ae4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36ae4-128">-SubscriptionId</span></span>
<span data-ttu-id="36ae4-129">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="36ae4-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="36ae4-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36ae4-130">-Confirm</span></span>
<span data-ttu-id="36ae4-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36ae4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ae4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ae4-132">-WhatIf</span></span>
<span data-ttu-id="36ae4-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36ae4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ae4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36ae4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ae4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ae4-135">CommonParameters</span></span>
<span data-ttu-id="36ae4-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ae4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ae4-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36ae4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ae4-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36ae4-138">INPUTS</span></span>

### <span data-ttu-id="36ae4-139">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. ICheckNameRequest</span><span class="sxs-lookup"><span data-stu-id="36ae4-139">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameRequest</span></span>

### <span data-ttu-id="36ae4-140">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="36ae4-140">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="36ae4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36ae4-141">OUTPUTS</span></span>

### <span data-ttu-id="36ae4-142">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="36ae4-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.ICheckNameResult</span></span>

## <span data-ttu-id="36ae4-143">Note</span><span class="sxs-lookup"><span data-stu-id="36ae4-143">NOTES</span></span>

<span data-ttu-id="36ae4-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="36ae4-144">ALIASES</span></span>

<span data-ttu-id="36ae4-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36ae4-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36ae4-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="36ae4-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36ae4-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36ae4-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36ae4-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest> : il risultato restituito da una richiesta di disponibilità nome controllo database.</span><span class="sxs-lookup"><span data-stu-id="36ae4-148">DIGITALTWINSINSTANCECHECKNAME <ICheckNameRequest>: The result returned from a database check name availability request.</span></span>
  - <span data-ttu-id="36ae4-149">`Name <String>`: Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="36ae4-149">`Name <String>`: Resource name.</span></span>

<span data-ttu-id="36ae4-150">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="36ae4-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36ae4-151">`[EndpointName <String>]`: Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="36ae4-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="36ae4-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="36ae4-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36ae4-153">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="36ae4-154">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="36ae4-155">`[ResourceName <String>]`: Nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="36ae4-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="36ae4-156">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="36ae4-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="36ae4-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36ae4-157">RELATED LINKS</span></span>

