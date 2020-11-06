---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518676"
---
# <span data-ttu-id="79639-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="79639-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="79639-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79639-102">SYNOPSIS</span></span>
<span data-ttu-id="79639-103">Rimuove una zona DNS da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79639-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79639-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79639-104">SYNTAX</span></span>

### <span data-ttu-id="79639-105">Campi</span><span class="sxs-lookup"><span data-stu-id="79639-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79639-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="79639-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79639-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79639-107">DESCRIPTION</span></span>
<span data-ttu-id="79639-108">Il cmdlet **Remove-AzureRmDnsZone** Elimina definitivamente una zona DNS (Domain Name System) da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="79639-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="79639-109">Vengono eliminati anche tutti i set di record contenuti nella zona.</span><span class="sxs-lookup"><span data-stu-id="79639-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="79639-110">Puoi passare un oggetto **dnsZone** usando il parametro *Name* oppure usando l'operatore pipeline o in alternativa puoi specificare i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="79639-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="79639-111">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="79639-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="79639-112">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="79639-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="79639-113">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="79639-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="79639-114">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="79639-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="79639-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79639-115">EXAMPLES</span></span>

### <span data-ttu-id="79639-116">Esempio 1: rimuovere un'area</span><span class="sxs-lookup"><span data-stu-id="79639-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="79639-117">Questo comando rimuove la zona denominata myzone.com dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="79639-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="79639-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79639-118">PARAMETERS</span></span>

### <span data-ttu-id="79639-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79639-119">-DefaultProfile</span></span>
<span data-ttu-id="79639-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79639-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79639-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="79639-121">-Name</span></span>
<span data-ttu-id="79639-122">Specifica il nome dell'area DNS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79639-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="79639-123">Devi anche specificare il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="79639-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="79639-124">In alternativa, puoi specificare la zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="79639-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="79639-125">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="79639-125">-Overwrite</span></span>
<span data-ttu-id="79639-126">Quando specifichi la zona usando un oggetto **dnsZone** (passato tramite il parametro pipeline o *zone* ), la zona non viene eliminata se è stata modificata in Azure DNS poiché l'oggetto **dnsZone** locale è stato recuperato (solo le operazioni direttamente nel conteggio delle risorse di zona DNS come le modifiche, le operazioni sui set di record all'interno della zona non).</span><span class="sxs-lookup"><span data-stu-id="79639-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="79639-127">Ciò offre protezione per le modifiche di zona simultanee.</span><span class="sxs-lookup"><span data-stu-id="79639-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="79639-128">Questa operazione può essere eliminata usando il parametro *overwrite* , che elimina la zona indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="79639-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="79639-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79639-129">-PassThru</span></span>
<span data-ttu-id="79639-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="79639-130">passthru</span></span>

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

### <span data-ttu-id="79639-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79639-131">-ResourceGroupName</span></span>
<span data-ttu-id="79639-132">Specifica il nome del gruppo di risorse che contiene la zona da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="79639-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="79639-133">Devi anche specificare il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="79639-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="79639-134">In alternativa, puoi specificare la zona DNS usando un oggetto **dnsZone** , passato tramite il parametro pipeline o *zone* .</span><span class="sxs-lookup"><span data-stu-id="79639-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="79639-135">-Zona</span><span class="sxs-lookup"><span data-stu-id="79639-135">-Zone</span></span>
<span data-ttu-id="79639-136">Specifica la zona DNS da eliminare.</span><span class="sxs-lookup"><span data-stu-id="79639-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="79639-137">L'oggetto **dnsZone** passato può essere passato anche tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="79639-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="79639-138">In alternativa, puoi specificare la zona DNS da eliminare usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="79639-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="79639-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79639-139">-Confirm</span></span>
<span data-ttu-id="79639-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79639-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79639-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79639-141">-WhatIf</span></span>
<span data-ttu-id="79639-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79639-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79639-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79639-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79639-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79639-144">CommonParameters</span></span>
<span data-ttu-id="79639-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79639-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79639-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79639-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79639-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79639-147">INPUTS</span></span>

### <span data-ttu-id="79639-148">System. String</span><span class="sxs-lookup"><span data-stu-id="79639-148">System.String</span></span>

### <span data-ttu-id="79639-149">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="79639-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="79639-150">Parameters: zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79639-150">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="79639-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79639-151">OUTPUTS</span></span>

### <span data-ttu-id="79639-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79639-152">System.Boolean</span></span>

## <span data-ttu-id="79639-153">Note</span><span class="sxs-lookup"><span data-stu-id="79639-153">NOTES</span></span>
<span data-ttu-id="79639-154">A causa dell'impatto potenzialmente elevato dell'eliminazione di una zona DNS, per impostazione predefinita, questo cmdlet richiede la conferma se la $ConfirmPreference variabile di Windows PowerShell contiene un valore diverso da None.</span><span class="sxs-lookup"><span data-stu-id="79639-154">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="79639-155">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="79639-155">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="79639-156">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="79639-156">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="79639-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79639-157">RELATED LINKS</span></span>

[<span data-ttu-id="79639-158">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="79639-158">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="79639-159">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="79639-159">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="79639-160">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="79639-160">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
