---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509867"
---
# <span data-ttu-id="85bd3-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="85bd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="85bd3-103">Aggiorna le proprietà di una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="85bd3-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85bd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85bd3-104">SYNTAX</span></span>

### <span data-ttu-id="85bd3-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85bd3-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bd3-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="85bd3-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bd3-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="85bd3-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85bd3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85bd3-108">DESCRIPTION</span></span>
<span data-ttu-id="85bd3-109">Il cmdlet **set-AzureRmDnsZone** aggiorna la zona DNS specificata nel servizio Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="85bd3-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="85bd3-110">Questo cmdlet non aggiorna i set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="85bd3-110">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="85bd3-111">Puoi passare un oggetto **dnsZone** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="85bd3-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="85bd3-112">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="85bd3-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="85bd3-113">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="85bd3-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="85bd3-114">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="85bd3-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="85bd3-115">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="85bd3-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="85bd3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85bd3-116">EXAMPLES</span></span>

### <span data-ttu-id="85bd3-117">Esempio 1: aggiornare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="85bd3-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="85bd3-118">Il primo comando consente di ottenere la zona denominata myzone.com dal gruppo di risorse specificato e quindi di archiviarla nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="85bd3-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="85bd3-119">Il secondo comando Aggiorna i tag per $Zone.</span><span class="sxs-lookup"><span data-stu-id="85bd3-119">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="85bd3-120">Il comando finale conferma la modifica.</span><span class="sxs-lookup"><span data-stu-id="85bd3-120">The final command commits the change.</span></span>

### <span data-ttu-id="85bd3-121">Esempio 2: aggiornare i tag per una zona</span><span class="sxs-lookup"><span data-stu-id="85bd3-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="85bd3-122">Questo comando Aggiorna i tag per la zona denominata myzone.com senza prima ottenere esplicitamente la zona.</span><span class="sxs-lookup"><span data-stu-id="85bd3-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="85bd3-123">Esempio 3: associazione di un'area privata a una rete virtuale specificando il relativo ID</span><span class="sxs-lookup"><span data-stu-id="85bd3-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="85bd3-124">Questo comando associa la zona DNS privata myprivatezone.com con la rete virtuale myvnet come rete di registrazione specificando il proprio ID.</span><span class="sxs-lookup"><span data-stu-id="85bd3-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="85bd3-125">Esempio 4: associazione di un'area privata a una rete virtuale specificando l'oggetto Network.</span><span class="sxs-lookup"><span data-stu-id="85bd3-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="85bd3-126">Questo comando associa la zona DNS privata myprivatezone.com con la rete virtuale myvnet come rete di registrazione passando l'oggetto di rete virtuale rappresentato da $vnet variabile al cmdlet Set-AzureRmDnsZone.</span><span class="sxs-lookup"><span data-stu-id="85bd3-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="85bd3-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85bd3-127">PARAMETERS</span></span>

### <span data-ttu-id="85bd3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bd3-128">-DefaultProfile</span></span>
<span data-ttu-id="85bd3-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85bd3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="85bd3-130">-Name</span></span>
<span data-ttu-id="85bd3-131">Specifica il nome della zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="85bd3-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-132">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="85bd3-132">-Overwrite</span></span>
<span data-ttu-id="85bd3-133">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="85bd3-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="85bd3-134">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="85bd3-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="85bd3-135">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="85bd3-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="85bd3-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85bd3-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="85bd3-137">L'elenco delle reti virtuali che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="85bd3-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="85bd3-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="85bd3-139">Elenco di ID di rete virtuale che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="85bd3-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85bd3-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="85bd3-141">L'elenco delle reti virtuali in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="85bd3-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="85bd3-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="85bd3-143">Elenco di ID di rete virtuale in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="85bd3-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85bd3-144">-ResourceGroupName</span></span>
<span data-ttu-id="85bd3-145">Specifica il nome del gruppo di risorse che contiene la zona da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="85bd3-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="85bd3-146">Devi anche specificare il parametro zonename.</span><span class="sxs-lookup"><span data-stu-id="85bd3-146">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="85bd3-147">In alternativa, puoi specificare la zona usando un oggetto DnsZone con il parametro *zone* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="85bd3-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="85bd3-148">-Tag</span></span>
<span data-ttu-id="85bd3-149">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="85bd3-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85bd3-150">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="85bd3-150">For example:</span></span>

<span data-ttu-id="85bd3-151">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="85bd3-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85bd3-152">-Zona</span><span class="sxs-lookup"><span data-stu-id="85bd3-152">-Zone</span></span>
<span data-ttu-id="85bd3-153">Specifica la zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="85bd3-153">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="85bd3-154">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="85bd3-154">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="85bd3-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85bd3-155">-Confirm</span></span>
<span data-ttu-id="85bd3-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85bd3-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85bd3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85bd3-157">-WhatIf</span></span>
<span data-ttu-id="85bd3-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85bd3-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85bd3-159">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85bd3-159">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85bd3-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85bd3-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85bd3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bd3-161">CommonParameters</span></span>
<span data-ttu-id="85bd3-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85bd3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bd3-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85bd3-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bd3-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85bd3-164">INPUTS</span></span>

### <span data-ttu-id="85bd3-165">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-165">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="85bd3-166">Puoi reindirizzare un oggetto DnsZone a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85bd3-166">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="85bd3-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85bd3-167">OUTPUTS</span></span>

### <span data-ttu-id="85bd3-168">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="85bd3-169">Questo cmdlet restituisce un oggetto DnsZone che rappresenta la zona DNS aggiornata con un nuovo ETag.</span><span class="sxs-lookup"><span data-stu-id="85bd3-169">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="85bd3-170">Note</span><span class="sxs-lookup"><span data-stu-id="85bd3-170">NOTES</span></span>
<span data-ttu-id="85bd3-171">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="85bd3-171">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="85bd3-172">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="85bd3-172">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="85bd3-173">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="85bd3-173">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="85bd3-174">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="85bd3-174">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="85bd3-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85bd3-175">RELATED LINKS</span></span>

[<span data-ttu-id="85bd3-176">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-176">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="85bd3-177">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-177">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="85bd3-178">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="85bd3-178">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
