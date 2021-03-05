---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984743"
---
# <span data-ttu-id="c3977-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="c3977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3977-102">SYNOPSIS</span></span>
<span data-ttu-id="c3977-103">Aggiorna un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="c3977-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="c3977-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3977-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3977-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3977-105">DESCRIPTION</span></span>
<span data-ttu-id="c3977-106">Il cmdlet **Set-AzDnsRecordSet** aggiorna un set di record nel servizio DNS di Azure da un oggetto **RecordSet** locale.</span><span class="sxs-lookup"><span data-stu-id="c3977-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="c3977-107">È possibile passare un **oggetto RecordSet** come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3977-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="c3977-108">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c3977-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c3977-109">Il set di record non viene aggiornato se è stato modificato nel DNS di Azure dopo il recupero **dell'oggetto RecordSet** locale.</span><span class="sxs-lookup"><span data-stu-id="c3977-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="c3977-110">Questo fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="c3977-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="c3977-111">È possibile disattivare questo comportamento usando il *parametro Overwrite,* che aggiorna il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="c3977-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="c3977-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3977-112">EXAMPLES</span></span>

### <span data-ttu-id="c3977-113">Esempio 1: Aggiornare un set di record</span><span class="sxs-lookup"><span data-stu-id="c3977-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="c3977-114">Il primo comando usa il cmdlet Get-AzDnsRecordSet per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.</span><span class="sxs-lookup"><span data-stu-id="c3977-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c3977-115">Il secondo e il terzo comando sono operazioni non in linea per aggiungere due record A al set di record.</span><span class="sxs-lookup"><span data-stu-id="c3977-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="c3977-116">Il comando finale usa il cmdlet **Set-AzDnsRecordSet** per eseguire il commit dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c3977-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="c3977-117">Esempio 2: Aggiornare un record SOA</span><span class="sxs-lookup"><span data-stu-id="c3977-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="c3977-118">Il primo comando usa il cmdlet **Get-AzDnsRecordset** per ottenere il set di record specificato e quindi lo archivia nella $RecordSet variabile.</span><span class="sxs-lookup"><span data-stu-id="c3977-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c3977-119">Il secondo comando aggiorna il record SOA specificato in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c3977-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="c3977-120">Il comando finale usa il cmdlet **Set-AzDnsRecordSet** per propagare l'aggiornamento in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="c3977-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="c3977-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3977-121">PARAMETERS</span></span>

### <span data-ttu-id="c3977-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3977-122">-DefaultProfile</span></span>
<span data-ttu-id="c3977-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c3977-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3977-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c3977-124">-Overwrite</span></span>
<span data-ttu-id="c3977-125">Indica di aggiornare il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="c3977-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="c3977-126">Il set di record non verrà aggiornato se è stato modificato nel DNS di Azure dopo il recupero **dell'oggetto RecordSet** locale.</span><span class="sxs-lookup"><span data-stu-id="c3977-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="c3977-127">Questo fornisce protezione per le modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="c3977-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="c3977-128">Per disattivare questo comportamento, è possibile usare il parametro *Overwrite,* che comporta l'aggiornamento del set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="c3977-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="c3977-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-129">-RecordSet</span></span>
<span data-ttu-id="c3977-130">Specifica il **RecordSet da** aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c3977-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3977-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3977-131">-Confirm</span></span>
<span data-ttu-id="c3977-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3977-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3977-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3977-133">-WhatIf</span></span>
<span data-ttu-id="c3977-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3977-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3977-135">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3977-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3977-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3977-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3977-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3977-137">CommonParameters</span></span>
<span data-ttu-id="c3977-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3977-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3977-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3977-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3977-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3977-140">INPUTS</span></span>

### <span data-ttu-id="c3977-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c3977-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3977-142">OUTPUTS</span></span>

### <span data-ttu-id="c3977-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c3977-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3977-144">NOTES</span></span>
<span data-ttu-id="c3977-145">È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c3977-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c3977-146">Per impostazione predefinita, il cmdlet chiede conferma se la $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="c3977-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="c3977-147">Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c3977-147">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c3977-148">Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c3977-148">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="c3977-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3977-149">RELATED LINKS</span></span>

[<span data-ttu-id="c3977-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="c3977-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="c3977-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3977-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
