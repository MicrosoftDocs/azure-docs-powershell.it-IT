---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202181"
---
# <span data-ttu-id="ff1a4-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="ff1a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1a4-103">Aggiorna un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="ff1a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff1a4-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff1a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff1a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ff1a4-106">Il cmdlet **set-AzDnsRecordSet** aggiorna un set di record nel servizio Azure DNS da un oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="ff1a4-107">Puoi passare un oggetto **Recordset** come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="ff1a4-108">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ff1a4-109">Il set di record non viene aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ff1a4-110">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ff1a4-111">Puoi eliminare questo comportamento usando il parametro *overwrite* , che aggiorna il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="ff1a4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff1a4-112">EXAMPLES</span></span>

### <span data-ttu-id="ff1a4-113">Esempio 1: aggiornare un set di record</span><span class="sxs-lookup"><span data-stu-id="ff1a4-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="ff1a4-114">Il primo comando usa il cmdlet Get-AzDnsRecordSet per ottenere il set di record specificato e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ff1a4-115">Il secondo e il terzo comando sono operazioni off-line per aggiungere due record al set di record.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="ff1a4-116">Il comando finale usa il cmdlet **set-AzDnsRecordSet** per eseguire il commit dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="ff1a4-117">Esempio 2: aggiornare un record SOA</span><span class="sxs-lookup"><span data-stu-id="ff1a4-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="ff1a4-118">Il primo comando usa il cmdlet **Get-AzDnsRecordset** per ottenere il set di record specificato e lo archivia nella variabile $recordset.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ff1a4-119">Il secondo comando Aggiorna il record SOA specificato in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="ff1a4-120">Il comando Final usa il cmdlet **set-AzDnsRecordSet** per propagare l'aggiornamento in $recordset.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="ff1a4-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff1a4-121">PARAMETERS</span></span>

### <span data-ttu-id="ff1a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1a4-122">-DefaultProfile</span></span>
<span data-ttu-id="ff1a4-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ff1a4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff1a4-124">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="ff1a4-124">-Overwrite</span></span>
<span data-ttu-id="ff1a4-125">Indica di aggiornare il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="ff1a4-126">Il set di record non verrà aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="ff1a4-127">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="ff1a4-128">Per eliminare questo comportamento, puoi usare il parametro *overwrite* , che determina l'aggiornamento del set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ff1a4-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-129">-RecordSet</span></span>
<span data-ttu-id="ff1a4-130">Specifica il **Recordset** da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-130">Specifies the **RecordSet** to update.</span></span>

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

### <span data-ttu-id="ff1a4-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff1a4-131">-Confirm</span></span>
<span data-ttu-id="ff1a4-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff1a4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff1a4-133">-WhatIf</span></span>
<span data-ttu-id="ff1a4-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff1a4-135">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff1a4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff1a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1a4-137">CommonParameters</span></span>
<span data-ttu-id="ff1a4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1a4-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1a4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1a4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff1a4-140">INPUTS</span></span>

### <span data-ttu-id="ff1a4-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ff1a4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff1a4-142">OUTPUTS</span></span>

### <span data-ttu-id="ff1a4-143">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ff1a4-144">Note</span><span class="sxs-lookup"><span data-stu-id="ff1a4-144">NOTES</span></span>
<span data-ttu-id="ff1a4-145">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ff1a4-146">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ff1a4-147">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ff1a4-148">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ff1a4-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="ff1a4-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff1a4-149">RELATED LINKS</span></span>

[<span data-ttu-id="ff1a4-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="ff1a4-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="ff1a4-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ff1a4-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)
