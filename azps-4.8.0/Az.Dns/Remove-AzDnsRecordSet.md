---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191564"
---
# <span data-ttu-id="ecf97-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="ecf97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecf97-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf97-103">Elimina un set di record.</span><span class="sxs-lookup"><span data-stu-id="ecf97-103">Deletes a record set.</span></span>

## <span data-ttu-id="ecf97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecf97-104">SYNTAX</span></span>

### <span data-ttu-id="ecf97-105">Campi</span><span class="sxs-lookup"><span data-stu-id="ecf97-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf97-106">Misto</span><span class="sxs-lookup"><span data-stu-id="ecf97-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf97-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ecf97-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf97-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf97-109">Il cmdlet **Remove-AzDnsRecordSet** Elimina il set di record specificato dalla zona specificata.</span><span class="sxs-lookup"><span data-stu-id="ecf97-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="ecf97-110">Non è possibile eliminare i record SOA o Name Server (NS) creati automaticamente nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="ecf97-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="ecf97-111">Puoi passare un oggetto **Recordset** a questo cmdlet usando l'operatore pipeline o come parametro.</span><span class="sxs-lookup"><span data-stu-id="ecf97-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="ecf97-112">Per identificare un record impostato per nome e tipo senza usare un oggetto **Recordset** , devi passare la zona come oggetto **dnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ecf97-113">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ecf97-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ecf97-114">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="ecf97-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ecf97-115">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ecf97-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ecf97-116">Puoi eliminarlo usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ecf97-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ecf97-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecf97-117">EXAMPLES</span></span>

### <span data-ttu-id="ecf97-118">Esempio 1: rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="ecf97-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="ecf97-119">Il primo comando ottiene il set di record specificato e lo archivia nella variabile $RecordSet. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ecf97-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="ecf97-120">Esempio 2: rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="ecf97-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="ecf97-121">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="ecf97-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="ecf97-122">Il secondo comando Elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="ecf97-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="ecf97-123">Le richieste di conferma vengono soppresse.</span><span class="sxs-lookup"><span data-stu-id="ecf97-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="ecf97-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecf97-124">PARAMETERS</span></span>

### <span data-ttu-id="ecf97-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf97-125">-DefaultProfile</span></span>
<span data-ttu-id="ecf97-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ecf97-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecf97-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecf97-127">-Name</span></span>
<span data-ttu-id="ecf97-128">Specifica il nome del **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ecf97-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="ecf97-129">Quando specifichi il record impostato per nome, la zona DNS deve essere specificata usando il parametro *zone* o i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ecf97-130">In alternativa, il set di record può essere specificato usando un oggetto **Recordset** , passato usando il parametro *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf97-131">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="ecf97-131">-Overwrite</span></span>
<span data-ttu-id="ecf97-132">Quando specifichi il set di record usando un oggetto **Recordset** , il set di record non viene eliminato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="ecf97-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ecf97-133">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ecf97-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ecf97-134">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ecf97-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ecf97-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecf97-135">-PassThru</span></span>
<span data-ttu-id="ecf97-136">PassThru</span><span class="sxs-lookup"><span data-stu-id="ecf97-136">passthru</span></span>

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

### <span data-ttu-id="ecf97-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-137">-RecordSet</span></span>
<span data-ttu-id="ecf97-138">Specifica l'oggetto **Recordset** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ecf97-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="ecf97-139">In alternativa, il set di record può essere specificato usando i parametri *Name* e *zone* oppure usando i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf97-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ecf97-140">-RecordType</span></span>
<span data-ttu-id="ecf97-141">Specifica il tipo di record DNS.</span><span class="sxs-lookup"><span data-stu-id="ecf97-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="ecf97-142">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ecf97-142">Valid values are:</span></span>
- <span data-ttu-id="ecf97-143">Un</span><span class="sxs-lookup"><span data-stu-id="ecf97-143">A</span></span>
- <span data-ttu-id="ecf97-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="ecf97-144">AAAA</span></span>
- <span data-ttu-id="ecf97-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="ecf97-145">CNAME</span></span>
- <span data-ttu-id="ecf97-146">MX</span><span class="sxs-lookup"><span data-stu-id="ecf97-146">MX</span></span>
- <span data-ttu-id="ecf97-147">NS</span><span class="sxs-lookup"><span data-stu-id="ecf97-147">NS</span></span>
- <span data-ttu-id="ecf97-148">PTR</span><span class="sxs-lookup"><span data-stu-id="ecf97-148">PTR</span></span>
- <span data-ttu-id="ecf97-149">SRV</span><span class="sxs-lookup"><span data-stu-id="ecf97-149">SRV</span></span>
- <span data-ttu-id="ecf97-150">I record SOA TXT vengono eliminati automaticamente quando la zona viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="ecf97-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="ecf97-151">Non è possibile eliminare manualmente i record SOA.</span><span class="sxs-lookup"><span data-stu-id="ecf97-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf97-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf97-152">-ResourceGroupName</span></span>
<span data-ttu-id="ecf97-153">Specifica il gruppo di risorse che contiene la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ecf97-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="ecf97-154">Questo parametro è applicabile solo quando il set di record e la zona DNS vengono specificati usando i parametri *Name* e *zonename* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="ecf97-155">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="ecf97-156">-Zona</span><span class="sxs-lookup"><span data-stu-id="ecf97-156">-Zone</span></span>
<span data-ttu-id="ecf97-157">Specifica la zona DNS che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ecf97-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="ecf97-158">Questo parametro è applicabile solo quando specifichi il set di record usando il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="ecf97-159">In alternativa, puoi specificare il set di record usando il parametro *Recordset* oppure i parametri *Name* , *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf97-160">-Zonename</span><span class="sxs-lookup"><span data-stu-id="ecf97-160">-ZoneName</span></span>
<span data-ttu-id="ecf97-161">Specifica il nome della zona che contiene il **Recordset** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="ecf97-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="ecf97-162">Devi anche specificare i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ecf97-163">In alternativa, il set di record può essere specificato usando il parametro *Recordset* oppure i parametri *Name* e *zone* .</span><span class="sxs-lookup"><span data-stu-id="ecf97-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="ecf97-164">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecf97-164">-Confirm</span></span>
<span data-ttu-id="ecf97-165">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf97-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf97-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf97-166">-WhatIf</span></span>
<span data-ttu-id="ecf97-167">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf97-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf97-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf97-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf97-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf97-169">CommonParameters</span></span>
<span data-ttu-id="ecf97-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf97-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf97-171">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf97-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf97-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecf97-172">INPUTS</span></span>

### <span data-ttu-id="ecf97-173">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="ecf97-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="ecf97-174">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf97-174">System.String</span></span>

### <span data-ttu-id="ecf97-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="ecf97-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="ecf97-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ecf97-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecf97-177">OUTPUTS</span></span>

### <span data-ttu-id="ecf97-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecf97-178">System.Boolean</span></span>

## <span data-ttu-id="ecf97-179">Note</span><span class="sxs-lookup"><span data-stu-id="ecf97-179">NOTES</span></span>
<span data-ttu-id="ecf97-180">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="ecf97-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ecf97-181">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="ecf97-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ecf97-182">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ecf97-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ecf97-183">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ecf97-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ecf97-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecf97-184">RELATED LINKS</span></span>

[<span data-ttu-id="ecf97-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="ecf97-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="ecf97-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecf97-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)