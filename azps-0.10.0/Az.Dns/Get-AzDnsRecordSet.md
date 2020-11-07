---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 7e1ea1213759e9c4edf9524a36637aff1ef1c12b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863186"
---
# <span data-ttu-id="a1423-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a1423-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="a1423-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1423-102">SYNOPSIS</span></span>
<span data-ttu-id="a1423-103">Ottiene un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="a1423-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="a1423-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1423-104">SYNTAX</span></span>

### <span data-ttu-id="a1423-105">Campi</span><span class="sxs-lookup"><span data-stu-id="a1423-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="a1423-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="a1423-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="a1423-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1423-107">DESCRIPTION</span></span>
<span data-ttu-id="a1423-108">Il cmdlet **Get-AzDnsRecordSet** ottiene il record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="a1423-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="a1423-109">Se non specifichi i parametri *Name* o *RecordType* , questo cmdlet restituisce tutti i set di record del tipo specificato nella zona.</span><span class="sxs-lookup"><span data-stu-id="a1423-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="a1423-110">Se specifichi il parametro *RecordType* ma non il parametro *Name* , questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="a1423-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="a1423-111">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro di *zona* o in alternativa puoi specificare il gruppo zona e risorsa per nome.</span><span class="sxs-lookup"><span data-stu-id="a1423-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="a1423-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1423-112">EXAMPLES</span></span>

### <span data-ttu-id="a1423-113">Esempio 1: ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="a1423-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="a1423-114">Questo comando ottiene il set di record del tipo di record un nome www nel gruppo di risorse e nella zona specificati e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="a1423-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="a1423-115">Poiché vengono specificati i parametri *Name* e *RecordType* , viene restituito un solo oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a1423-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="a1423-116">Esempio 2: ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="a1423-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="a1423-117">Questo comando ottiene una matrice di tutti i set di record del tipo di record a nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a1423-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a1423-118">Esempio 3: ottenere tutti i set di record in una zona</span><span class="sxs-lookup"><span data-stu-id="a1423-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="a1423-119">Questo comando consente di ottenere una matrice di tutti i set di record nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi di archiviarli nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a1423-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a1423-120">Esempio 4: ottenere tutti i set di record in una zona usando un oggetto DnsZone</span><span class="sxs-lookup"><span data-stu-id="a1423-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="a1423-121">Questo esempio equivale all'esempio 3 precedente.</span><span class="sxs-lookup"><span data-stu-id="a1423-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="a1423-122">Questa volta, la zona viene specificata usando un oggetto zone.</span><span class="sxs-lookup"><span data-stu-id="a1423-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="a1423-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1423-123">PARAMETERS</span></span>

### <span data-ttu-id="a1423-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1423-124">-Name</span></span>
<span data-ttu-id="a1423-125">Specifica il nome del **Recordset** da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1423-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="a1423-126">Se non specifichi il parametro *Name* , verranno restituiti tutti i set di record del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="a1423-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1423-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a1423-127">-RecordType</span></span>
<span data-ttu-id="a1423-128">Specifica il tipo di record DNS ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1423-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="a1423-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a1423-129">Valid values are:</span></span> 

- <span data-ttu-id="a1423-130">Un</span><span class="sxs-lookup"><span data-stu-id="a1423-130">A</span></span>
- <span data-ttu-id="a1423-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="a1423-131">AAAA</span></span>
- <span data-ttu-id="a1423-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="a1423-132">CNAME</span></span>
- <span data-ttu-id="a1423-133">MX</span><span class="sxs-lookup"><span data-stu-id="a1423-133">MX</span></span>
- <span data-ttu-id="a1423-134">NS</span><span class="sxs-lookup"><span data-stu-id="a1423-134">NS</span></span>
- <span data-ttu-id="a1423-135">PTR</span><span class="sxs-lookup"><span data-stu-id="a1423-135">PTR</span></span>
- <span data-ttu-id="a1423-136">SOA</span><span class="sxs-lookup"><span data-stu-id="a1423-136">SOA</span></span>
- <span data-ttu-id="a1423-137">SRV</span><span class="sxs-lookup"><span data-stu-id="a1423-137">SRV</span></span>
- <span data-ttu-id="a1423-138">TXT</span><span class="sxs-lookup"><span data-stu-id="a1423-138">TXT</span></span>

<span data-ttu-id="a1423-139">Se non specifichi il parametro *RecordType* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="a1423-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="a1423-140">Questo cmdlet restituisce quindi tutti i set di record nella zona (di tutti i nomi e i tipi).</span><span class="sxs-lookup"><span data-stu-id="a1423-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1423-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1423-141">-ResourceGroupName</span></span>
<span data-ttu-id="a1423-142">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a1423-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a1423-143">Il nome della zona deve essere specificato anche usando il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="a1423-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="a1423-144">In alternativa, puoi specificare il gruppo zona e risorsa passando un oggetto **dnsZone** usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="a1423-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a1423-145">-Zona</span><span class="sxs-lookup"><span data-stu-id="a1423-145">-Zone</span></span>
<span data-ttu-id="a1423-146">Specifica la zona DNS che contiene il set di record ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1423-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="a1423-147">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a1423-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="a1423-148">-Zonename</span><span class="sxs-lookup"><span data-stu-id="a1423-148">-ZoneName</span></span>
<span data-ttu-id="a1423-149">Specifica il nome della zona DNS che contiene il record impostato per ottenere.</span><span class="sxs-lookup"><span data-stu-id="a1423-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="a1423-150">Il gruppo di risorse che contiene la zona deve essere specificato anche usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a1423-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="a1423-151">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="a1423-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a1423-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1423-152">CommonParameters</span></span>
<span data-ttu-id="a1423-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1423-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1423-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1423-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1423-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1423-155">INPUTS</span></span>

### <span data-ttu-id="a1423-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a1423-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a1423-157">Puoi reindirizzare un oggetto **dnsZone** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1423-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="a1423-158">L'oggetto **dnsZone** rappresenta l'area in cui cercare l'oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a1423-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="a1423-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1423-159">OUTPUTS</span></span>

### <span data-ttu-id="a1423-160">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a1423-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a1423-161">Questo cmdlet restituisce uno o più oggetti che rappresentano i set di record trovati.</span><span class="sxs-lookup"><span data-stu-id="a1423-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="a1423-162">Verrà restituito al massimo un **Recordset** se sono specificati i parametri *Name* e *RecordType* , in caso contrario vengono restituiti più oggetti **Recordset** come matrice.</span><span class="sxs-lookup"><span data-stu-id="a1423-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="a1423-163">Note</span><span class="sxs-lookup"><span data-stu-id="a1423-163">NOTES</span></span>

## <span data-ttu-id="a1423-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1423-164">RELATED LINKS</span></span>

[<span data-ttu-id="a1423-165">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a1423-165">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a1423-166">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a1423-166">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="a1423-167">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a1423-167">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


