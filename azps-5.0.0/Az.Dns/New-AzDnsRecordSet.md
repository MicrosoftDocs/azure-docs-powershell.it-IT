---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200937"
---
# <span data-ttu-id="3aa77-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3aa77-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="3aa77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3aa77-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa77-103">Crea un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="3aa77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3aa77-104">SYNTAX</span></span>

### <span data-ttu-id="3aa77-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3aa77-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa77-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="3aa77-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa77-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="3aa77-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa77-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="3aa77-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aa77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3aa77-109">DESCRIPTION</span></span>
<span data-ttu-id="3aa77-110">Il cmdlet **New-AzDnsRecordSet** crea un nuovo record DNS (Domain Name System) impostato con il nome e il tipo specificati nella zona specificata.</span><span class="sxs-lookup"><span data-stu-id="3aa77-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="3aa77-111">Un oggetto **Recordset** è un set di record DNS con lo stesso nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="3aa77-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="3aa77-112">Tieni presente che il nome è relativo all'area e non il nome completo.</span><span class="sxs-lookup"><span data-stu-id="3aa77-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="3aa77-113">Il parametro *DnsRecords* specifica i record nel set di record.</span><span class="sxs-lookup"><span data-stu-id="3aa77-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="3aa77-114">Questo parametro accetta una matrice di record DNS, costruita con New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="3aa77-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="3aa77-115">Puoi usare l'operatore pipeline per passare un oggetto **dnsZone** a questo cmdlet oppure puoi passare un oggetto **dnsZone** come parametro *zone* oppure puoi specificare la zona per nome.</span><span class="sxs-lookup"><span data-stu-id="3aa77-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="3aa77-116">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3aa77-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3aa77-117">Se un **oggetto recordset** corrispondente esiste già (stesso nome e tipo di record), è necessario specificare il parametro *overwrite* , altrimenti il cmdlet non creerà un nuovo **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="3aa77-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="3aa77-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3aa77-118">EXAMPLES</span></span>

### <span data-ttu-id="3aa77-119">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="3aa77-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="3aa77-120">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-121">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-122">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="3aa77-123">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="3aa77-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-124">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-125">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-126">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-126">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-127">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-128">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="3aa77-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-129">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-130">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-131">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-131">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-132">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-133">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="3aa77-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-134">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-135">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-136">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-136">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-137">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-138">Esempio 5: creare un RecordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="3aa77-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-139">Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-140">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-141">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-141">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-142">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-143">Esempio 6: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="3aa77-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="3aa77-144">Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="3aa77-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="3aa77-145">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-146">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-146">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-147">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-148">Esempio 7: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="3aa77-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-149">Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-150">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-151">Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="3aa77-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="3aa77-152">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="3aa77-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="3aa77-153">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-154">Esempio 8: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="3aa77-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-155">Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-156">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-157">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-157">It contains a single DNS record.</span></span>
<span data-ttu-id="3aa77-158">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-159">Esempio 9: creare un RecordSet nella zona Apex</span><span class="sxs-lookup"><span data-stu-id="3aa77-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-160">Questo comando crea un **Recordset** all'apice (o radice) della zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-161">A tale scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).</span><span class="sxs-lookup"><span data-stu-id="3aa77-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="3aa77-162">Non è possibile creare record CNAME all'apice di una zona.</span><span class="sxs-lookup"><span data-stu-id="3aa77-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="3aa77-163">Questo è un vincolo degli standard DNS; non si tratta di una limitazione di Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="3aa77-164">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-165">Esempio 10: creare un set di record con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="3aa77-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="3aa77-166">Questo comando crea un **Recordset** denominato \* nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-167">Si tratta di un set di record con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="3aa77-167">This is a wildcard record set.</span></span>
<span data-ttu-id="3aa77-168">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="3aa77-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="3aa77-169">Esempio 11: creare un set di record vuoto</span><span class="sxs-lookup"><span data-stu-id="3aa77-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="3aa77-170">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="3aa77-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="3aa77-171">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="3aa77-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="3aa77-172">Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere più tardi i record.</span><span class="sxs-lookup"><span data-stu-id="3aa77-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="3aa77-173">Esempio 12: creare un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="3aa77-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="3aa77-174">Questo comando crea un **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3aa77-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="3aa77-175">Il *parametro overwrite garantisce* che questo set di record sovrascriva qualsiasi set di record preesistente con lo stesso nome e tipo (i record esistenti in tale set di record andranno perduti).</span><span class="sxs-lookup"><span data-stu-id="3aa77-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="3aa77-176">Il parametro *Confirm* con un valore di $false Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="3aa77-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="3aa77-177">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3aa77-177">PARAMETERS</span></span>

### <span data-ttu-id="3aa77-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa77-178">-DefaultProfile</span></span>
<span data-ttu-id="3aa77-179">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3aa77-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aa77-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="3aa77-180">-DnsRecords</span></span>
<span data-ttu-id="3aa77-181">Specifica la matrice di record DNS da includere nel set di record.</span><span class="sxs-lookup"><span data-stu-id="3aa77-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="3aa77-182">Puoi usare il cmdlet New-AzDnsRecordConfig per creare oggetti record DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="3aa77-183">Per altre informazioni, vedere gli esempi.</span><span class="sxs-lookup"><span data-stu-id="3aa77-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3aa77-184">-Metadata</span></span>
<span data-ttu-id="3aa77-185">Specifica una matrice di metadati da associare al RecordSet.</span><span class="sxs-lookup"><span data-stu-id="3aa77-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="3aa77-186">I metadati vengono specificati usando coppie nome/valore rappresentate come tabelle hash, ad esempio @ {"Dept" = "shopping"; " ENV "=" Production "}.</span><span class="sxs-lookup"><span data-stu-id="3aa77-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="3aa77-187">-Name</span></span>
<span data-ttu-id="3aa77-188">Specifica il nome del **Recordset** da creare.</span><span class="sxs-lookup"><span data-stu-id="3aa77-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-189">-Sovrascrivere</span><span class="sxs-lookup"><span data-stu-id="3aa77-189">-Overwrite</span></span>
<span data-ttu-id="3aa77-190">Indica che questo cmdlet sovrascrive il **Recordset** specificato se esiste già.</span><span class="sxs-lookup"><span data-stu-id="3aa77-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="3aa77-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="3aa77-191">-RecordType</span></span>
<span data-ttu-id="3aa77-192">Specifica il tipo di record DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="3aa77-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="3aa77-193">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3aa77-193">Valid values are:</span></span>
- <span data-ttu-id="3aa77-194">Un</span><span class="sxs-lookup"><span data-stu-id="3aa77-194">A</span></span>
- <span data-ttu-id="3aa77-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="3aa77-195">AAAA</span></span>
- <span data-ttu-id="3aa77-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="3aa77-196">CNAME</span></span>
- <span data-ttu-id="3aa77-197">MX</span><span class="sxs-lookup"><span data-stu-id="3aa77-197">MX</span></span>
- <span data-ttu-id="3aa77-198">NS</span><span class="sxs-lookup"><span data-stu-id="3aa77-198">NS</span></span>
- <span data-ttu-id="3aa77-199">PTR</span><span class="sxs-lookup"><span data-stu-id="3aa77-199">PTR</span></span>
- <span data-ttu-id="3aa77-200">SRV</span><span class="sxs-lookup"><span data-stu-id="3aa77-200">SRV</span></span>
- <span data-ttu-id="3aa77-201">I record SOA TXT vengono creati automaticamente quando la zona viene creata e non può essere creata manualmente.</span><span class="sxs-lookup"><span data-stu-id="3aa77-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa77-202">-ResourceGroupName</span></span>
<span data-ttu-id="3aa77-203">Specifica il gruppo di risorse che contiene la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="3aa77-204">Devi anche specificare il parametro *zonename* per specificare il nome della zona.</span><span class="sxs-lookup"><span data-stu-id="3aa77-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="3aa77-205">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="3aa77-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa77-206">-TargetResourceId</span></span>
<span data-ttu-id="3aa77-207">ID risorsa di destinazione alias.</span><span class="sxs-lookup"><span data-stu-id="3aa77-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="3aa77-208">-Ttl</span></span>
<span data-ttu-id="3aa77-209">Specifica il TTL (time to Live) per il RecordSet DNS.</span><span class="sxs-lookup"><span data-stu-id="3aa77-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-210">-Zona</span><span class="sxs-lookup"><span data-stu-id="3aa77-210">-Zone</span></span>
<span data-ttu-id="3aa77-211">Specifica il DnsZone in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3aa77-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="3aa77-212">In alternativa, puoi specificare la zona usando i parametri *zonename* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3aa77-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-213">-Zonename</span><span class="sxs-lookup"><span data-stu-id="3aa77-213">-ZoneName</span></span>
<span data-ttu-id="3aa77-214">Specifica il nome dell'area in cui creare il **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3aa77-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="3aa77-215">Devi anche specificare il gruppo di risorse che contiene la zona usando il parametro *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3aa77-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="3aa77-216">In alternativa, puoi specificare il gruppo zona e risorse passando un oggetto zona DNS usando il parametro *zone* .</span><span class="sxs-lookup"><span data-stu-id="3aa77-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aa77-217">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3aa77-217">-Confirm</span></span>
<span data-ttu-id="3aa77-218">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3aa77-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa77-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa77-219">-WhatIf</span></span>
<span data-ttu-id="3aa77-220">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aa77-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa77-221">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3aa77-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa77-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa77-222">CommonParameters</span></span>
<span data-ttu-id="3aa77-223">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa77-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa77-224">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa77-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa77-225">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3aa77-225">INPUTS</span></span>

### <span data-ttu-id="3aa77-226">System. String</span><span class="sxs-lookup"><span data-stu-id="3aa77-226">System.String</span></span>

### <span data-ttu-id="3aa77-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="3aa77-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="3aa77-228">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="3aa77-228">System.UInt32</span></span>

### <span data-ttu-id="3aa77-229">Microsoft. Azure. Management. DNS. Models. RecordType</span><span class="sxs-lookup"><span data-stu-id="3aa77-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="3aa77-230">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3aa77-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3aa77-231">Microsoft. Azure. Commands. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="3aa77-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="3aa77-232">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3aa77-232">OUTPUTS</span></span>

### <span data-ttu-id="3aa77-233">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3aa77-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="3aa77-234">Note</span><span class="sxs-lookup"><span data-stu-id="3aa77-234">NOTES</span></span>
<span data-ttu-id="3aa77-235">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="3aa77-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3aa77-236">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="3aa77-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="3aa77-237">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3aa77-237">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3aa77-238">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3aa77-238">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3aa77-239">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3aa77-239">RELATED LINKS</span></span>

[<span data-ttu-id="3aa77-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3aa77-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="3aa77-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3aa77-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="3aa77-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3aa77-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="3aa77-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3aa77-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="3aa77-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3aa77-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
