---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519470"
---
# <span data-ttu-id="2e4e3-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2e4e3-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="2e4e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e4e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4e3-103">Ottiene un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e4e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e4e3-104">SYNTAX</span></span>

### <span data-ttu-id="2e4e3-105">Campi</span><span class="sxs-lookup"><span data-stu-id="2e4e3-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e4e3-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2e4e3-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e4e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e4e3-107">DESCRIPTION</span></span>
<span data-ttu-id="2e4e3-108">Il cmdlet **Get-AzureRmDnsRecordSet** ottiene il record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="2e4e3-109">Se non specifichi i parametri *Name* o *RecordType* , questo cmdlet restituisce tutti i set di record del tipo specificato nella zona.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="2e4e3-110">Se specifichi il parametro *RecordType* ma non il parametro *Name* , questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="2e4e3-111">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro di *zona* o in alternativa puoi specificare il gruppo zona e risorsa per nome.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="2e4e3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e4e3-112">EXAMPLES</span></span>

### <span data-ttu-id="2e4e3-113">Esempio 1: ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="2e4e3-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="2e4e3-114">Questo comando ottiene il set di record del tipo di record un nome www nel gruppo di risorse e nella zona specificati e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="2e4e3-115">Poiché vengono specificati i parametri *Name* e *RecordType* , viene restituito un solo oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="2e4e3-116">Esempio 2: ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="2e4e3-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="2e4e3-117">Questo comando ottiene una matrice di tutti i set di record del tipo di record a nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="2e4e3-118">Esempio 3: ottenere tutti i set di record in una zona</span><span class="sxs-lookup"><span data-stu-id="2e4e3-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="2e4e3-119">Questo comando consente di ottenere una matrice di tutti i set di record nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi di archiviarli nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="2e4e3-120">Esempio 4: ottenere tutti i set di record in una zona usando un oggetto DnsZone</span><span class="sxs-lookup"><span data-stu-id="2e4e3-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="2e4e3-121">Questo esempio equivale all'esempio 3 precedente.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="2e4e3-122">Questa volta, la zona viene specificata usando un oggetto zone.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="2e4e3-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e4e3-123">PARAMETERS</span></span>

### <span data-ttu-id="2e4e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4e3-124">-DefaultProfile</span></span>
<span data-ttu-id="2e4e3-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2e4e3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e4e3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e4e3-126">-Name</span></span>
<span data-ttu-id="2e4e3-127">Specifica il nome del **Recordset** da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="2e4e3-128">Se non specifichi il parametro *Name* , verranno restituiti tutti i set di record del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="2e4e3-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="2e4e3-129">-RecordType</span></span>
<span data-ttu-id="2e4e3-130">Specifica il tipo di record DNS ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-130">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="2e4e3-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="2e4e3-131">Valid values are:</span></span> 

- <span data-ttu-id="2e4e3-132">Un</span><span class="sxs-lookup"><span data-stu-id="2e4e3-132">A</span></span>
- <span data-ttu-id="2e4e3-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="2e4e3-133">AAAA</span></span>
- <span data-ttu-id="2e4e3-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="2e4e3-134">CNAME</span></span>
- <span data-ttu-id="2e4e3-135">MX</span><span class="sxs-lookup"><span data-stu-id="2e4e3-135">MX</span></span>
- <span data-ttu-id="2e4e3-136">NS</span><span class="sxs-lookup"><span data-stu-id="2e4e3-136">NS</span></span>
- <span data-ttu-id="2e4e3-137">PTR</span><span class="sxs-lookup"><span data-stu-id="2e4e3-137">PTR</span></span>
- <span data-ttu-id="2e4e3-138">SOA</span><span class="sxs-lookup"><span data-stu-id="2e4e3-138">SOA</span></span>
- <span data-ttu-id="2e4e3-139">SRV</span><span class="sxs-lookup"><span data-stu-id="2e4e3-139">SRV</span></span>
- <span data-ttu-id="2e4e3-140">TXT</span><span class="sxs-lookup"><span data-stu-id="2e4e3-140">TXT</span></span>

<span data-ttu-id="2e4e3-141">Se non specifichi il parametro *RecordType* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-141">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="2e4e3-142">Questo cmdlet restituisce quindi tutti i set di record nella zona (di tutti i nomi e i tipi).</span><span class="sxs-lookup"><span data-stu-id="2e4e3-142">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="2e4e3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4e3-143">-ResourceGroupName</span></span>
<span data-ttu-id="2e4e3-144">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-144">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="2e4e3-145">Il nome della zona deve essere specificato anche usando il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-145">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="2e4e3-146">In alternativa, puoi specificare il gruppo zona e risorsa passando un oggetto **dnsZone** usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-146">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2e4e3-147">-Zona</span><span class="sxs-lookup"><span data-stu-id="2e4e3-147">-Zone</span></span>
<span data-ttu-id="2e4e3-148">Specifica la zona DNS che contiene il set di record ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-148">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="2e4e3-149">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-149">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="2e4e3-150">-Zonename</span><span class="sxs-lookup"><span data-stu-id="2e4e3-150">-ZoneName</span></span>
<span data-ttu-id="2e4e3-151">Specifica il nome della zona DNS che contiene il record impostato per ottenere.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-151">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="2e4e3-152">Il gruppo di risorse che contiene la zona deve essere specificato anche usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-152">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="2e4e3-153">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-153">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2e4e3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4e3-154">CommonParameters</span></span>
<span data-ttu-id="2e4e3-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4e3-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4e3-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e4e3-157">INPUTS</span></span>

### <span data-ttu-id="2e4e3-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="2e4e3-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2e4e3-159">Puoi reindirizzare un oggetto **dnsZone** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-159">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="2e4e3-160">L'oggetto **dnsZone** rappresenta l'area in cui cercare l'oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2e4e3-160">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="2e4e3-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e4e3-161">OUTPUTS</span></span>

### <span data-ttu-id="2e4e3-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2e4e3-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="2e4e3-163">Questo cmdlet restituisce uno o più oggetti che rappresentano i set di record trovati.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-163">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="2e4e3-164">Verrà restituito al massimo un **Recordset** se sono specificati i parametri *Name* e *RecordType* , in caso contrario vengono restituiti più oggetti **Recordset** come matrice.</span><span class="sxs-lookup"><span data-stu-id="2e4e3-164">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="2e4e3-165">Note</span><span class="sxs-lookup"><span data-stu-id="2e4e3-165">NOTES</span></span>

## <span data-ttu-id="2e4e3-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e4e3-166">RELATED LINKS</span></span>

[<span data-ttu-id="2e4e3-167">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2e4e3-167">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="2e4e3-168">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2e4e3-168">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="2e4e3-169">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2e4e3-169">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

