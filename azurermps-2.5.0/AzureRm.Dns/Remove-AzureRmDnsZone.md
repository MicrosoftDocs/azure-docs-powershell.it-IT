---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867116"
---
# <span data-ttu-id="57a0a-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57a0a-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="57a0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="57a0a-103">Rimuove una zona DNS da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57a0a-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57a0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57a0a-104">SYNTAX</span></span>

### <span data-ttu-id="57a0a-105">Campi</span><span class="sxs-lookup"><span data-stu-id="57a0a-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57a0a-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="57a0a-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57a0a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57a0a-107">DESCRIPTION</span></span>
<span data-ttu-id="57a0a-108">Il cmdlet **Remove-AzureRmDnsZone** Elimina definitivamente una zona DNS (Domain Name System) da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="57a0a-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="57a0a-109">Vengono eliminati anche tutti i set di record contenuti nella zona.</span><span class="sxs-lookup"><span data-stu-id="57a0a-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="57a0a-110">Puoi passare un oggetto **dnsZone** usando il parametro *Name* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="57a0a-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="57a0a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="57a0a-112">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="57a0a-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="57a0a-113">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="57a0a-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="57a0a-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="57a0a-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="57a0a-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57a0a-115">EXAMPLES</span></span>

### <span data-ttu-id="57a0a-116">Esempio 1: rimuovere un'area</span><span class="sxs-lookup"><span data-stu-id="57a0a-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="57a0a-117">Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="57a0a-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="57a0a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57a0a-118">PARAMETERS</span></span>

### <span data-ttu-id="57a0a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="57a0a-119">-Force</span></span>
<span data-ttu-id="57a0a-120">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a0a-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="57a0a-121">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="57a0a-121">It will be removed in a future release.</span></span>

<span data-ttu-id="57a0a-122">Per verificare se questo cmdlet richiede la conferma, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="57a0a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="57a0a-123">-Name</span></span>
<span data-ttu-id="57a0a-124">Specifica il nome dell'area DNS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a0a-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="57a0a-125">Devi anche specificare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="57a0a-126">In alternativa, puoi specificare la zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="57a0a-127">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="57a0a-127">-Overwrite</span></span>
<span data-ttu-id="57a0a-128">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="57a0a-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="57a0a-129">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="57a0a-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="57a0a-130">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="57a0a-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="57a0a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57a0a-131">-PassThru</span></span>
<span data-ttu-id="57a0a-132">PassThru</span><span class="sxs-lookup"><span data-stu-id="57a0a-132">passthru</span></span>

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

### <span data-ttu-id="57a0a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a0a-133">-ResourceGroupName</span></span>
<span data-ttu-id="57a0a-134">Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="57a0a-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="57a0a-135">Devi anche specificare il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="57a0a-136">In alternativa, puoi specificare la zona DNS usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="57a0a-137">-Zona</span><span class="sxs-lookup"><span data-stu-id="57a0a-137">-Zone</span></span>
<span data-ttu-id="57a0a-138">Specifica la zona DNS da eliminare.</span><span class="sxs-lookup"><span data-stu-id="57a0a-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="57a0a-139">L'oggetto **dnsZone** passato può essere passato anche tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="57a0a-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="57a0a-140">In alternativa, puoi specificare la zona DNS da eliminare usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="57a0a-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="57a0a-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57a0a-141">-Confirm</span></span>
<span data-ttu-id="57a0a-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a0a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57a0a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a0a-143">-WhatIf</span></span>
<span data-ttu-id="57a0a-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57a0a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a0a-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57a0a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57a0a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a0a-146">CommonParameters</span></span>
<span data-ttu-id="57a0a-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a0a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a0a-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a0a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a0a-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57a0a-149">INPUTS</span></span>

### <span data-ttu-id="57a0a-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="57a0a-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="57a0a-151">Puoi reindirizzare un oggetto **dnsZone** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57a0a-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="57a0a-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57a0a-152">OUTPUTS</span></span>

### <span data-ttu-id="57a0a-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="57a0a-153">None</span></span>
<span data-ttu-id="57a0a-154">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="57a0a-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="57a0a-155">Note</span><span class="sxs-lookup"><span data-stu-id="57a0a-155">NOTES</span></span>
<span data-ttu-id="57a0a-156">A causa dell'impatto potenzialmente elevato dell'eliminazione di una zona DNS, per impostazione predefinita, questo cmdlet richiede la conferma se la $ConfirmPreference variabile di Windows PowerShell contiene un valore diverso da None.</span><span class="sxs-lookup"><span data-stu-id="57a0a-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="57a0a-157">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="57a0a-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="57a0a-158">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="57a0a-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="57a0a-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57a0a-159">RELATED LINKS</span></span>

[<span data-ttu-id="57a0a-160">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57a0a-160">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="57a0a-161">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57a0a-161">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="57a0a-162">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="57a0a-162">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
