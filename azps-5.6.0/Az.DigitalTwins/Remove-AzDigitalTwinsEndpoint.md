---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: f7d8b5665ff150e0501d77a76c2dde7e4a947cb5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984926"
---
# <span data-ttu-id="fff18-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="fff18-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="fff18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fff18-102">SYNOPSIS</span></span>
<span data-ttu-id="fff18-103">Eliminare un endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="fff18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fff18-104">SYNTAX</span></span>

### <span data-ttu-id="fff18-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fff18-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="fff18-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fff18-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fff18-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fff18-107">DESCRIPTION</span></span>
<span data-ttu-id="fff18-108">Eliminare un endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="fff18-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fff18-109">EXAMPLES</span></span>

### <span data-ttu-id="fff18-110">Esempio 1: Eliminare azDigitalTwinsEndPoint da EndPointName</span><span class="sxs-lookup"><span data-stu-id="fff18-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="fff18-111">Eliminare azDigitalTwinsEndPoint da EndPointName ResourceGroupName e ResourceName</span><span class="sxs-lookup"><span data-stu-id="fff18-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="fff18-112">Esempio 2: Eliminare il file azDigitalTwinsEndPoint in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="fff18-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="fff18-113">Eliminare il valore azDigitalTwinsEndPoint in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="fff18-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="fff18-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fff18-114">PARAMETERS</span></span>

### <span data-ttu-id="fff18-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fff18-115">-AsJob</span></span>
<span data-ttu-id="fff18-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fff18-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fff18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff18-117">-DefaultProfile</span></span>
<span data-ttu-id="fff18-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fff18-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fff18-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fff18-119">-EndpointName</span></span>
<span data-ttu-id="fff18-120">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="fff18-120">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff18-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fff18-121">-InputObject</span></span>
<span data-ttu-id="fff18-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fff18-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fff18-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fff18-123">-NoWait</span></span>
<span data-ttu-id="fff18-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fff18-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fff18-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fff18-125">-PassThru</span></span>
<span data-ttu-id="fff18-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="fff18-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fff18-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fff18-127">-ResourceGroupName</span></span>
<span data-ttu-id="fff18-128">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff18-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fff18-129">-ResourceName</span></span>
<span data-ttu-id="fff18-130">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-130">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff18-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fff18-131">-SubscriptionId</span></span>
<span data-ttu-id="fff18-132">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fff18-132">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fff18-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fff18-133">-Confirm</span></span>
<span data-ttu-id="fff18-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff18-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff18-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff18-135">-WhatIf</span></span>
<span data-ttu-id="fff18-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fff18-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fff18-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fff18-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff18-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff18-138">CommonParameters</span></span>
<span data-ttu-id="fff18-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff18-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff18-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fff18-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff18-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="fff18-141">INPUTS</span></span>

### <span data-ttu-id="fff18-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="fff18-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="fff18-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fff18-143">OUTPUTS</span></span>

### <span data-ttu-id="fff18-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="fff18-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="fff18-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="fff18-145">NOTES</span></span>

<span data-ttu-id="fff18-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fff18-146">ALIASES</span></span>

<span data-ttu-id="fff18-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="fff18-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fff18-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fff18-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fff18-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fff18-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fff18-150">INPUTOBJECT <IDigitalTwinsIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="fff18-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fff18-151">`[EndpointName <String>]`: nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="fff18-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="fff18-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="fff18-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fff18-153">`[Location <String>]`: posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="fff18-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="fff18-155">`[ResourceName <String>]`: nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="fff18-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="fff18-156">`[SubscriptionId <String>]`: l'identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fff18-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="fff18-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fff18-157">RELATED LINKS</span></span>

