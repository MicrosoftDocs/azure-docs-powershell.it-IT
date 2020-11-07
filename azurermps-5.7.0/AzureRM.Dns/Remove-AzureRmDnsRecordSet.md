---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: fce5cbe993861d2a0d97bffd4bf4c7dbe19cc535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686200"
---
# <span data-ttu-id="72da2-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="72da2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72da2-102">SYNOPSIS</span></span>
<span data-ttu-id="72da2-103">Elimina un set di record.</span><span class="sxs-lookup"><span data-stu-id="72da2-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72da2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72da2-104">SYNTAX</span></span>

### <span data-ttu-id="72da2-105">Campi</span><span class="sxs-lookup"><span data-stu-id="72da2-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72da2-106">Misto</span><span class="sxs-lookup"><span data-stu-id="72da2-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72da2-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="72da2-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72da2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72da2-108">DESCRIPTION</span></span>
<span data-ttu-id="72da2-109">Il cmdlet **Remove-AzureRmDnsRecordSet** Elimina il set di record specificato dalla zona specificata.</span><span class="sxs-lookup"><span data-stu-id="72da2-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="72da2-110">Non è possibile eliminare i record SOA o Name Server (NS) creati automaticamente nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="72da2-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="72da2-111">Puoi passare un oggetto **Recordset** a questo cmdlet usando l'operatore pipeline o come parametro.</span><span class="sxs-lookup"><span data-stu-id="72da2-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="72da2-112">Per identificare un record impostato per nome e tipo senza usare un oggetto **Recordset** , devi passare la zona come oggetto **dnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="72da2-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="72da2-113">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="72da2-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="72da2-114">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="72da2-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="72da2-115">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72da2-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="72da2-116">Puoi eliminarlo usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72da2-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="72da2-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72da2-117">EXAMPLES</span></span>

### <span data-ttu-id="72da2-118">Esempio 1: rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="72da2-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="72da2-119">Il primo comando ottiene il set di record specificato e lo archivia nella variabile $RecordSet. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="72da2-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="72da2-120">Esempio 2: rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="72da2-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="72da2-121">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="72da2-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="72da2-122">Il secondo comando Elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="72da2-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="72da2-123">Le richieste di conferma vengono soppresse.</span><span class="sxs-lookup"><span data-stu-id="72da2-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="72da2-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72da2-124">PARAMETERS</span></span>

### <span data-ttu-id="72da2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72da2-125">-DefaultProfile</span></span>
<span data-ttu-id="72da2-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72da2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72da2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="72da2-127">-Force</span></span>
<span data-ttu-id="72da2-128">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72da2-128">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="72da2-129">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="72da2-129">It will be removed in a future release.</span></span>

<span data-ttu-id="72da2-130">Per verificare se questo cmdlet richiede la conferma, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="72da2-130">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="72da2-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="72da2-131">-Name</span></span>
<span data-ttu-id="72da2-132">Specifica il nome del **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="72da2-132">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="72da2-133">Quando specifichi il record impostato per nome, la zona DNS deve essere specificata usando il parametro *zone* o i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="72da2-133">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="72da2-134">In alternativa, il set di record può essere specificato usando un oggetto **Recordset** , passato usando il parametro *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="72da2-134">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="72da2-135">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="72da2-135">-Overwrite</span></span>
<span data-ttu-id="72da2-136">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="72da2-136">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="72da2-137">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72da2-137">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="72da2-138">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="72da2-138">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="72da2-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72da2-139">-PassThru</span></span>
<span data-ttu-id="72da2-140">PassThru</span><span class="sxs-lookup"><span data-stu-id="72da2-140">passthru</span></span>

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

### <span data-ttu-id="72da2-141">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-141">-RecordSet</span></span>
<span data-ttu-id="72da2-142">Specifica l'oggetto **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="72da2-142">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="72da2-143">In alternativa, il set di record può essere specificato usando i parametri *Name* e *zone* oppure usando i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="72da2-143">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="72da2-144">-RecordType</span><span class="sxs-lookup"><span data-stu-id="72da2-144">-RecordType</span></span>
<span data-ttu-id="72da2-145">Specifica il tipo di record DNS.</span><span class="sxs-lookup"><span data-stu-id="72da2-145">Specifies the type of DNS record.</span></span>

<span data-ttu-id="72da2-146">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="72da2-146">Valid values are:</span></span>

- <span data-ttu-id="72da2-147">Un</span><span class="sxs-lookup"><span data-stu-id="72da2-147">A</span></span>
- <span data-ttu-id="72da2-148">AAAA</span><span class="sxs-lookup"><span data-stu-id="72da2-148">AAAA</span></span>
- <span data-ttu-id="72da2-149">CNAME</span><span class="sxs-lookup"><span data-stu-id="72da2-149">CNAME</span></span>
- <span data-ttu-id="72da2-150">MX</span><span class="sxs-lookup"><span data-stu-id="72da2-150">MX</span></span>
- <span data-ttu-id="72da2-151">NS</span><span class="sxs-lookup"><span data-stu-id="72da2-151">NS</span></span>
- <span data-ttu-id="72da2-152">PTR</span><span class="sxs-lookup"><span data-stu-id="72da2-152">PTR</span></span>
- <span data-ttu-id="72da2-153">SRV</span><span class="sxs-lookup"><span data-stu-id="72da2-153">SRV</span></span>
- <span data-ttu-id="72da2-154">TXT</span><span class="sxs-lookup"><span data-stu-id="72da2-154">TXT</span></span>

<span data-ttu-id="72da2-155">I record SOA vengono eliminati automaticamente quando la zona viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="72da2-155">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="72da2-156">Non è possibile eliminare manualmente i record SOA.</span><span class="sxs-lookup"><span data-stu-id="72da2-156">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72da2-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72da2-157">-ResourceGroupName</span></span>
<span data-ttu-id="72da2-158">Specifica il gruppo di risorse che contiene la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="72da2-158">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="72da2-159">Questo parametro è applicabile solo quando il set di record e la zona DNS vengono specificati usando i parametri *Name* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="72da2-159">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="72da2-160">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="72da2-160">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="72da2-161">-Zona</span><span class="sxs-lookup"><span data-stu-id="72da2-161">-Zone</span></span>
<span data-ttu-id="72da2-162">Specifica la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="72da2-162">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="72da2-163">Questo parametro è applicabile solo quando specifichi il set di record usando il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="72da2-163">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="72da2-164">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="72da2-164">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="72da2-165">-Zonename</span><span class="sxs-lookup"><span data-stu-id="72da2-165">-ZoneName</span></span>
<span data-ttu-id="72da2-166">Specifica il nome della zona che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="72da2-166">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="72da2-167">Devi anche specificare i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="72da2-167">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="72da2-168">In alternativa, il set di record può essere specificato usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="72da2-168">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="72da2-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72da2-169">-Confirm</span></span>
<span data-ttu-id="72da2-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72da2-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72da2-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72da2-171">-WhatIf</span></span>
<span data-ttu-id="72da2-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72da2-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72da2-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72da2-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72da2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72da2-174">CommonParameters</span></span>
<span data-ttu-id="72da2-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72da2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72da2-176">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72da2-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72da2-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72da2-177">INPUTS</span></span>

### <span data-ttu-id="72da2-178">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="72da2-179">È possibile reindirizzare un oggetto **Recordset** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72da2-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="72da2-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72da2-180">OUTPUTS</span></span>

### <span data-ttu-id="72da2-181">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72da2-181">None</span></span>
<span data-ttu-id="72da2-182">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="72da2-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="72da2-183">Note</span><span class="sxs-lookup"><span data-stu-id="72da2-183">NOTES</span></span>
<span data-ttu-id="72da2-184">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="72da2-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="72da2-185">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="72da2-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="72da2-186">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="72da2-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="72da2-187">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="72da2-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="72da2-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72da2-188">RELATED LINKS</span></span>

[<span data-ttu-id="72da2-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="72da2-190">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="72da2-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72da2-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
