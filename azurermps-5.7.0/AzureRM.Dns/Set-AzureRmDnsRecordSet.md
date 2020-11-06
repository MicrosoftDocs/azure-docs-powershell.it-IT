---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsRecordSet.md
ms.openlocfilehash: 69cdea37f0a736c13d561ecd0d6864f3ef71b466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520460"
---
# <span data-ttu-id="d4ab3-101">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-101">Set-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="d4ab3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ab3-103">Aggiorna un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-103">Updates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4ab3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4ab3-104">SYNTAX</span></span>

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ab3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="d4ab3-106">Il cmdlet **set-AzureRmDnsRecordSet** aggiorna un set di record nel servizio Azure DNS da un oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-106">The **Set-AzureRmDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="d4ab3-107">Puoi passare un oggetto **Recordset** come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="d4ab3-108">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="d4ab3-109">Il set di record non viene aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d4ab3-110">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d4ab3-111">Puoi eliminare questo comportamento usando il parametro *overwrite* , che aggiorna il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d4ab3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4ab3-112">EXAMPLES</span></span>

### <span data-ttu-id="d4ab3-113">Esempio 1: aggiornare un set di record</span><span class="sxs-lookup"><span data-stu-id="d4ab3-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="d4ab3-114">Il primo comando usa il cmdlet Get-AzureRmDnsRecordSet per ottenere il set di record specificato e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-114">The first command uses the Get-AzureRmDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="d4ab3-115">Il secondo e il terzo comando sono operazioni off-line per aggiungere due record al set di record.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="d4ab3-116">Il comando finale usa il cmdlet **set-AzureRmDnsRecordSet** per eseguire il commit dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-116">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="d4ab3-117">Esempio 2: aggiornare un record SOA</span><span class="sxs-lookup"><span data-stu-id="d4ab3-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="d4ab3-118">Il primo comando usa il cmdlet **Get-AzureRmDnsRecordset** per ottenere il set di record specificato e lo archivia nella variabile $recordset.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-118">The first command uses the **Get-AzureRmDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="d4ab3-119">Il secondo comando Aggiorna il record SOA specificato in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="d4ab3-120">Il comando Final usa il cmdlet **set-AzureRmDnsRecordSet** per propagare l'aggiornamento in $recordset.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-120">The final command uses the **Set-AzureRmDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d4ab3-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4ab3-121">PARAMETERS</span></span>

### <span data-ttu-id="d4ab3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ab3-122">-DefaultProfile</span></span>
<span data-ttu-id="d4ab3-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d4ab3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4ab3-124">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="d4ab3-124">-Overwrite</span></span>
<span data-ttu-id="d4ab3-125">Indica di aggiornare il set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-125">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="d4ab3-126">Il set di record non verrà aggiornato se è stato modificato in Azure DNS dopo che è stato recuperato l'oggetto **Recordset** locale.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="d4ab3-127">In questo articolo viene fornita la protezione delle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="d4ab3-128">Per eliminare questo comportamento, puoi usare il parametro *overwrite* , che determina l'aggiornamento del set di record indipendentemente dalle modifiche simultanee.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d4ab3-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-129">-RecordSet</span></span>
<span data-ttu-id="d4ab3-130">Specifica il **Recordset** da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4ab3-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d4ab3-131">-Confirm</span></span>
<span data-ttu-id="d4ab3-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ab3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ab3-133">-WhatIf</span></span>
<span data-ttu-id="d4ab3-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4ab3-135">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4ab3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ab3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ab3-137">CommonParameters</span></span>
<span data-ttu-id="d4ab3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ab3-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ab3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ab3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4ab3-140">INPUTS</span></span>

### <span data-ttu-id="d4ab3-141">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d4ab3-142">Puoi passare un oggetto **Recordset** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-142">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="d4ab3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4ab3-143">OUTPUTS</span></span>

### <span data-ttu-id="d4ab3-144">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-144">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d4ab3-145">Questo cmdlet restituisce un oggetto che rappresenta l'oggetto **Recordset** aggiornato.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-145">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="d4ab3-146">Note</span><span class="sxs-lookup"><span data-stu-id="d4ab3-146">NOTES</span></span>
<span data-ttu-id="d4ab3-147">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-147">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d4ab3-148">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-148">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="d4ab3-149">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-149">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d4ab3-150">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="d4ab3-150">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="d4ab3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4ab3-151">RELATED LINKS</span></span>

[<span data-ttu-id="d4ab3-152">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-152">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d4ab3-153">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-153">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d4ab3-154">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d4ab3-154">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)
