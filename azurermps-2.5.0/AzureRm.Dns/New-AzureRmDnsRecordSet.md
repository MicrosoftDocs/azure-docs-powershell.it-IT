---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866111"
---
# <span data-ttu-id="db2a0-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db2a0-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="db2a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="db2a0-103">Crea un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db2a0-104">SYNTAX</span></span>

### <span data-ttu-id="db2a0-105">Campi</span><span class="sxs-lookup"><span data-stu-id="db2a0-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2a0-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="db2a0-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db2a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db2a0-107">DESCRIPTION</span></span>
<span data-ttu-id="db2a0-108">Il cmdlet **New-AzureRmDnsRecordSet** crea un nuovo record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="db2a0-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="db2a0-109">Un oggetto **Recordset** è un set di record DNS con lo stesso nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="db2a0-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="db2a0-110">Tieni presente che il nome è relativo all'area e non il nome completo.</span><span class="sxs-lookup"><span data-stu-id="db2a0-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="db2a0-111">Il parametro *DnsRecords* specifica i record nel set di record.</span><span class="sxs-lookup"><span data-stu-id="db2a0-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="db2a0-112">Questo parametro accetta una matrice di record DNS, costruita con New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="db2a0-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="db2a0-113">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro *zone* oppure puoi specificare la zona per nome.</span><span class="sxs-lookup"><span data-stu-id="db2a0-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="db2a0-114">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="db2a0-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="db2a0-115">Se un **oggetto recordset** corrispondente esiste già (stesso nome e tipo di record), è necessario specificare il parametro *overwrite* , altrimenti il cmdlet non creerà un nuovo **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="db2a0-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="db2a0-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db2a0-116">EXAMPLES</span></span>

### <span data-ttu-id="db2a0-117">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="db2a0-117">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-118">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-119">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-120">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="db2a0-121">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="db2a0-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-122">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-123">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-124">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-124">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-125">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-126">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="db2a0-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-127">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-128">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-129">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-129">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-130">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-131">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="db2a0-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-132">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-133">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-134">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-134">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-135">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-136">Esempio 5: creare un RecordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="db2a0-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-137">Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-138">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-139">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-139">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-140">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-141">Esempio 6: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="db2a0-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="db2a0-142">Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="db2a0-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="db2a0-143">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-144">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-144">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-145">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-146">Esempio 7: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="db2a0-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-147">Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-148">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-149">Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="db2a0-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="db2a0-150">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="db2a0-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="db2a0-151">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-152">Esempio 8: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="db2a0-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-153">Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-154">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-155">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-155">It contains a single DNS record.</span></span>

<span data-ttu-id="db2a0-156">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-157">Esempio 9: creare un RecordSet nella zona Apex</span><span class="sxs-lookup"><span data-stu-id="db2a0-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-158">Questo comando crea un **Recordset** all'apice (o radice) della zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-159">A tale scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).</span><span class="sxs-lookup"><span data-stu-id="db2a0-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="db2a0-160">Non è possibile creare record CNAME all'apice di una zona.</span><span class="sxs-lookup"><span data-stu-id="db2a0-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="db2a0-161">Questo è un vincolo degli standard DNS; non si tratta di una limitazione di Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="db2a0-162">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-163">Esempio 10: creare un set di record con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="db2a0-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="db2a0-164">Questo comando crea un **Recordset** denominato \* nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-165">Si tratta di un set di record con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="db2a0-165">This is a wildcard record set.</span></span>

<span data-ttu-id="db2a0-166">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="db2a0-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="db2a0-167">Esempio 11: creare un set di record vuoto</span><span class="sxs-lookup"><span data-stu-id="db2a0-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="db2a0-168">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="db2a0-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="db2a0-169">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="db2a0-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="db2a0-170">Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere più tardi i record.</span><span class="sxs-lookup"><span data-stu-id="db2a0-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="db2a0-171">Esempio 12: creare un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="db2a0-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="db2a0-172">Questo comando crea un **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="db2a0-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="db2a0-173">Il *parametro overwrite garantisce* che questo set di record sovrascriva qualsiasi set di record preesistente con lo stesso nome e tipo (i record esistenti in tale set di record andranno perduti).</span><span class="sxs-lookup"><span data-stu-id="db2a0-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="db2a0-174">Il parametro *Confirm* con un valore di $false Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="db2a0-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="db2a0-175">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db2a0-175">PARAMETERS</span></span>

### <span data-ttu-id="db2a0-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="db2a0-176">-DnsRecords</span></span>
<span data-ttu-id="db2a0-177">Specifica la matrice di record DNS da includere nel set di record.</span><span class="sxs-lookup"><span data-stu-id="db2a0-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="db2a0-178">Puoi usare il cmdlet New-AzureRmDnsRecordConfig per creare oggetti record DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-178">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="db2a0-179">Per altre informazioni, vedere gli esempi.</span><span class="sxs-lookup"><span data-stu-id="db2a0-179">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db2a0-180">-Force</span><span class="sxs-lookup"><span data-stu-id="db2a0-180">-Force</span></span>
<span data-ttu-id="db2a0-181">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2a0-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="db2a0-182">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="db2a0-182">It will be removed in a future release.</span></span>

<span data-ttu-id="db2a0-183">Per controllare se questo cmdlet richiede la confirmazione, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="db2a0-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="db2a0-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="db2a0-184">-Metadata</span></span>
<span data-ttu-id="db2a0-185">Specifica una matrice di metadati da associare al RecordSet.</span><span class="sxs-lookup"><span data-stu-id="db2a0-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="db2a0-186">I metadati vengono specificati usando coppie nome/valore rappresentate come tabelle hash, ad esempio @ (@ {"Name" = "Dept"; "Value" = "shopping"}, @ {"Name" = "ENV"; "Value" = "Production"}).</span><span class="sxs-lookup"><span data-stu-id="db2a0-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2a0-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="db2a0-187">-Name</span></span>
<span data-ttu-id="db2a0-188">Specifica il nome del **Recordset** da creare.</span><span class="sxs-lookup"><span data-stu-id="db2a0-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2a0-189">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="db2a0-189">-Overwrite</span></span>
<span data-ttu-id="db2a0-190">Indica che questo cmdlet sovrascrive il **Recordset** specificato se esiste già.</span><span class="sxs-lookup"><span data-stu-id="db2a0-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="db2a0-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="db2a0-191">-RecordType</span></span>
<span data-ttu-id="db2a0-192">Specifica il tipo di record DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="db2a0-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="db2a0-193">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="db2a0-193">Valid values are:</span></span>

- <span data-ttu-id="db2a0-194">Un</span><span class="sxs-lookup"><span data-stu-id="db2a0-194">A</span></span>
- <span data-ttu-id="db2a0-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="db2a0-195">AAAA</span></span>
- <span data-ttu-id="db2a0-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="db2a0-196">CNAME</span></span>
- <span data-ttu-id="db2a0-197">MX</span><span class="sxs-lookup"><span data-stu-id="db2a0-197">MX</span></span>
- <span data-ttu-id="db2a0-198">NS</span><span class="sxs-lookup"><span data-stu-id="db2a0-198">NS</span></span>
- <span data-ttu-id="db2a0-199">PTR</span><span class="sxs-lookup"><span data-stu-id="db2a0-199">PTR</span></span>
- <span data-ttu-id="db2a0-200">SRV</span><span class="sxs-lookup"><span data-stu-id="db2a0-200">SRV</span></span>
- <span data-ttu-id="db2a0-201">TXT</span><span class="sxs-lookup"><span data-stu-id="db2a0-201">TXT</span></span>

<span data-ttu-id="db2a0-202">I record SOA vengono creati automaticamente quando la zona viene creata e non può essere creata manualmente.</span><span class="sxs-lookup"><span data-stu-id="db2a0-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2a0-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2a0-203">-ResourceGroupName</span></span>
<span data-ttu-id="db2a0-204">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="db2a0-205">Devi anche specificare il parametro *zonename* per specificare il nome della zona.</span><span class="sxs-lookup"><span data-stu-id="db2a0-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="db2a0-206">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="db2a0-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="db2a0-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="db2a0-207">-Ttl</span></span>
<span data-ttu-id="db2a0-208">Specifica il TTL (time to Live) per il RecordSet DNS.</span><span class="sxs-lookup"><span data-stu-id="db2a0-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2a0-209">-Zona</span><span class="sxs-lookup"><span data-stu-id="db2a0-209">-Zone</span></span>
<span data-ttu-id="db2a0-210">Specifica il DnsZone in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="db2a0-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="db2a0-211">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="db2a0-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="db2a0-212">-Zonename</span><span class="sxs-lookup"><span data-stu-id="db2a0-212">-ZoneName</span></span>
<span data-ttu-id="db2a0-213">Specifica il nome dell'area in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="db2a0-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="db2a0-214">Devi anche specificare il gruppo di risorse che contiene la zona usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="db2a0-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="db2a0-215">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="db2a0-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="db2a0-216">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db2a0-216">-Confirm</span></span>
<span data-ttu-id="db2a0-217">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2a0-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2a0-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2a0-218">-WhatIf</span></span>
<span data-ttu-id="db2a0-219">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db2a0-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2a0-220">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db2a0-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2a0-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2a0-221">CommonParameters</span></span>
<span data-ttu-id="db2a0-222">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2a0-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2a0-223">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2a0-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2a0-224">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db2a0-224">INPUTS</span></span>

### <span data-ttu-id="db2a0-225">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="db2a0-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="db2a0-226">Puoi reindirizzare un oggetto DnsZone a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2a0-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="db2a0-227">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db2a0-227">OUTPUTS</span></span>

### <span data-ttu-id="db2a0-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db2a0-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="db2a0-229">Questo cmdlet restituisce un oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="db2a0-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="db2a0-230">Note</span><span class="sxs-lookup"><span data-stu-id="db2a0-230">NOTES</span></span>
<span data-ttu-id="db2a0-231">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="db2a0-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="db2a0-232">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="db2a0-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="db2a0-233">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="db2a0-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="db2a0-234">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="db2a0-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="db2a0-235">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db2a0-235">RELATED LINKS</span></span>

[<span data-ttu-id="db2a0-236">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="db2a0-236">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="db2a0-237">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db2a0-237">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="db2a0-238">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="db2a0-238">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="db2a0-239">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db2a0-239">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="db2a0-240">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="db2a0-240">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
