---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863162"
---
# <span data-ttu-id="bac46-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bac46-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="bac46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bac46-102">SYNOPSIS</span></span>
<span data-ttu-id="bac46-103">Rimuove un record DNS da un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="bac46-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="bac46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bac46-104">SYNTAX</span></span>

### <span data-ttu-id="bac46-105">Un</span><span class="sxs-lookup"><span data-stu-id="bac46-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="bac46-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="bac46-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="bac46-107">NS</span><span class="sxs-lookup"><span data-stu-id="bac46-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="bac46-108">MX</span><span class="sxs-lookup"><span data-stu-id="bac46-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="bac46-109">PTR</span><span class="sxs-lookup"><span data-stu-id="bac46-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="bac46-110">TXT</span><span class="sxs-lookup"><span data-stu-id="bac46-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="bac46-111">SRV</span><span class="sxs-lookup"><span data-stu-id="bac46-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="bac46-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="bac46-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="bac46-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bac46-113">DESCRIPTION</span></span>
<span data-ttu-id="bac46-114">Il cmdlet **Remove-AzDnsRecordConfig** rimuove un record DNS (Domain Name System) da un set di record.</span><span class="sxs-lookup"><span data-stu-id="bac46-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="bac46-115">L'oggetto **Recordset** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non viene eseguito il cmdlet Set-AzDnsRecordSet per rendere persistente la modifica al servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bac46-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="bac46-116">Per rimuovere un record, tutti i campi per il tipo di record devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="bac46-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="bac46-117">Non è possibile aggiungere o rimuovere record SOA.</span><span class="sxs-lookup"><span data-stu-id="bac46-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="bac46-118">I record SOA vengono creati automaticamente quando viene creata e eliminata automaticamente una zona DNS quando la zona DNS viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="bac46-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="bac46-119">Puoi passare l'oggetto **Recordset** a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="bac46-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="bac46-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bac46-120">EXAMPLES</span></span>

### <span data-ttu-id="bac46-121">Esempio 1: rimuovere un record da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-122">Questo esempio rimuove un record A da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="bac46-123">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="bac46-124">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-125">Esempio 2: rimuovere un record AAAA da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-126">In questo esempio viene rimosso un record AAAA da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="bac46-127">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="bac46-128">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-129">Esempio 3: rimuovere un record CNAME da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-130">In questo esempio viene rimosso un record CNAME da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="bac46-131">Dato che un set di record CNAME può contenere al massimo un record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="bac46-132">Esempio 4: rimuovere un record MX da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-133">In questo esempio viene rimosso un record MX da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="bac46-134">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="bac46-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="bac46-135">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="bac46-136">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-137">Esempio 5: rimuovere un record NS da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-138">In questo esempio viene rimosso un record NS da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="bac46-139">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="bac46-140">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-141">Esempio 6: rimuovere un record PTR da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-142">In questo esempio viene rimosso un record PTR da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="bac46-143">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="bac46-144">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-145">Esempio 7: rimuovere un record SRV da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-146">In questo esempio viene rimosso un record SRV da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="bac46-147">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="bac46-148">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="bac46-149">Esempio 8: rimuovere un record TXT da un set di record</span><span class="sxs-lookup"><span data-stu-id="bac46-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="bac46-150">In questo esempio viene rimosso un record TXT da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="bac46-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="bac46-151">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="bac46-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="bac46-152">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="bac46-153">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bac46-153">PARAMETERS</span></span>

### <span data-ttu-id="bac46-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="bac46-154">-Cname</span></span>
<span data-ttu-id="bac46-155">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="bac46-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="bac46-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="bac46-156">-Exchange</span></span>
<span data-ttu-id="bac46-157">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="bac46-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="bac46-158">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="bac46-158">-Ipv4Address</span></span>
<span data-ttu-id="bac46-159">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="bac46-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="bac46-160">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="bac46-160">-Ipv6Address</span></span>
<span data-ttu-id="bac46-161">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="bac46-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="bac46-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="bac46-162">-Nsdname</span></span>
<span data-ttu-id="bac46-163">Specifica il server dei nomi per un record del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="bac46-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="bac46-164">-Porta</span><span class="sxs-lookup"><span data-stu-id="bac46-164">-Port</span></span>
<span data-ttu-id="bac46-165">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="bac46-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="bac46-166">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="bac46-166">-Preference</span></span>
<span data-ttu-id="bac46-167">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="bac46-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="bac46-168">-Priorità</span><span class="sxs-lookup"><span data-stu-id="bac46-168">-Priority</span></span>
<span data-ttu-id="bac46-169">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="bac46-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="bac46-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="bac46-170">-Ptrdname</span></span>
<span data-ttu-id="bac46-171">Specifica il nome di dominio di destinazione di un record puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="bac46-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="bac46-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="bac46-172">-RecordSet</span></span>
<span data-ttu-id="bac46-173">Specifica l'oggetto **Recordset** che contiene il record da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bac46-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="bac46-174">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="bac46-174">-Target</span></span>
<span data-ttu-id="bac46-175">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="bac46-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="bac46-176">-Valore</span><span class="sxs-lookup"><span data-stu-id="bac46-176">-Value</span></span>
<span data-ttu-id="bac46-177">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="bac46-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="bac46-178">-Peso</span><span class="sxs-lookup"><span data-stu-id="bac46-178">-Weight</span></span>
<span data-ttu-id="bac46-179">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="bac46-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="bac46-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac46-180">CommonParameters</span></span>
<span data-ttu-id="bac46-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bac46-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac46-182">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac46-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac46-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bac46-183">INPUTS</span></span>

### <span data-ttu-id="bac46-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bac46-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="bac46-185">Puoi reindirizzare un oggetto **DnsRecordSet** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bac46-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="bac46-186">Si tratta di una rappresentazione offline del set di record e gli aggiornamenti non cambiano le risposte DNS fino a quando non si esegue set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="bac46-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="bac46-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bac46-187">OUTPUTS</span></span>

### <span data-ttu-id="bac46-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bac46-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="bac46-189">Questo cmdlet restituisce l'oggetto **Recordset** modificato.</span><span class="sxs-lookup"><span data-stu-id="bac46-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="bac46-190">Note</span><span class="sxs-lookup"><span data-stu-id="bac46-190">NOTES</span></span>

## <span data-ttu-id="bac46-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bac46-191">RELATED LINKS</span></span>

[<span data-ttu-id="bac46-192">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bac46-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="bac46-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bac46-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="bac46-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bac46-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
