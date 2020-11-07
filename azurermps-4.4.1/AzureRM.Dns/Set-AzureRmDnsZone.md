---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687524"
---
# <span data-ttu-id="2d3ba-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="2d3ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3ba-103">Aggiorna le proprietà di una zona DNS.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d3ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d3ba-104">SYNTAX</span></span>

### <span data-ttu-id="2d3ba-105">Campi</span><span class="sxs-lookup"><span data-stu-id="2d3ba-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d3ba-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2d3ba-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d3ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d3ba-107">DESCRIPTION</span></span>
<span data-ttu-id="2d3ba-108">Il cmdlet **set-AzureRmDnsZone** aggiorna la zona DNS specificata nel servizio Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="2d3ba-109">Questo cmdlet non aggiorna i set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="2d3ba-110">Puoi passare un oggetto **dnsZone** come parametro o usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2d3ba-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="2d3ba-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="2d3ba-112">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2d3ba-113">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2d3ba-114">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2d3ba-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d3ba-115">EXAMPLES</span></span>

### <span data-ttu-id="2d3ba-116">Esempio 1: aggiornare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="2d3ba-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="2d3ba-117">Il primo comando consente di ottenere la zona denominata myzone.com dal gruppo di risorse specificato e quindi di archiviarla nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="2d3ba-118">Il secondo comando Aggiorna i tag per $Zone.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="2d3ba-119">Il comando finale conferma la modifica.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-119">The final command commits the change.</span></span>

### <span data-ttu-id="2d3ba-120">Esempio 2: aggiornare i tag per una zona</span><span class="sxs-lookup"><span data-stu-id="2d3ba-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="2d3ba-121">Questo comando Aggiorna i tag per la zona denominata myzone.com senza prima ottenere esplicitamente la zona.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="2d3ba-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d3ba-122">PARAMETERS</span></span>

### <span data-ttu-id="2d3ba-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d3ba-123">-Name</span></span>
<span data-ttu-id="2d3ba-124">Specifica il nome della zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3ba-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="2d3ba-125">-Overwrite</span></span>
<span data-ttu-id="2d3ba-126">Quando si passa una zona DNS come oggetto (usando l'oggetto zone o tramite la pipeline), non viene aggiornata se è stata modificata in Azure DNS dopo che è stato recuperato l'oggetto DnsZone locale.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="2d3ba-127">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2d3ba-128">Puoi eliminare questo comportamento con il parametro *overwrite* , che aggiorna la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="2d3ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d3ba-130">Specifica il nome del gruppo di risorse che contiene la zona da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="2d3ba-131">Devi anche specificare il parametro zonename.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="2d3ba-132">In alternativa, puoi specificare la zona usando un oggetto DnsZone con il parametro *zone* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3ba-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d3ba-133">-Tag</span></span>
<span data-ttu-id="2d3ba-134">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d3ba-135">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="2d3ba-135">For example:</span></span>

<span data-ttu-id="2d3ba-136">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2d3ba-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d3ba-137">-Zona</span><span class="sxs-lookup"><span data-stu-id="2d3ba-137">-Zone</span></span>
<span data-ttu-id="2d3ba-138">Specifica la zona DNS da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="2d3ba-139">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2d3ba-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="2d3ba-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d3ba-140">-Confirm</span></span>
<span data-ttu-id="2d3ba-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3ba-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3ba-142">-WhatIf</span></span>
<span data-ttu-id="2d3ba-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d3ba-144">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d3ba-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3ba-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3ba-146">-DefaultProfile</span></span>
<span data-ttu-id="2d3ba-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d3ba-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3ba-148">CommonParameters</span></span>
<span data-ttu-id="2d3ba-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3ba-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d3ba-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3ba-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d3ba-151">INPUTS</span></span>

### <span data-ttu-id="2d3ba-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2d3ba-153">Puoi reindirizzare un oggetto DnsZone a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-153">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="2d3ba-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d3ba-154">OUTPUTS</span></span>

### <span data-ttu-id="2d3ba-155">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-155">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2d3ba-156">Questo cmdlet restituisce un oggetto DnsZone che rappresenta la zona DNS aggiornata con un nuovo ETag.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-156">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="2d3ba-157">Note</span><span class="sxs-lookup"><span data-stu-id="2d3ba-157">NOTES</span></span>
<span data-ttu-id="2d3ba-158">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-158">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="2d3ba-159">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-159">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="2d3ba-160">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-160">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2d3ba-161">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2d3ba-161">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2d3ba-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d3ba-162">RELATED LINKS</span></span>

[<span data-ttu-id="2d3ba-163">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-163">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2d3ba-164">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-164">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="2d3ba-165">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2d3ba-165">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
