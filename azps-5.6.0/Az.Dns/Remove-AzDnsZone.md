---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984744"
---
# <span data-ttu-id="90a26-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="90a26-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="90a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a26-102">SYNOPSIS</span></span>
<span data-ttu-id="90a26-103">Rimuove un'area DNS da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90a26-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="90a26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90a26-104">SYNTAX</span></span>

### <span data-ttu-id="90a26-105">Campi</span><span class="sxs-lookup"><span data-stu-id="90a26-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a26-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="90a26-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a26-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="90a26-107">DESCRIPTION</span></span>
<span data-ttu-id="90a26-108">Il cmdlet **Remove-AzDnsZone** elimina definitivamente un'area DNS (Domain Name System) da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="90a26-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="90a26-109">Vengono eliminati anche tutti i set di record contenuti nell'area.</span><span class="sxs-lookup"><span data-stu-id="90a26-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="90a26-110">È possibile passare un **oggetto DnsZone** usando il parametro *Name* o usando l'operatore pipeline oppure in alternativa è possibile specificare i parametri *ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="90a26-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="90a26-111">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="90a26-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="90a26-112">Quando si specifica l'area usando un oggetto **DnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché l'oggetto **DnsZone** locale è stato recuperato (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).</span><span class="sxs-lookup"><span data-stu-id="90a26-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="90a26-113">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="90a26-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="90a26-114">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="90a26-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="90a26-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90a26-115">EXAMPLES</span></span>

### <span data-ttu-id="90a26-116">Esempio 1: Rimuovere un'area</span><span class="sxs-lookup"><span data-stu-id="90a26-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="90a26-117">Questo comando rimuove l'area myzone.com denominata risorse dal gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="90a26-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="90a26-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a26-118">PARAMETERS</span></span>

### <span data-ttu-id="90a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a26-119">-DefaultProfile</span></span>
<span data-ttu-id="90a26-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90a26-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90a26-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90a26-121">-Name</span></span>
<span data-ttu-id="90a26-122">Specifica il nome dell'area DNS rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a26-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="90a26-123">È anche necessario specificare il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="90a26-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="90a26-124">In alternativa, è possibile specificare l'area DNS usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="90a26-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="90a26-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="90a26-125">-Overwrite</span></span>
<span data-ttu-id="90a26-126">Quando si specifica l'area usando un oggetto **DnsZone** (passato tramite la pipeline o il parametro *Zone),* l'area non viene eliminata se è stata modificata nel DNS di Azure perché l'oggetto **DnsZone** locale è stato recuperato (solo le operazioni direttamente nella risorsa zona DNS vengono conteggiati come modifiche, non le operazioni sui set di record all'interno dell'area).</span><span class="sxs-lookup"><span data-stu-id="90a26-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="90a26-127">Ciò fornisce protezione per le modifiche simultanee all'area.</span><span class="sxs-lookup"><span data-stu-id="90a26-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="90a26-128">Questa operazione può essere soppressa con il parametro *Overwrite,* che elimina l'area indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="90a26-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="90a26-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90a26-129">-PassThru</span></span>
<span data-ttu-id="90a26-130">passthru</span><span class="sxs-lookup"><span data-stu-id="90a26-130">passthru</span></span>

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

### <span data-ttu-id="90a26-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a26-131">-ResourceGroupName</span></span>
<span data-ttu-id="90a26-132">Specifica il nome del gruppo di risorse che contiene l'area da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="90a26-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="90a26-133">È anche necessario specificare il *parametro ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="90a26-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="90a26-134">In alternativa, è possibile specificare l'area DNS usando un **oggetto DnsZone,** passato tramite la pipeline o il parametro *Zone.*</span><span class="sxs-lookup"><span data-stu-id="90a26-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="90a26-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="90a26-135">-Zone</span></span>
<span data-ttu-id="90a26-136">Specifica l'area DNS da eliminare.</span><span class="sxs-lookup"><span data-stu-id="90a26-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="90a26-137">**L'oggetto DnsZone** passato può essere passato anche tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="90a26-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="90a26-138">In alternativa, è possibile specificare l'area DNS da eliminare usando i parametri *ZoneName* *e ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="90a26-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="90a26-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90a26-139">-Confirm</span></span>
<span data-ttu-id="90a26-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a26-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a26-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a26-141">-WhatIf</span></span>
<span data-ttu-id="90a26-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90a26-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a26-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90a26-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a26-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a26-144">CommonParameters</span></span>
<span data-ttu-id="90a26-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a26-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a26-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a26-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a26-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="90a26-147">INPUTS</span></span>

### <span data-ttu-id="90a26-148">System.String</span><span class="sxs-lookup"><span data-stu-id="90a26-148">System.String</span></span>

### <span data-ttu-id="90a26-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="90a26-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="90a26-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90a26-150">OUTPUTS</span></span>

### <span data-ttu-id="90a26-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90a26-151">System.Boolean</span></span>

## <span data-ttu-id="90a26-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="90a26-152">NOTES</span></span>
<span data-ttu-id="90a26-153">A causa dell'impatto potenziale dell'eliminazione di un'area DNS, per impostazione predefinita questo cmdlet richiede conferma se la variabile $ConfirmPreference Windows PowerShell ha un valore diverso da Nessuno.</span><span class="sxs-lookup"><span data-stu-id="90a26-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="90a26-154">Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="90a26-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="90a26-155">Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="90a26-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="90a26-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90a26-156">RELATED LINKS</span></span>

[<span data-ttu-id="90a26-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="90a26-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="90a26-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="90a26-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="90a26-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="90a26-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
