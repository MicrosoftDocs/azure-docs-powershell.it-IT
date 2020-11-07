---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
ms.openlocfilehash: b86ad0382fa7f87ac8aabb6b026b84d5a879f8ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866690"
---
# <span data-ttu-id="62219-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="62219-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62219-102">SYNOPSIS</span></span>
<span data-ttu-id="62219-103">Elimina un set di record.</span><span class="sxs-lookup"><span data-stu-id="62219-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62219-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62219-104">SYNTAX</span></span>

### <span data-ttu-id="62219-105">Campi</span><span class="sxs-lookup"><span data-stu-id="62219-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62219-106">Misto</span><span class="sxs-lookup"><span data-stu-id="62219-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62219-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="62219-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62219-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62219-108">DESCRIPTION</span></span>
<span data-ttu-id="62219-109">Il cmdlet **Remove-AzureRmDnsRecordSet** Elimina il set di record specificato dalla zona specificata.</span><span class="sxs-lookup"><span data-stu-id="62219-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="62219-110">Non è possibile eliminare i record SOA o Name Server (NS) creati automaticamente nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="62219-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="62219-111">Puoi passare un oggetto **Recordset** a questo cmdlet usando l'operatore pipeline o come parametro.</span><span class="sxs-lookup"><span data-stu-id="62219-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="62219-112">Per identificare un record impostato per nome e tipo senza usare un oggetto **Recordset** , devi passare la zona come oggetto **dnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62219-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="62219-113">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="62219-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="62219-114">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="62219-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="62219-115">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="62219-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="62219-116">Puoi eliminarlo usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="62219-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="62219-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62219-117">EXAMPLES</span></span>

### <span data-ttu-id="62219-118">Esempio 1: rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="62219-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="62219-119">Il primo comando ottiene il set di record specificato e lo archivia nella variabile $RecordSet. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="62219-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="62219-120">Esempio 2: rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="62219-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="62219-121">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="62219-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="62219-122">Il secondo comando Elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="62219-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="62219-123">Le richieste di conferma vengono soppresse.</span><span class="sxs-lookup"><span data-stu-id="62219-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="62219-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62219-124">PARAMETERS</span></span>

### <span data-ttu-id="62219-125">-Force</span><span class="sxs-lookup"><span data-stu-id="62219-125">-Force</span></span>
<span data-ttu-id="62219-126">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62219-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="62219-127">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="62219-127">It will be removed in a future release.</span></span>

<span data-ttu-id="62219-128">Per verificare se questo cmdlet richiede la conferma, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="62219-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62219-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="62219-129">-Name</span></span>
<span data-ttu-id="62219-130">Specifica il nome del **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="62219-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="62219-131">Quando specifichi il record impostato per nome, la zona DNS deve essere specificata usando il parametro *zone* o i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62219-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="62219-132">In alternativa, il set di record può essere specificato usando un oggetto **Recordset** , passato usando il parametro *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="62219-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62219-133">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="62219-133">-Overwrite</span></span>
<span data-ttu-id="62219-134">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="62219-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="62219-135">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="62219-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="62219-136">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="62219-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="62219-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62219-137">-PassThru</span></span>
<span data-ttu-id="62219-138">PassThru</span><span class="sxs-lookup"><span data-stu-id="62219-138">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62219-139">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-139">-RecordSet</span></span>
<span data-ttu-id="62219-140">Specifica l'oggetto **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="62219-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="62219-141">In alternativa, il set di record può essere specificato usando i parametri *Name* e *zone* oppure usando i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62219-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62219-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="62219-142">-RecordType</span></span>
<span data-ttu-id="62219-143">Specifica il tipo di record DNS.</span><span class="sxs-lookup"><span data-stu-id="62219-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="62219-144">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="62219-144">Valid values are:</span></span>

- <span data-ttu-id="62219-145">Un</span><span class="sxs-lookup"><span data-stu-id="62219-145">A</span></span>
- <span data-ttu-id="62219-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="62219-146">AAAA</span></span>
- <span data-ttu-id="62219-147">CNAME</span><span class="sxs-lookup"><span data-stu-id="62219-147">CNAME</span></span>
- <span data-ttu-id="62219-148">MX</span><span class="sxs-lookup"><span data-stu-id="62219-148">MX</span></span>
- <span data-ttu-id="62219-149">NS</span><span class="sxs-lookup"><span data-stu-id="62219-149">NS</span></span>
- <span data-ttu-id="62219-150">PTR</span><span class="sxs-lookup"><span data-stu-id="62219-150">PTR</span></span>
- <span data-ttu-id="62219-151">SRV</span><span class="sxs-lookup"><span data-stu-id="62219-151">SRV</span></span>
- <span data-ttu-id="62219-152">TXT</span><span class="sxs-lookup"><span data-stu-id="62219-152">TXT</span></span>

<span data-ttu-id="62219-153">I record SOA vengono eliminati automaticamente quando la zona viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="62219-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="62219-154">Non è possibile eliminare manualmente i record SOA.</span><span class="sxs-lookup"><span data-stu-id="62219-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62219-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62219-155">-ResourceGroupName</span></span>
<span data-ttu-id="62219-156">Specifica il gruppo di risorse che contiene la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="62219-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62219-157">Questo parametro è applicabile solo quando il set di record e la zona DNS vengono specificati usando i parametri *Name* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="62219-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="62219-158">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="62219-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="62219-159">-Zona</span><span class="sxs-lookup"><span data-stu-id="62219-159">-Zone</span></span>
<span data-ttu-id="62219-160">Specifica la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="62219-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62219-161">Questo parametro è applicabile solo quando specifichi il set di record usando il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="62219-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="62219-162">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62219-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62219-163">-Zonename</span><span class="sxs-lookup"><span data-stu-id="62219-163">-ZoneName</span></span>
<span data-ttu-id="62219-164">Specifica il nome della zona che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="62219-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="62219-165">Devi anche specificare i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="62219-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="62219-166">In alternativa, il set di record può essere specificato usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="62219-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="62219-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62219-167">-Confirm</span></span>
<span data-ttu-id="62219-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62219-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62219-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62219-169">-WhatIf</span></span>
<span data-ttu-id="62219-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62219-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62219-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62219-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62219-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62219-172">CommonParameters</span></span>
<span data-ttu-id="62219-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62219-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62219-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62219-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62219-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62219-175">INPUTS</span></span>

### <span data-ttu-id="62219-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="62219-177">È possibile reindirizzare un oggetto **Recordset** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62219-177">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="62219-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62219-178">OUTPUTS</span></span>

### <span data-ttu-id="62219-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62219-179">None</span></span>
<span data-ttu-id="62219-180">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="62219-180">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="62219-181">Note</span><span class="sxs-lookup"><span data-stu-id="62219-181">NOTES</span></span>
<span data-ttu-id="62219-182">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="62219-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="62219-183">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="62219-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="62219-184">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="62219-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="62219-185">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="62219-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="62219-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62219-186">RELATED LINKS</span></span>

[<span data-ttu-id="62219-187">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-187">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="62219-188">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-188">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="62219-189">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="62219-189">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
