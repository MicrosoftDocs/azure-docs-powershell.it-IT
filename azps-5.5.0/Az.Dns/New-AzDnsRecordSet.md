---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209618"
---
# <span data-ttu-id="ea125-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea125-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="ea125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea125-102">SYNOPSIS</span></span>
<span data-ttu-id="ea125-103">Crea un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="ea125-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea125-104">SYNTAX</span></span>

### <span data-ttu-id="ea125-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea125-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea125-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="ea125-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea125-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ea125-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea125-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="ea125-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea125-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea125-109">DESCRIPTION</span></span>
<span data-ttu-id="ea125-110">Il cmdlet **New-AzDnsRecordSet** crea un nuovo record DNS (Domain Name System) con il nome specificato e digita nell'area specificata.</span><span class="sxs-lookup"><span data-stu-id="ea125-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="ea125-111">Un **oggetto RecordSet** è un set di record DNS con lo stesso nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="ea125-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="ea125-112">Si noti che il nome è relativo all'area e non al nome completo.</span><span class="sxs-lookup"><span data-stu-id="ea125-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="ea125-113">Il *parametro DnsRecords* specifica i record nel set di record.</span><span class="sxs-lookup"><span data-stu-id="ea125-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="ea125-114">Questo parametro accetta una matrice di record DNS, costruita con New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="ea125-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="ea125-115">È possibile usare l'operatore della pipeline per passare un oggetto **DnsZone** a questo cmdlet oppure passare un oggetto **DnsZone** come parametro *Zone* oppure, in alternativa, è possibile specificare l'area in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ea125-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="ea125-116">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ea125-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ea125-117">Se esiste già **un RecordSet** corrispondente (stesso nome e tipo di record), è necessario specificare il parametro *Overwrite,* altrimenti il cmdlet non creerà un nuovo **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="ea125-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="ea125-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea125-118">EXAMPLES</span></span>

### <span data-ttu-id="ea125-119">Esempio 1: Creare un recordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="ea125-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="ea125-120">In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-121">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-122">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="ea125-123">Esempio 2: Creare un recordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="ea125-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-124">In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-125">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-126">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-126">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-127">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-128">Esempio 3: Creare un recordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="ea125-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-129">In questo esempio viene **creato un recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-130">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-131">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-131">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-132">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-133">Esempio 4: Creare un recordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="ea125-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-134">Questo comando crea un **recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-135">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-136">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-136">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-137">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-138">Esempio 5: Creare un recordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="ea125-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-139">Questo comando crea un **recordSet** denominato ns1 nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-140">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-141">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-141">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-142">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-143">Esempio 6: Creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="ea125-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="ea125-144">Questo comando crea un **recordSet** denominato 4 nell'3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="ea125-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="ea125-145">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-146">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-146">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-147">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-148">Esempio 7: Creare un recordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="ea125-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-149">Questo comando crea un **recordSet** denominato _sip._tcp nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-150">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-151">Contiene un singolo record DNS che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="ea125-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="ea125-152">Il servizio (sip) e il protocollo (tcp) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="ea125-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="ea125-153">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-154">Esempio 8: Creare un recordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="ea125-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-155">Questo comando crea un **recordSet denominato** testo nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-156">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-157">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-157">It contains a single DNS record.</span></span>
<span data-ttu-id="ea125-158">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-159">Esempio 9: Creare un recordSet nell'apice zone</span><span class="sxs-lookup"><span data-stu-id="ea125-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-160">Questo comando crea un **recordSet** in corrispondenza dell'apice (o radice) della myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="ea125-161">A questo scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).</span><span class="sxs-lookup"><span data-stu-id="ea125-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="ea125-162">Non è possibile creare record CNAME nell'apice di un'area.</span><span class="sxs-lookup"><span data-stu-id="ea125-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="ea125-163">Questo è un vincolo degli standard DNS; non è una limitazione del DNS di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea125-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="ea125-164">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-165">Esempio 10: Creare un set di record con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ea125-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea125-166">Questo comando crea un **recordSet** denominato \* nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-167">Si tratta di un set di record con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ea125-167">This is a wildcard record set.</span></span>
<span data-ttu-id="ea125-168">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ea125-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea125-169">Esempio 11: Creare un set di record vuoto</span><span class="sxs-lookup"><span data-stu-id="ea125-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="ea125-170">Questo comando crea un **recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="ea125-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea125-171">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="ea125-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea125-172">Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere in seguito i record.</span><span class="sxs-lookup"><span data-stu-id="ea125-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="ea125-173">Esempio 12: Creare un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="ea125-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="ea125-174">Questo comando crea un **recordSet.**</span><span class="sxs-lookup"><span data-stu-id="ea125-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="ea125-175">Il *parametro Overwrite* assicura che questo set di record sovrascriva qualsiasi set di record pre-esistente con lo stesso nome e lo stesso tipo. I record esistenti in tale set di record andranno persi.</span><span class="sxs-lookup"><span data-stu-id="ea125-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="ea125-176">Il *parametro Confirm* con valore $False elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="ea125-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="ea125-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea125-177">PARAMETERS</span></span>

### <span data-ttu-id="ea125-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea125-178">-DefaultProfile</span></span>
<span data-ttu-id="ea125-179">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ea125-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea125-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="ea125-180">-DnsRecords</span></span>
<span data-ttu-id="ea125-181">Specifica la matrice di record DNS da includere nel set di record.</span><span class="sxs-lookup"><span data-stu-id="ea125-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="ea125-182">È possibile usare il cmdlet New-AzDnsRecordConfig per creare oggetti record DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="ea125-183">Per altre informazioni, vedere gli esempi.</span><span class="sxs-lookup"><span data-stu-id="ea125-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="ea125-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ea125-184">-Metadata</span></span>
<span data-ttu-id="ea125-185">Specifica una matrice di metadati da associare al recordSet.</span><span class="sxs-lookup"><span data-stu-id="ea125-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="ea125-186">I metadati vengono specificati usando coppie nome-valore rappresentate come tabelle hash, ad esempio @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="ea125-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="ea125-187">-Name</span><span class="sxs-lookup"><span data-stu-id="ea125-187">-Name</span></span>
<span data-ttu-id="ea125-188">Specifica il nome del **recordSet** da creare.</span><span class="sxs-lookup"><span data-stu-id="ea125-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="ea125-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ea125-189">-Overwrite</span></span>
<span data-ttu-id="ea125-190">Indica che questo cmdlet sovrascrive il **recordSet** specificato, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="ea125-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="ea125-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ea125-191">-RecordType</span></span>
<span data-ttu-id="ea125-192">Specifica il tipo di record DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="ea125-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="ea125-193">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ea125-193">Valid values are:</span></span>
- <span data-ttu-id="ea125-194">A</span><span class="sxs-lookup"><span data-stu-id="ea125-194">A</span></span>
- <span data-ttu-id="ea125-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="ea125-195">AAAA</span></span>
- <span data-ttu-id="ea125-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="ea125-196">CNAME</span></span>
- <span data-ttu-id="ea125-197">MX</span><span class="sxs-lookup"><span data-stu-id="ea125-197">MX</span></span>
- <span data-ttu-id="ea125-198">NS</span><span class="sxs-lookup"><span data-stu-id="ea125-198">NS</span></span>
- <span data-ttu-id="ea125-199">PTR</span><span class="sxs-lookup"><span data-stu-id="ea125-199">PTR</span></span>
- <span data-ttu-id="ea125-200">SRV</span><span class="sxs-lookup"><span data-stu-id="ea125-200">SRV</span></span>
- <span data-ttu-id="ea125-201">I record TXT SOA vengono creati automaticamente al momento della creazione dell'area e non possono essere creati manualmente.</span><span class="sxs-lookup"><span data-stu-id="ea125-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="ea125-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea125-202">-ResourceGroupName</span></span>
<span data-ttu-id="ea125-203">Specifica il gruppo di risorse che contiene l'area DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="ea125-204">È anche necessario specificare il *parametro ZoneName* per specificare il nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="ea125-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="ea125-205">In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="ea125-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ea125-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ea125-206">-TargetResourceId</span></span>
<span data-ttu-id="ea125-207">ID risorsa di destinazione alias.</span><span class="sxs-lookup"><span data-stu-id="ea125-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="ea125-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="ea125-208">-Ttl</span></span>
<span data-ttu-id="ea125-209">Specifica il valore Time to Live (TTL) per il recordSet DNS.</span><span class="sxs-lookup"><span data-stu-id="ea125-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="ea125-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="ea125-210">-Zone</span></span>
<span data-ttu-id="ea125-211">Specifica il valore DnsZone in cui creare il **recordSet.**</span><span class="sxs-lookup"><span data-stu-id="ea125-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="ea125-212">In alternativa, è possibile specificare l'area usando *i parametri ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ea125-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="ea125-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ea125-213">-ZoneName</span></span>
<span data-ttu-id="ea125-214">Specifica il nome dell'area in cui creare il **recordSet.**</span><span class="sxs-lookup"><span data-stu-id="ea125-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="ea125-215">È anche necessario specificare il gruppo di risorse che contiene l'area usando *il parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ea125-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ea125-216">In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="ea125-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ea125-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea125-217">-Confirm</span></span>
<span data-ttu-id="ea125-218">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea125-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea125-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea125-219">-WhatIf</span></span>
<span data-ttu-id="ea125-220">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea125-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea125-221">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea125-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea125-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea125-222">CommonParameters</span></span>
<span data-ttu-id="ea125-223">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea125-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea125-224">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea125-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea125-225">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea125-225">INPUTS</span></span>

### <span data-ttu-id="ea125-226">System.String</span><span class="sxs-lookup"><span data-stu-id="ea125-226">System.String</span></span>

### <span data-ttu-id="ea125-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="ea125-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="ea125-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ea125-228">System.UInt32</span></span>

### <span data-ttu-id="ea125-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="ea125-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="ea125-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea125-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ea125-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="ea125-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="ea125-232">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea125-232">OUTPUTS</span></span>

### <span data-ttu-id="ea125-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea125-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ea125-234">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea125-234">NOTES</span></span>
<span data-ttu-id="ea125-235">È possibile usare il *parametro Confirm* per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ea125-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ea125-236">Per impostazione predefinita, il cmdlet chiede conferma se la variabile $ConfirmPreference Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="ea125-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="ea125-237">Se si specifica *Conferma* o *Conferma:$True,* questo cmdlet richiede conferma prima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ea125-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ea125-238">Se si specifica *Conferma:$False,* il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="ea125-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ea125-239">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea125-239">RELATED LINKS</span></span>

[<span data-ttu-id="ea125-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ea125-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="ea125-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea125-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="ea125-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ea125-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="ea125-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea125-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="ea125-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea125-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
