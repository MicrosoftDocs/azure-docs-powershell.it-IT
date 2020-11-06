---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: ac3f65ed82f9b04eb49e26a8cb03a3dcd8c9bc34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520462"
---
# <span data-ttu-id="dd7d1-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="dd7d1-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="dd7d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7d1-103">Rimuove una zona DNS da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd7d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd7d1-104">SYNTAX</span></span>

### <span data-ttu-id="dd7d1-105">Campi</span><span class="sxs-lookup"><span data-stu-id="dd7d1-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7d1-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="dd7d1-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd7d1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd7d1-107">DESCRIPTION</span></span>
<span data-ttu-id="dd7d1-108">Il cmdlet **Remove-AzureRmDnsZone** Elimina definitivamente una zona DNS (Domain Name System) da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="dd7d1-109">Vengono eliminati anche tutti i set di record contenuti nella zona.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="dd7d1-110">Puoi passare un oggetto **dnsZone** usando il parametro *Name* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="dd7d1-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="dd7d1-112">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="dd7d1-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="dd7d1-113">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="dd7d1-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="dd7d1-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd7d1-115">EXAMPLES</span></span>

### <span data-ttu-id="dd7d1-116">Esempio 1: rimuovere un'area</span><span class="sxs-lookup"><span data-stu-id="dd7d1-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="dd7d1-117">Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="dd7d1-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd7d1-118">PARAMETERS</span></span>

### <span data-ttu-id="dd7d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7d1-119">-DefaultProfile</span></span>
<span data-ttu-id="dd7d1-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dd7d1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd7d1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dd7d1-121">-Force</span></span>
<span data-ttu-id="dd7d1-122">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-122">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="dd7d1-123">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-123">It will be removed in a future release.</span></span>

<span data-ttu-id="dd7d1-124">Per verificare se questo cmdlet richiede la conferma, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-124">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="dd7d1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd7d1-125">-Name</span></span>
<span data-ttu-id="dd7d1-126">Specifica il nome dell'area DNS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-126">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="dd7d1-127">Devi anche specificare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-127">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="dd7d1-128">In alternativa, puoi specificare la zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-128">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="dd7d1-129">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="dd7d1-129">-Overwrite</span></span>
<span data-ttu-id="dd7d1-130">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="dd7d1-130">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="dd7d1-131">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-131">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="dd7d1-132">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-132">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="dd7d1-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd7d1-133">-PassThru</span></span>
<span data-ttu-id="dd7d1-134">PassThru</span><span class="sxs-lookup"><span data-stu-id="dd7d1-134">passthru</span></span>

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

### <span data-ttu-id="dd7d1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7d1-135">-ResourceGroupName</span></span>
<span data-ttu-id="dd7d1-136">Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-136">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="dd7d1-137">Devi anche specificare il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-137">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="dd7d1-138">In alternativa, puoi specificare la zona DNS usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-138">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="dd7d1-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="dd7d1-139">-Zone</span></span>
<span data-ttu-id="dd7d1-140">Specifica la zona DNS da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-140">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="dd7d1-141">L'oggetto **dnsZone** passato può essere passato anche tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-141">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="dd7d1-142">In alternativa, puoi specificare la zona DNS da eliminare usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-142">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="dd7d1-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd7d1-143">-Confirm</span></span>
<span data-ttu-id="dd7d1-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7d1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd7d1-145">-WhatIf</span></span>
<span data-ttu-id="dd7d1-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7d1-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7d1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7d1-148">CommonParameters</span></span>
<span data-ttu-id="dd7d1-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7d1-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd7d1-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7d1-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd7d1-151">INPUTS</span></span>

### <span data-ttu-id="dd7d1-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="dd7d1-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="dd7d1-153">Puoi reindirizzare un oggetto **dnsZone** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="dd7d1-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd7d1-154">OUTPUTS</span></span>

### <span data-ttu-id="dd7d1-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd7d1-155">None</span></span>
<span data-ttu-id="dd7d1-156">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="dd7d1-157">Note</span><span class="sxs-lookup"><span data-stu-id="dd7d1-157">NOTES</span></span>
<span data-ttu-id="dd7d1-158">A causa dell'impatto potenzialmente elevato dell'eliminazione di una zona DNS, per impostazione predefinita, questo cmdlet richiede la conferma se la $ConfirmPreference variabile di Windows PowerShell contiene un valore diverso da None.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="dd7d1-159">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="dd7d1-160">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="dd7d1-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="dd7d1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd7d1-161">RELATED LINKS</span></span>

[<span data-ttu-id="dd7d1-162">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="dd7d1-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="dd7d1-163">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="dd7d1-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="dd7d1-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="dd7d1-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
