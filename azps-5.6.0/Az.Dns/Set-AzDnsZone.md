---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984701"
---
# <span data-ttu-id="2ba74-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="2ba74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ba74-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba74-103">Aggiorna le proprietà di un'area DNS.</span><span class="sxs-lookup"><span data-stu-id="2ba74-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="2ba74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ba74-104">SYNTAX</span></span>

### <span data-ttu-id="2ba74-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ba74-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba74-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="2ba74-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba74-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2ba74-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ba74-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ba74-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba74-109">Il cmdlet **Set-AzDnsZone** aggiorna l'area DNS specificata nel servizio DNS di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba74-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="2ba74-110">Questo cmdlet non aggiorna i set di record nell'area.</span><span class="sxs-lookup"><span data-stu-id="2ba74-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="2ba74-111">È possibile passare un **oggetto DnsZone** come parametro o usando l'operatore pipeline oppure in alternativa è possibile specificare i parametri *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="2ba74-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="2ba74-112">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2ba74-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2ba74-113">Quando si passa un'area DNS come oggetto, usando l'oggetto Zone o tramite la pipeline, non viene aggiornata se è stata modificata in Azure DNS dopo il recupero dell'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="2ba74-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2ba74-114">Ciò fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2ba74-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2ba74-115">È possibile disattivare questo comportamento con il *parametro Overwrite,* che aggiorna l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2ba74-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2ba74-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ba74-116">EXAMPLES</span></span>

### <span data-ttu-id="2ba74-117">Esempio 1: Aggiornare un'area DNS</span><span class="sxs-lookup"><span data-stu-id="2ba74-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="2ba74-118">Il primo comando recupera l'area myzone.com denominata dal gruppo di risorse specificato e quindi la archivia nella $Zone variabile.</span><span class="sxs-lookup"><span data-stu-id="2ba74-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="2ba74-119">Il secondo comando aggiorna i tag per $Zone.</span><span class="sxs-lookup"><span data-stu-id="2ba74-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="2ba74-120">Il comando finale esegue il commit della modifica.</span><span class="sxs-lookup"><span data-stu-id="2ba74-120">The final command commits the change.</span></span>

### <span data-ttu-id="2ba74-121">Esempio 2: Aggiornare i tag per un'area</span><span class="sxs-lookup"><span data-stu-id="2ba74-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="2ba74-122">Questo comando aggiorna i tag per l'area myzone.com senza prima ottenere esplicitamente l'area.</span><span class="sxs-lookup"><span data-stu-id="2ba74-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="2ba74-123">Esempio 3: Associazione di un'area privata a una rete virtuale specificandone l'ID</span><span class="sxs-lookup"><span data-stu-id="2ba74-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="2ba74-124">Questo comando associa l'area DNS myprivatezone.com privata alla rete virtuale myvnet come rete di registrazione specificandone l'ID.</span><span class="sxs-lookup"><span data-stu-id="2ba74-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="2ba74-125">Esempio 4: Associazione di un'area privata a una rete virtuale specificando l'oggetto di rete.</span><span class="sxs-lookup"><span data-stu-id="2ba74-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="2ba74-126">Questo comando associa l'myprivatezone.com di zona DNS privata alla rete virtuale myvnet come rete di registrazione passando l'oggetto di rete virtuale rappresentato dalla variabile $vnet al cmdlet Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="2ba74-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="2ba74-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ba74-127">PARAMETERS</span></span>

### <span data-ttu-id="2ba74-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba74-128">-DefaultProfile</span></span>
<span data-ttu-id="2ba74-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ba74-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-130">-Name</span><span class="sxs-lookup"><span data-stu-id="2ba74-130">-Name</span></span>
<span data-ttu-id="2ba74-131">Specifica il nome dell'area DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2ba74-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="2ba74-132">-Overwrite</span></span>
<span data-ttu-id="2ba74-133">Quando si passa un'area DNS come oggetto, usando l'oggetto Zone o tramite la pipeline, non viene aggiornata se è stata modificata in Azure DNS dopo il recupero dell'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="2ba74-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2ba74-134">Ciò fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2ba74-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2ba74-135">È possibile disattivare questo comportamento con il *parametro Overwrite,* che aggiorna l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2ba74-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ba74-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="2ba74-137">Elenco di reti virtuali in cui verranno registrati i record dei nomi host delle macchine virtuali in questa area DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="2ba74-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2ba74-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2ba74-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="2ba74-139">L'elenco degli ID di rete virtuale che registreranno i record dei nomi host delle macchine virtuali in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="2ba74-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2ba74-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ba74-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="2ba74-141">Elenco di reti virtuali in grado di risolvere i record in questa area DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="2ba74-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2ba74-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2ba74-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="2ba74-143">L'elenco degli ID di rete virtuale in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="2ba74-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="2ba74-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba74-144">-ResourceGroupName</span></span>
<span data-ttu-id="2ba74-145">Specifica il nome del gruppo di risorse che contiene l'area da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2ba74-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="2ba74-146">È anche necessario specificare il parametro ZoneName.</span><span class="sxs-lookup"><span data-stu-id="2ba74-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="2ba74-147">In alternativa, è possibile specificare l'area usando un oggetto DnsZone con il parametro *Zone* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2ba74-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ba74-148">-Tag</span></span>
<span data-ttu-id="2ba74-149">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2ba74-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ba74-150">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2ba74-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="2ba74-151">-Zone</span></span>
<span data-ttu-id="2ba74-152">Specifica l'area DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2ba74-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="2ba74-153">In alternativa, è possibile specificare l'area usando *i parametri ZoneName* *e ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="2ba74-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba74-154">-Confirm</span></span>
<span data-ttu-id="2ba74-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ba74-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba74-156">-WhatIf</span></span>
<span data-ttu-id="2ba74-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba74-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ba74-158">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba74-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ba74-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ba74-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba74-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba74-160">CommonParameters</span></span>
<span data-ttu-id="2ba74-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba74-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba74-162">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba74-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba74-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ba74-163">INPUTS</span></span>

### <span data-ttu-id="2ba74-164">System.String</span><span class="sxs-lookup"><span data-stu-id="2ba74-164">System.String</span></span>

### <span data-ttu-id="2ba74-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ba74-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2ba74-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ba74-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ba74-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2ba74-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2ba74-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="2ba74-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ba74-169">OUTPUTS</span></span>

### <span data-ttu-id="2ba74-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="2ba74-171">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ba74-171">NOTES</span></span>
<span data-ttu-id="2ba74-172">È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2ba74-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2ba74-173">Per impostazione predefinita, il cmdlet chiede conferma se la $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="2ba74-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="2ba74-174">Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2ba74-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2ba74-175">Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2ba74-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2ba74-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ba74-176">RELATED LINKS</span></span>

[<span data-ttu-id="2ba74-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="2ba74-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="2ba74-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="2ba74-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
