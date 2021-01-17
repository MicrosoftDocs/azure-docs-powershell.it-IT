---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473946"
---
# <span data-ttu-id="4cd98-101">Remove-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4cd98-101">Remove-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="4cd98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4cd98-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd98-103">Eliminare un endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-103">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="4cd98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cd98-104">SYNTAX</span></span>

### <span data-ttu-id="4cd98-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4cd98-105">Delete (Default)</span></span>
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4cd98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4cd98-106">DeleteViaIdentity</span></span>
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4cd98-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cd98-107">DESCRIPTION</span></span>
<span data-ttu-id="4cd98-108">Eliminare un endpoint DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-108">Delete a DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="4cd98-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cd98-109">EXAMPLES</span></span>

### <span data-ttu-id="4cd98-110">Esempio 1: eliminare il azDigitalTwinsEndPoint per EndPointname</span><span class="sxs-lookup"><span data-stu-id="4cd98-110">Example 1: Delete the azDigitalTwinsEndPoint by EndPointName</span></span>
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

<span data-ttu-id="4cd98-111">Eliminare il azDigitalTwinsEndPoint per EndPointname ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="4cd98-111">Delete the azDigitalTwinsEndPoint by EndPointName ResourceGroupName and ResourceName</span></span>

### <span data-ttu-id="4cd98-112">Esempio 2: eliminare il azDigitalTwinsEndPoint per oggetto</span><span class="sxs-lookup"><span data-stu-id="4cd98-112">Example 2: Delete the azDigitalTwinsEndPoint by Object</span></span>
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

<span data-ttu-id="4cd98-113">Eliminare il azDigitalTwinsEndPoint per oggetto</span><span class="sxs-lookup"><span data-stu-id="4cd98-113">Delete the azDigitalTwinsEndPoint by Object</span></span>

## <span data-ttu-id="4cd98-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cd98-114">PARAMETERS</span></span>

### <span data-ttu-id="4cd98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cd98-115">-AsJob</span></span>
<span data-ttu-id="4cd98-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4cd98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4cd98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd98-117">-DefaultProfile</span></span>
<span data-ttu-id="4cd98-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cd98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cd98-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4cd98-119">-EndpointName</span></span>
<span data-ttu-id="4cd98-120">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="4cd98-120">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="4cd98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cd98-121">-InputObject</span></span>
<span data-ttu-id="4cd98-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4cd98-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cd98-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="4cd98-123">-NoWait</span></span>
<span data-ttu-id="4cd98-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4cd98-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4cd98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cd98-125">-PassThru</span></span>
<span data-ttu-id="4cd98-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="4cd98-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4cd98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd98-127">-ResourceGroupName</span></span>
<span data-ttu-id="4cd98-128">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-128">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4cd98-129">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4cd98-129">-ResourceName</span></span>
<span data-ttu-id="4cd98-130">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-130">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="4cd98-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cd98-131">-SubscriptionId</span></span>
<span data-ttu-id="4cd98-132">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4cd98-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="4cd98-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4cd98-133">-Confirm</span></span>
<span data-ttu-id="4cd98-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cd98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd98-135">-WhatIf</span></span>
<span data-ttu-id="4cd98-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cd98-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd98-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4cd98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cd98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd98-138">CommonParameters</span></span>
<span data-ttu-id="4cd98-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd98-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cd98-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd98-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4cd98-141">INPUTS</span></span>

### <span data-ttu-id="4cd98-142">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="4cd98-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="4cd98-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cd98-143">OUTPUTS</span></span>

### <span data-ttu-id="4cd98-144">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="4cd98-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="4cd98-145">Note</span><span class="sxs-lookup"><span data-stu-id="4cd98-145">NOTES</span></span>

<span data-ttu-id="4cd98-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4cd98-146">ALIASES</span></span>

<span data-ttu-id="4cd98-147">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4cd98-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4cd98-148">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4cd98-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cd98-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4cd98-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4cd98-150">INPUTOBJECT <IDigitalTwinsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4cd98-150">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4cd98-151">`[EndpointName <String>]`: Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="4cd98-151">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="4cd98-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="4cd98-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4cd98-153">`[Location <String>]`: Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-153">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4cd98-154">`[ResourceGroupName <String>]`: Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4cd98-155">`[ResourceName <String>]`: Nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="4cd98-155">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="4cd98-156">`[SubscriptionId <String>]`: Identificatore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4cd98-156">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4cd98-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cd98-157">RELATED LINKS</span></span>

