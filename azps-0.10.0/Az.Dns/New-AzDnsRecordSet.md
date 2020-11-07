---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 0327837f6e28d7147892669bd77b1aa78747a5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863161"
---
# <span data-ttu-id="d254b-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d254b-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="d254b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d254b-102">SYNOPSIS</span></span>
<span data-ttu-id="d254b-103">Crea un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="d254b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d254b-104">SYNTAX</span></span>

### <span data-ttu-id="d254b-105">Campi</span><span class="sxs-lookup"><span data-stu-id="d254b-105">Fields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d254b-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="d254b-106">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d254b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d254b-107">DESCRIPTION</span></span>
<span data-ttu-id="d254b-108">Il cmdlet **New-AzDnsRecordSet** crea un nuovo record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="d254b-108">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="d254b-109">Un oggetto **Recordset** è un set di record DNS con lo stesso nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="d254b-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="d254b-110">Tieni presente che il nome è relativo all'area e non il nome completo.</span><span class="sxs-lookup"><span data-stu-id="d254b-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="d254b-111">Il parametro *DnsRecords* specifica i record nel set di record.</span><span class="sxs-lookup"><span data-stu-id="d254b-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="d254b-112">Questo parametro accetta una matrice di record DNS, costruita con New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="d254b-112">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>

<span data-ttu-id="d254b-113">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro *zone* oppure puoi specificare la zona per nome.</span><span class="sxs-lookup"><span data-stu-id="d254b-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="d254b-114">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="d254b-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="d254b-115">Se un **oggetto recordset** corrispondente esiste già (stesso nome e tipo di record), è necessario specificare il parametro *overwrite* , altrimenti il cmdlet non creerà un nuovo **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d254b-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="d254b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d254b-116">EXAMPLES</span></span>

### <span data-ttu-id="d254b-117">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="d254b-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="d254b-118">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-119">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-120">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="d254b-121">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="d254b-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-122">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-123">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-124">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-124">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-125">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-126">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="d254b-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-127">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-128">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-129">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-129">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-130">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-131">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="d254b-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-132">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-133">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-134">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-134">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-135">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-136">Esempio 5: creare un RecordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="d254b-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-137">Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-138">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-139">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-139">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-140">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-141">Esempio 6: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="d254b-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="d254b-142">Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="d254b-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="d254b-143">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-144">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-144">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-145">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-146">Esempio 7: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="d254b-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-147">Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-148">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-149">Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="d254b-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="d254b-150">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="d254b-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="d254b-151">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-152">Esempio 8: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="d254b-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-153">Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-154">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-155">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-155">It contains a single DNS record.</span></span>

<span data-ttu-id="d254b-156">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-157">Esempio 9: creare un RecordSet nella zona Apex</span><span class="sxs-lookup"><span data-stu-id="d254b-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-158">Questo comando crea un **Recordset** all'apice (o radice) della zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="d254b-159">A tale scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).</span><span class="sxs-lookup"><span data-stu-id="d254b-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="d254b-160">Non è possibile creare record CNAME all'apice di una zona.</span><span class="sxs-lookup"><span data-stu-id="d254b-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="d254b-161">Questo è un vincolo degli standard DNS; non si tratta di una limitazione di Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="d254b-162">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-163">Esempio 10: creare un set di record con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="d254b-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d254b-164">Questo comando crea un **Recordset** denominato \* nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-165">Si tratta di un set di record con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="d254b-165">This is a wildcard record set.</span></span>

<span data-ttu-id="d254b-166">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d254b-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d254b-167">Esempio 11: creare un set di record vuoto</span><span class="sxs-lookup"><span data-stu-id="d254b-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="d254b-168">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="d254b-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d254b-169">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d254b-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d254b-170">Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere più tardi i record.</span><span class="sxs-lookup"><span data-stu-id="d254b-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="d254b-171">Esempio 12: creare un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="d254b-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="d254b-172">Questo comando crea un **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d254b-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="d254b-173">Il *parametro overwrite garantisce* che questo set di record sovrascriva qualsiasi set di record preesistente con lo stesso nome e tipo (i record esistenti in tale set di record andranno perduti).</span><span class="sxs-lookup"><span data-stu-id="d254b-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="d254b-174">Il parametro *Confirm* con un valore di $false Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="d254b-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="d254b-175">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d254b-175">PARAMETERS</span></span>

### <span data-ttu-id="d254b-176">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="d254b-176">-DnsRecords</span></span>
<span data-ttu-id="d254b-177">Specifica la matrice di record DNS da includere nel set di record.</span><span class="sxs-lookup"><span data-stu-id="d254b-177">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="d254b-178">Puoi usare il cmdlet New-AzDnsRecordConfig per creare oggetti record DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-178">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="d254b-179">Per altre informazioni, vedere gli esempi.</span><span class="sxs-lookup"><span data-stu-id="d254b-179">See the examples for more information.</span></span>

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

### <span data-ttu-id="d254b-180">-Force</span><span class="sxs-lookup"><span data-stu-id="d254b-180">-Force</span></span>
<span data-ttu-id="d254b-181">Questo parametro è deprecato per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d254b-181">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="d254b-182">Verrà rimosso in una versione futura.</span><span class="sxs-lookup"><span data-stu-id="d254b-182">It will be removed in a future release.</span></span>

<span data-ttu-id="d254b-183">Per controllare se questo cmdlet richiede la confirmazione, usare il parametro *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="d254b-183">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="d254b-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d254b-184">-Metadata</span></span>
<span data-ttu-id="d254b-185">Specifica una matrice di metadati da associare al RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d254b-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="d254b-186">I metadati vengono specificati usando coppie nome/valore rappresentate come tabelle hash, ad esempio @ (@ {"Name" = "Dept"; "Value" = "shopping"}, @ {"Name" = "ENV"; "Value" = "Production"}).</span><span class="sxs-lookup"><span data-stu-id="d254b-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="d254b-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="d254b-187">-Name</span></span>
<span data-ttu-id="d254b-188">Specifica il nome del **Recordset** da creare.</span><span class="sxs-lookup"><span data-stu-id="d254b-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="d254b-189">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="d254b-189">-Overwrite</span></span>
<span data-ttu-id="d254b-190">Indica che questo cmdlet sovrascrive il **Recordset** specificato se esiste già.</span><span class="sxs-lookup"><span data-stu-id="d254b-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="d254b-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="d254b-191">-RecordType</span></span>
<span data-ttu-id="d254b-192">Specifica il tipo di record DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="d254b-192">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="d254b-193">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="d254b-193">Valid values are:</span></span>

- <span data-ttu-id="d254b-194">Un</span><span class="sxs-lookup"><span data-stu-id="d254b-194">A</span></span>
- <span data-ttu-id="d254b-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="d254b-195">AAAA</span></span>
- <span data-ttu-id="d254b-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="d254b-196">CNAME</span></span>
- <span data-ttu-id="d254b-197">MX</span><span class="sxs-lookup"><span data-stu-id="d254b-197">MX</span></span>
- <span data-ttu-id="d254b-198">NS</span><span class="sxs-lookup"><span data-stu-id="d254b-198">NS</span></span>
- <span data-ttu-id="d254b-199">PTR</span><span class="sxs-lookup"><span data-stu-id="d254b-199">PTR</span></span>
- <span data-ttu-id="d254b-200">SRV</span><span class="sxs-lookup"><span data-stu-id="d254b-200">SRV</span></span>
- <span data-ttu-id="d254b-201">TXT</span><span class="sxs-lookup"><span data-stu-id="d254b-201">TXT</span></span>

<span data-ttu-id="d254b-202">I record SOA vengono creati automaticamente quando la zona viene creata e non può essere creata manualmente.</span><span class="sxs-lookup"><span data-stu-id="d254b-202">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="d254b-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d254b-203">-ResourceGroupName</span></span>
<span data-ttu-id="d254b-204">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-204">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="d254b-205">Devi anche specificare il parametro *zonename* per specificare il nome della zona.</span><span class="sxs-lookup"><span data-stu-id="d254b-205">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="d254b-206">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="d254b-206">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d254b-207">-TTL</span><span class="sxs-lookup"><span data-stu-id="d254b-207">-Ttl</span></span>
<span data-ttu-id="d254b-208">Specifica il TTL (time to Live) per il RecordSet DNS.</span><span class="sxs-lookup"><span data-stu-id="d254b-208">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="d254b-209">-Zona</span><span class="sxs-lookup"><span data-stu-id="d254b-209">-Zone</span></span>
<span data-ttu-id="d254b-210">Specifica il DnsZone in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d254b-210">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="d254b-211">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d254b-211">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="d254b-212">-Zonename</span><span class="sxs-lookup"><span data-stu-id="d254b-212">-ZoneName</span></span>
<span data-ttu-id="d254b-213">Specifica il nome dell'area in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d254b-213">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="d254b-214">Devi anche specificare il gruppo di risorse che contiene la zona usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d254b-214">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="d254b-215">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="d254b-215">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d254b-216">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d254b-216">-Confirm</span></span>
<span data-ttu-id="d254b-217">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d254b-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d254b-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d254b-218">-WhatIf</span></span>
<span data-ttu-id="d254b-219">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d254b-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d254b-220">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d254b-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d254b-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d254b-221">CommonParameters</span></span>
<span data-ttu-id="d254b-222">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d254b-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d254b-223">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d254b-223">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d254b-224">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d254b-224">INPUTS</span></span>

### <span data-ttu-id="d254b-225">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="d254b-225">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d254b-226">Puoi reindirizzare un oggetto DnsZone a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d254b-226">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="d254b-227">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d254b-227">OUTPUTS</span></span>

### <span data-ttu-id="d254b-228">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d254b-228">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d254b-229">Questo cmdlet restituisce un oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d254b-229">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="d254b-230">Note</span><span class="sxs-lookup"><span data-stu-id="d254b-230">NOTES</span></span>
<span data-ttu-id="d254b-231">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="d254b-231">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d254b-232">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="d254b-232">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="d254b-233">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d254b-233">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="d254b-234">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="d254b-234">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d254b-235">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d254b-235">RELATED LINKS</span></span>

[<span data-ttu-id="d254b-236">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d254b-236">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="d254b-237">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d254b-237">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="d254b-238">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d254b-238">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="d254b-239">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d254b-239">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="d254b-240">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d254b-240">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
