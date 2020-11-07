---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861530"
---
# <span data-ttu-id="6a5be-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="6a5be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a5be-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5be-103">Aggiorna le proprietà di una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6a5be-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="6a5be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a5be-104">SYNTAX</span></span>

### <span data-ttu-id="6a5be-105">Campi</span><span class="sxs-lookup"><span data-stu-id="6a5be-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a5be-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="6a5be-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a5be-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a5be-107">DESCRIPTION</span></span>
<span data-ttu-id="6a5be-108">Il cmdlet **set-AzDnsZone** aggiorna la zona DNS specificata nel servizio Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="6a5be-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="6a5be-109">Questo cmdlet non aggiorna i set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="6a5be-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="6a5be-110">Puoi passare un oggetto **dnsZone** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6a5be-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="6a5be-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6a5be-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="6a5be-112">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="6a5be-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6a5be-113">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="6a5be-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6a5be-114">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="6a5be-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="6a5be-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a5be-115">EXAMPLES</span></span>

### <span data-ttu-id="6a5be-116">Esempio 1: aggiornare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="6a5be-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="6a5be-117">Il primo comando consente di ottenere la zona denominata myzone.com dal gruppo di risorse specificato e quindi di archiviarla nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="6a5be-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="6a5be-118">Il secondo comando Aggiorna i tag per $Zone.</span><span class="sxs-lookup"><span data-stu-id="6a5be-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="6a5be-119">Il comando finale conferma la modifica.</span><span class="sxs-lookup"><span data-stu-id="6a5be-119">The final command commits the change.</span></span>

### <span data-ttu-id="6a5be-120">Esempio 2: aggiornare i tag per una zona</span><span class="sxs-lookup"><span data-stu-id="6a5be-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="6a5be-121">Questo comando Aggiorna i tag per la zona denominata myzone.com senza prima ottenere esplicitamente la zona.</span><span class="sxs-lookup"><span data-stu-id="6a5be-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="6a5be-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a5be-122">PARAMETERS</span></span>

### <span data-ttu-id="6a5be-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a5be-123">-Name</span></span>
<span data-ttu-id="6a5be-124">Specifica il nome della zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6a5be-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="6a5be-125">-Overwrite</span></span>
<span data-ttu-id="6a5be-126">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="6a5be-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="6a5be-127">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="6a5be-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="6a5be-128">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="6a5be-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5be-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a5be-130">Specifica il nome del gruppo di risorse che contiene la zona da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6a5be-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="6a5be-131">Devi anche specificare il parametro zonename.</span><span class="sxs-lookup"><span data-stu-id="6a5be-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="6a5be-132">In alternativa, puoi specificare la zona usando un oggetto DnsZone con il parametro *zone* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a5be-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a5be-133">-Tag</span></span>
<span data-ttu-id="6a5be-134">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6a5be-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a5be-135">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6a5be-135">For example:</span></span>

<span data-ttu-id="6a5be-136">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6a5be-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-137">-Zona</span><span class="sxs-lookup"><span data-stu-id="6a5be-137">-Zone</span></span>
<span data-ttu-id="6a5be-138">Specifica la zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="6a5be-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="6a5be-139">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6a5be-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a5be-140">-Confirm</span></span>
<span data-ttu-id="6a5be-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a5be-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5be-142">-WhatIf</span></span>
<span data-ttu-id="6a5be-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a5be-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a5be-144">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a5be-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a5be-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a5be-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5be-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5be-146">CommonParameters</span></span>
<span data-ttu-id="6a5be-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5be-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5be-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a5be-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5be-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a5be-149">INPUTS</span></span>

### <span data-ttu-id="6a5be-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6a5be-151">Puoi reindirizzare un oggetto DnsZone a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a5be-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="6a5be-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a5be-152">OUTPUTS</span></span>

### <span data-ttu-id="6a5be-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6a5be-154">Questo cmdlet restituisce un oggetto DnsZone che rappresenta la zona DNS aggiornata con un nuovo ETag.</span><span class="sxs-lookup"><span data-stu-id="6a5be-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="6a5be-155">Note</span><span class="sxs-lookup"><span data-stu-id="6a5be-155">NOTES</span></span>
<span data-ttu-id="6a5be-156">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="6a5be-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6a5be-157">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="6a5be-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6a5be-158">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6a5be-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6a5be-159">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6a5be-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6a5be-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a5be-160">RELATED LINKS</span></span>

[<span data-ttu-id="6a5be-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="6a5be-162">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="6a5be-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="6a5be-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)