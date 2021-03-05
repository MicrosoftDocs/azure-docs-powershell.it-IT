---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984772"
---
# <span data-ttu-id="007e2-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="007e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="007e2-102">SYNOPSIS</span></span>
<span data-ttu-id="007e2-103">Elimina un set di record.</span><span class="sxs-lookup"><span data-stu-id="007e2-103">Deletes a record set.</span></span>

## <span data-ttu-id="007e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="007e2-104">SYNTAX</span></span>

### <span data-ttu-id="007e2-105">Campi</span><span class="sxs-lookup"><span data-stu-id="007e2-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007e2-106">Misto</span><span class="sxs-lookup"><span data-stu-id="007e2-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="007e2-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="007e2-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007e2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="007e2-108">DESCRIPTION</span></span>
<span data-ttu-id="007e2-109">Il cmdlet **Remove-AzDnsRecordSet** elimina il set di record specificato dall'area specificata.</span><span class="sxs-lookup"><span data-stu-id="007e2-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="007e2-110">Non è possibile eliminare record SOA o server dei nomi (NS) creati automaticamente nell'apice di zona.</span><span class="sxs-lookup"><span data-stu-id="007e2-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="007e2-111">È possibile passare un **oggetto RecordSet** a questo cmdlet usando l'operatore della pipeline o come parametro.</span><span class="sxs-lookup"><span data-stu-id="007e2-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="007e2-112">Per identificare un record in base al nome e al tipo senza usare un oggetto **RecordSet,** è necessario passare l'area come oggetto **DnsZone** a questo cmdlet usando l'operatore della pipeline o come parametro oppure in alternativa è possibile specificare i parametri *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="007e2-113">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="007e2-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="007e2-114">Quando si specifica il set di record con un oggetto **RecordSet,** il set di record non viene eliminato se è stato modificato nel DNS di Azure dopo il recupero dell'oggetto **RecordSet** locale.</span><span class="sxs-lookup"><span data-stu-id="007e2-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="007e2-115">Ciò fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="007e2-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="007e2-116">È possibile eliminare questa operazione usando il parametro *Overwrite,* che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="007e2-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="007e2-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="007e2-117">EXAMPLES</span></span>

### <span data-ttu-id="007e2-118">Esempio 1: Rimuovere un set di record</span><span class="sxs-lookup"><span data-stu-id="007e2-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="007e2-119">Il primo comando ottiene il set di record specificato e quindi lo archivia nella $RecordSet variabile. Il secondo comando rimuove il set di record in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="007e2-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="007e2-120">Esempio 2: Rimuovere un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="007e2-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="007e2-121">Il primo comando ottiene il set di record specificato.</span><span class="sxs-lookup"><span data-stu-id="007e2-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="007e2-122">Il secondo comando elimina il set di record, anche se è stato modificato nel frattempo.</span><span class="sxs-lookup"><span data-stu-id="007e2-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="007e2-123">Le richieste di conferma vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="007e2-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="007e2-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="007e2-124">PARAMETERS</span></span>

### <span data-ttu-id="007e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007e2-125">-DefaultProfile</span></span>
<span data-ttu-id="007e2-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="007e2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="007e2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="007e2-127">-Name</span></span>
<span data-ttu-id="007e2-128">Specifica il nome del **recordSet** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="007e2-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="007e2-129">Quando si specifica il set di record in base al nome, è necessario specificare l'area DNS usando il parametro *Zone* o *i parametri ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="007e2-130">In alternativa, è possibile specificare il set di record usando un **oggetto RecordSet,** passato con il *parametro RecordSet.*</span><span class="sxs-lookup"><span data-stu-id="007e2-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="007e2-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="007e2-131">-Overwrite</span></span>
<span data-ttu-id="007e2-132">Quando si specifica il set di record con un oggetto **RecordSet,** il set di record non viene eliminato se è stato modificato nel DNS di Azure dopo il recupero dell'oggetto **RecordSet** locale.</span><span class="sxs-lookup"><span data-stu-id="007e2-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="007e2-133">Ciò fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="007e2-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="007e2-134">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="007e2-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="007e2-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="007e2-135">-PassThru</span></span>
<span data-ttu-id="007e2-136">passthru</span><span class="sxs-lookup"><span data-stu-id="007e2-136">passthru</span></span>

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

### <span data-ttu-id="007e2-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-137">-RecordSet</span></span>
<span data-ttu-id="007e2-138">Specifica **l'oggetto RecordSet** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="007e2-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="007e2-139">In alternativa, è possibile specificare il set di record usando i parametri *Name* e *Zone* oppure i parametri *Name,* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="007e2-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="007e2-140">-RecordType</span></span>
<span data-ttu-id="007e2-141">Specifica il tipo di record DNS.</span><span class="sxs-lookup"><span data-stu-id="007e2-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="007e2-142">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="007e2-142">Valid values are:</span></span>
- <span data-ttu-id="007e2-143">A</span><span class="sxs-lookup"><span data-stu-id="007e2-143">A</span></span>
- <span data-ttu-id="007e2-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="007e2-144">AAAA</span></span>
- <span data-ttu-id="007e2-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="007e2-145">CNAME</span></span>
- <span data-ttu-id="007e2-146">MX</span><span class="sxs-lookup"><span data-stu-id="007e2-146">MX</span></span>
- <span data-ttu-id="007e2-147">NS</span><span class="sxs-lookup"><span data-stu-id="007e2-147">NS</span></span>
- <span data-ttu-id="007e2-148">PTR</span><span class="sxs-lookup"><span data-stu-id="007e2-148">PTR</span></span>
- <span data-ttu-id="007e2-149">SRV</span><span class="sxs-lookup"><span data-stu-id="007e2-149">SRV</span></span>
- <span data-ttu-id="007e2-150">I record TXT SOA vengono eliminati automaticamente quando l'area viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="007e2-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="007e2-151">Non è possibile eliminare manualmente i record SOA.</span><span class="sxs-lookup"><span data-stu-id="007e2-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="007e2-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007e2-152">-ResourceGroupName</span></span>
<span data-ttu-id="007e2-153">Specifica il gruppo di risorse che contiene l'area DNS che contiene il **RecordSet** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="007e2-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="007e2-154">Questo parametro è valido solo quando il set di record e l'area DNS vengono specificati usando i *parametri Name* e *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="007e2-155">In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i *parametri Name* e *Zone.*</span><span class="sxs-lookup"><span data-stu-id="007e2-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="007e2-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="007e2-156">-Zone</span></span>
<span data-ttu-id="007e2-157">Specifica l'area DNS che contiene il **RecordSet** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="007e2-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="007e2-158">Questo parametro è applicabile solo quando si specifica il set di record usando il *parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="007e2-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="007e2-159">In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i parametri *Name,* *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="007e2-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="007e2-160">-ZoneName</span></span>
<span data-ttu-id="007e2-161">Specifica il nome dell'area che contiene il **recordSet** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="007e2-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="007e2-162">È anche necessario specificare i *parametri Name* *e ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="007e2-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="007e2-163">In alternativa, è possibile specificare il set di record usando il parametro *RecordSet* o i *parametri Name* e *Zone.*</span><span class="sxs-lookup"><span data-stu-id="007e2-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="007e2-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="007e2-164">-Confirm</span></span>
<span data-ttu-id="007e2-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="007e2-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007e2-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007e2-166">-WhatIf</span></span>
<span data-ttu-id="007e2-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="007e2-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="007e2-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="007e2-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007e2-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007e2-169">CommonParameters</span></span>
<span data-ttu-id="007e2-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007e2-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007e2-171">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007e2-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007e2-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="007e2-172">INPUTS</span></span>

### <span data-ttu-id="007e2-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="007e2-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="007e2-174">System.String</span><span class="sxs-lookup"><span data-stu-id="007e2-174">System.String</span></span>

### <span data-ttu-id="007e2-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="007e2-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="007e2-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="007e2-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="007e2-177">OUTPUTS</span></span>

### <span data-ttu-id="007e2-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="007e2-178">System.Boolean</span></span>

## <span data-ttu-id="007e2-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="007e2-179">NOTES</span></span>
<span data-ttu-id="007e2-180">È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="007e2-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="007e2-181">Per impostazione predefinita, il cmdlet chiede conferma se la $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="007e2-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="007e2-182">Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="007e2-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="007e2-183">Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="007e2-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="007e2-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="007e2-184">RELATED LINKS</span></span>

[<span data-ttu-id="007e2-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="007e2-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="007e2-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="007e2-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
