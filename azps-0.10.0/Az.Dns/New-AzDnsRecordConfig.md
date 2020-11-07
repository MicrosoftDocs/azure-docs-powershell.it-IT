---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: 0bc25aecae445ba18634df578de590f514640c07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863165"
---
# <span data-ttu-id="f2496-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f2496-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="f2496-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2496-102">SYNOPSIS</span></span>
<span data-ttu-id="f2496-103">Crea un nuovo oggetto local record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="f2496-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2496-104">SYNTAX</span></span>

### <span data-ttu-id="f2496-105">Un</span><span class="sxs-lookup"><span data-stu-id="f2496-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="f2496-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="f2496-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="f2496-107">NS</span><span class="sxs-lookup"><span data-stu-id="f2496-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="f2496-108">MX</span><span class="sxs-lookup"><span data-stu-id="f2496-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="f2496-109">PTR</span><span class="sxs-lookup"><span data-stu-id="f2496-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="f2496-110">Txt</span><span class="sxs-lookup"><span data-stu-id="f2496-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="f2496-111">SRV</span><span class="sxs-lookup"><span data-stu-id="f2496-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="f2496-112">CName</span><span class="sxs-lookup"><span data-stu-id="f2496-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="f2496-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2496-113">DESCRIPTION</span></span>
<span data-ttu-id="f2496-114">Il cmdlet **New-AzDnsRecordConfig** crea un oggetto **DnsRecord** locale.</span><span class="sxs-lookup"><span data-stu-id="f2496-114">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="f2496-115">Una matrice di questi oggetti viene passata al cmdlet New-AzDnsRecordSet usando il parametro *DnsRecords* per specificare i record da creare nel set di record.</span><span class="sxs-lookup"><span data-stu-id="f2496-115">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="f2496-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2496-116">EXAMPLES</span></span>

### <span data-ttu-id="f2496-117">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="f2496-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-118">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-119">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-120">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="f2496-121">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="f2496-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-122">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-123">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-124">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-124">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-125">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-126">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="f2496-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-127">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-128">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-129">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-129">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-130">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-131">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="f2496-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-132">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-133">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-134">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-134">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-135">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-136">Esempio 5: creare un RecordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="f2496-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-137">Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-138">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-139">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-139">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-140">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-141">Esempio 6: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="f2496-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="f2496-142">Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="f2496-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="f2496-143">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-144">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-144">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-145">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-146">Esempio 7: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="f2496-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-147">Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-148">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-149">Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="f2496-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="f2496-150">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="f2496-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="f2496-151">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="f2496-152">Esempio 8: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="f2496-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="f2496-153">Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="f2496-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="f2496-154">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="f2496-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="f2496-155">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="f2496-155">It contains a single DNS record.</span></span>

<span data-ttu-id="f2496-156">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="f2496-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="f2496-157">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2496-157">PARAMETERS</span></span>

### <span data-ttu-id="f2496-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f2496-158">-Cname</span></span>
<span data-ttu-id="f2496-159">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="f2496-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f2496-160">-Exchange</span></span>
<span data-ttu-id="f2496-161">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="f2496-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-162">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="f2496-162">-Ipv4Address</span></span>
<span data-ttu-id="f2496-163">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="f2496-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="f2496-164">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="f2496-164">-Ipv6Address</span></span>
<span data-ttu-id="f2496-165">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="f2496-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="f2496-166">-Nsdname</span></span>
<span data-ttu-id="f2496-167">Specifica il nome del server dei nomi per un record NS (Name Server).</span><span class="sxs-lookup"><span data-stu-id="f2496-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-168">-Porta</span><span class="sxs-lookup"><span data-stu-id="f2496-168">-Port</span></span>
<span data-ttu-id="f2496-169">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="f2496-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-170">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="f2496-170">-Preference</span></span>
<span data-ttu-id="f2496-171">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="f2496-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-172">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f2496-172">-Priority</span></span>
<span data-ttu-id="f2496-173">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f2496-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f2496-174">-Ptrdname</span></span>
<span data-ttu-id="f2496-175">Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="f2496-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-176">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="f2496-176">-Target</span></span>
<span data-ttu-id="f2496-177">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f2496-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-178">-Valore</span><span class="sxs-lookup"><span data-stu-id="f2496-178">-Value</span></span>
<span data-ttu-id="f2496-179">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="f2496-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-180">-Peso</span><span class="sxs-lookup"><span data-stu-id="f2496-180">-Weight</span></span>
<span data-ttu-id="f2496-181">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f2496-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2496-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2496-182">CommonParameters</span></span>
<span data-ttu-id="f2496-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2496-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2496-184">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2496-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2496-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2496-185">INPUTS</span></span>

### <span data-ttu-id="f2496-186">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f2496-186">None.</span></span>

## <span data-ttu-id="f2496-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2496-187">OUTPUTS</span></span>

### <span data-ttu-id="f2496-188">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="f2496-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="f2496-189">Note</span><span class="sxs-lookup"><span data-stu-id="f2496-189">NOTES</span></span>

## <span data-ttu-id="f2496-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2496-190">RELATED LINKS</span></span>

[<span data-ttu-id="f2496-191">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f2496-191">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="f2496-192">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f2496-192">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f2496-193">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f2496-193">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
