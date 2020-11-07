---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678856"
---
# <span data-ttu-id="89088-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89088-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="89088-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89088-102">SYNOPSIS</span></span>
<span data-ttu-id="89088-103">Ottiene un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="89088-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="89088-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89088-104">SYNTAX</span></span>

### <span data-ttu-id="89088-105">Campi</span><span class="sxs-lookup"><span data-stu-id="89088-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89088-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="89088-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89088-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89088-107">DESCRIPTION</span></span>
<span data-ttu-id="89088-108">Il cmdlet **Get-AzDnsRecordSet** ottiene il record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="89088-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="89088-109">Se non specifichi i parametri *Name* o *RecordType* , questo cmdlet restituisce tutti i set di record del tipo specificato nella zona.</span><span class="sxs-lookup"><span data-stu-id="89088-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="89088-110">Se specifichi il parametro *RecordType* ma non il parametro *Name* , questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="89088-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="89088-111">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro di *zona* o in alternativa puoi specificare il gruppo zona e risorsa per nome.</span><span class="sxs-lookup"><span data-stu-id="89088-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="89088-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89088-112">EXAMPLES</span></span>

### <span data-ttu-id="89088-113">Esempio 1: ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="89088-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="89088-114">Questo comando ottiene il set di record del tipo di record un nome www nel gruppo di risorse e nella zona specificati e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="89088-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="89088-115">Poiché vengono specificati i parametri *Name* e *RecordType* , viene restituito un solo oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="89088-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="89088-116">Esempio 2: ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="89088-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="89088-117">Questo comando ottiene una matrice di tutti i set di record del tipo di record a nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="89088-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="89088-118">Esempio 3: ottenere tutti i set di record in una zona</span><span class="sxs-lookup"><span data-stu-id="89088-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="89088-119">Questo comando consente di ottenere una matrice di tutti i set di record nella zona denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi di archiviarli nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="89088-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="89088-120">Esempio 4: ottenere tutti i set di record in una zona usando un oggetto DnsZone</span><span class="sxs-lookup"><span data-stu-id="89088-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="89088-121">Questo esempio equivale all'esempio 3 precedente.</span><span class="sxs-lookup"><span data-stu-id="89088-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="89088-122">Questa volta, la zona viene specificata usando un oggetto zone.</span><span class="sxs-lookup"><span data-stu-id="89088-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="89088-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89088-123">PARAMETERS</span></span>

### <span data-ttu-id="89088-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89088-124">-DefaultProfile</span></span>
<span data-ttu-id="89088-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="89088-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89088-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="89088-126">-Name</span></span>
<span data-ttu-id="89088-127">Specifica il nome del **Recordset** da ottenere.</span><span class="sxs-lookup"><span data-stu-id="89088-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="89088-128">Se non specifichi il parametro *Name* , verranno restituiti tutti i set di record del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="89088-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89088-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="89088-129">-RecordType</span></span>
<span data-ttu-id="89088-130">Specifica il tipo di record DNS ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89088-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="89088-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="89088-131">Valid values are:</span></span> 
- <span data-ttu-id="89088-132">Un</span><span class="sxs-lookup"><span data-stu-id="89088-132">A</span></span>
- <span data-ttu-id="89088-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="89088-133">AAAA</span></span>
- <span data-ttu-id="89088-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="89088-134">CNAME</span></span>
- <span data-ttu-id="89088-135">MX</span><span class="sxs-lookup"><span data-stu-id="89088-135">MX</span></span>
- <span data-ttu-id="89088-136">NS</span><span class="sxs-lookup"><span data-stu-id="89088-136">NS</span></span>
- <span data-ttu-id="89088-137">PTR</span><span class="sxs-lookup"><span data-stu-id="89088-137">PTR</span></span>
- <span data-ttu-id="89088-138">SOA</span><span class="sxs-lookup"><span data-stu-id="89088-138">SOA</span></span>
- <span data-ttu-id="89088-139">SRV</span><span class="sxs-lookup"><span data-stu-id="89088-139">SRV</span></span>
- <span data-ttu-id="89088-140">TXT se non specifichi il parametro *RecordType* , devi anche omettere il parametro *Name* .</span><span class="sxs-lookup"><span data-stu-id="89088-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="89088-141">Questo cmdlet restituisce quindi tutti i set di record nella zona (di tutti i nomi e i tipi).</span><span class="sxs-lookup"><span data-stu-id="89088-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89088-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89088-142">-ResourceGroupName</span></span>
<span data-ttu-id="89088-143">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="89088-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="89088-144">Il nome della zona deve essere specificato anche usando il parametro *zonename* .</span><span class="sxs-lookup"><span data-stu-id="89088-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="89088-145">In alternativa, puoi specificare il gruppo zona e risorsa passando un oggetto **dnsZone** usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="89088-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="89088-146">-Zona</span><span class="sxs-lookup"><span data-stu-id="89088-146">-Zone</span></span>
<span data-ttu-id="89088-147">Specifica la zona DNS che contiene il set di record ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89088-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="89088-148">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="89088-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="89088-149">-Zonename</span><span class="sxs-lookup"><span data-stu-id="89088-149">-ZoneName</span></span>
<span data-ttu-id="89088-150">Specifica il nome della zona DNS che contiene il record impostato per ottenere.</span><span class="sxs-lookup"><span data-stu-id="89088-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="89088-151">Il gruppo di risorse che contiene la zona deve essere specificato anche usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="89088-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="89088-152">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="89088-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="89088-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89088-153">CommonParameters</span></span>
<span data-ttu-id="89088-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89088-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89088-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89088-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89088-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89088-156">INPUTS</span></span>

### <span data-ttu-id="89088-157">System. String</span><span class="sxs-lookup"><span data-stu-id="89088-157">System.String</span></span>

### <span data-ttu-id="89088-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="89088-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="89088-159">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="89088-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="89088-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89088-160">OUTPUTS</span></span>

### <span data-ttu-id="89088-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89088-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="89088-162">Note</span><span class="sxs-lookup"><span data-stu-id="89088-162">NOTES</span></span>

## <span data-ttu-id="89088-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89088-163">RELATED LINKS</span></span>

[<span data-ttu-id="89088-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89088-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="89088-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89088-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="89088-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="89088-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


