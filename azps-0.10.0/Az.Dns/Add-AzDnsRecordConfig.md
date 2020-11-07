---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861545"
---
# <span data-ttu-id="a4e5f-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5f-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="a4e5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e5f-103">Aggiunge un record DNS a un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="a4e5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4e5f-104">SYNTAX</span></span>

### <span data-ttu-id="a4e5f-105">Un</span><span class="sxs-lookup"><span data-stu-id="a4e5f-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="a4e5f-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-107">NS</span><span class="sxs-lookup"><span data-stu-id="a4e5f-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-108">MX</span><span class="sxs-lookup"><span data-stu-id="a4e5f-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-109">PTR</span><span class="sxs-lookup"><span data-stu-id="a4e5f-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-110">TXT</span><span class="sxs-lookup"><span data-stu-id="a4e5f-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-111">SRV</span><span class="sxs-lookup"><span data-stu-id="a4e5f-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="a4e5f-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="a4e5f-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="a4e5f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4e5f-113">DESCRIPTION</span></span>
<span data-ttu-id="a4e5f-114">Il cmdlet **Add-AzDnsRecordConfig** aggiunge un record DNS (Domain Name System) a un oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a4e5f-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="a4e5f-115">L'oggetto **Recordset** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non viene eseguito il cmdlet Set-AzDnsRecordSet per rendere persistente la modifica al servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="a4e5f-116">I record SOA vengono creati quando viene creata una zona DNS e vengono rimossi quando viene eliminata la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="a4e5f-117">Non è possibile aggiungere o rimuovere record SOA, ma è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="a4e5f-118">Puoi passare l'oggetto **Recordset** a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="a4e5f-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4e5f-119">EXAMPLES</span></span>

### <span data-ttu-id="a4e5f-120">Esempio 1: aggiungere un record a in un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-121">Questo esempio aggiunge un record a a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="a4e5f-122">Esempio 2: aggiungere un record AAAA a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-123">Questo esempio aggiunge un record AAAA a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="a4e5f-124">Esempio 3: aggiungere un record CNAME a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-125">Questo esempio aggiunge un record CNAME a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="a4e5f-126">Dato che un set di record CNAME può contenere al massimo un record, deve essere inizialmente un set di record vuoto o i record esistenti devono essere rimossi usando Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="a4e5f-127">Esempio 4: aggiungere un record MX a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-128">Questo esempio aggiunge un record MX a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="a4e5f-129">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="a4e5f-130">Esempio 5: aggiungere un record NS a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-131">Questo esempio aggiunge un record NS a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="a4e5f-132">Esempio 6: aggiungere un record PTR a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-133">Questo esempio aggiunge un record PTR a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="a4e5f-134">Esempio 7: aggiungere un record SRV a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-135">Questo esempio aggiunge un record SRV a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="a4e5f-136">Esempio 8: aggiungere un record TXT a un set di record</span><span class="sxs-lookup"><span data-stu-id="a4e5f-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="a4e5f-137">Questo esempio aggiunge un record TXT a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="a4e5f-138">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4e5f-138">PARAMETERS</span></span>

### <span data-ttu-id="a4e5f-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="a4e5f-139">-Cname</span></span>
<span data-ttu-id="a4e5f-140">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="a4e5f-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a4e5f-141">-Exchange</span></span>
<span data-ttu-id="a4e5f-142">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="a4e5f-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-143">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="a4e5f-143">-Ipv4Address</span></span>
<span data-ttu-id="a4e5f-144">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-145">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="a4e5f-145">-Ipv6Address</span></span>
<span data-ttu-id="a4e5f-146">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="a4e5f-147">-Nsdname</span></span>
<span data-ttu-id="a4e5f-148">Specifica il nome del server dei nomi per un record NS (Name Server).</span><span class="sxs-lookup"><span data-stu-id="a4e5f-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-149">-Porta</span><span class="sxs-lookup"><span data-stu-id="a4e5f-149">-Port</span></span>
<span data-ttu-id="a4e5f-150">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="a4e5f-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-151">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="a4e5f-151">-Preference</span></span>
<span data-ttu-id="a4e5f-152">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-153">-Priorità</span><span class="sxs-lookup"><span data-stu-id="a4e5f-153">-Priority</span></span>
<span data-ttu-id="a4e5f-154">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="a4e5f-155">-Ptrdname</span></span>
<span data-ttu-id="a4e5f-156">Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="a4e5f-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="a4e5f-157">-RecordSet</span></span>
<span data-ttu-id="a4e5f-158">Specifica l'oggetto **Recordset** da modificare.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="a4e5f-159">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="a4e5f-159">-Target</span></span>
<span data-ttu-id="a4e5f-160">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-161">-Valore</span><span class="sxs-lookup"><span data-stu-id="a4e5f-161">-Value</span></span>
<span data-ttu-id="a4e5f-162">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-163">-Peso</span><span class="sxs-lookup"><span data-stu-id="a4e5f-163">-Weight</span></span>
<span data-ttu-id="a4e5f-164">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e5f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e5f-165">CommonParameters</span></span>
<span data-ttu-id="a4e5f-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e5f-167">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e5f-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e5f-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4e5f-168">INPUTS</span></span>

### <span data-ttu-id="a4e5f-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a4e5f-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a4e5f-170">È possibile reindirizzare un oggetto **Recordset** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="a4e5f-171">Si tratta di una rappresentazione offline del **Recordset** e le modifiche apportate non modificano le risposte DNS finché non si esegue il cmdlet Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="a4e5f-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4e5f-172">OUTPUTS</span></span>

### <span data-ttu-id="a4e5f-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a4e5f-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a4e5f-174">Questo cmdlet restituisce l'oggetto **Recordset** modificato.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="a4e5f-175">Inoltre, l'oggetto passato viene modificato direttamente.</span><span class="sxs-lookup"><span data-stu-id="a4e5f-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="a4e5f-176">Note</span><span class="sxs-lookup"><span data-stu-id="a4e5f-176">NOTES</span></span>

## <span data-ttu-id="a4e5f-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4e5f-177">RELATED LINKS</span></span>

[<span data-ttu-id="a4e5f-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a4e5f-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="a4e5f-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a4e5f-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="a4e5f-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a4e5f-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
