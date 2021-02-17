---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189343"
---
# <span data-ttu-id="5a1e5-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5a1e5-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5a1e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1e5-103">Crea un set di record in un'area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="5a1e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a1e5-104">SYNTAX</span></span>

### <span data-ttu-id="5a1e5-105">Campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a1e5-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a1e5-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="5a1e5-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a1e5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a1e5-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a1e5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a1e5-108">DESCRIPTION</span></span>
<span data-ttu-id="5a1e5-109">Il cmdlet New-AzPrivateDnsRecordSet crea un nuovo record DNS (Private Domain Name System) con il nome specificato e digita nell'area privata specificata.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="5a1e5-110">Un oggetto RecordSet è un set di record DNS privati con lo stesso nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="5a1e5-111">Si noti che il nome è relativo all'area privata e non al nome completo.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="5a1e5-112">Il parametro PrivateDnsRecord specifica i record nel set di record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="5a1e5-113">Questo parametro accetta una matrice di record DNS privati, costruita con New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="5a1e5-114">È possibile usare l'operatore della pipeline per passare un oggetto PSPrivateDnsZone a questo cmdlet oppure passare un oggetto PSPrivateDnsZone come parametro Zone oppure è possibile specificare l'area in base al valore ResourceId oppure è possibile specificare l'area in base al nome.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="5a1e5-115">È possibile usare il parametro Confirm $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="5a1e5-116">Se esiste già un RecordSet corrispondente (stesso nome e tipo di record), è necessario specificare il parametro Overwrite, altrimenti il cmdlet non creerà un nuovo RecordSet.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="5a1e5-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a1e5-117">EXAMPLES</span></span>

### <span data-ttu-id="5a1e5-118">Esempio 1: Creare un recordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="5a1e5-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-119">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-120">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-121">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="5a1e5-122">Esempio 2: Creare un recordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="5a1e5-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-123">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-124">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-125">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="5a1e5-126">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-127">Esempio 3: Creare un recordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="5a1e5-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-128">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-129">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-130">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="5a1e5-131">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-132">Esempio 4: Creare un recordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="5a1e5-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-133">Questo comando crea un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-134">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-135">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="5a1e5-136">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-137">Esempio 5: Creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="5a1e5-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-138">Questo comando crea un recordSet denominato 4 nell'area privata 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="5a1e5-139">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-140">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="5a1e5-141">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-142">Esempio 6: Creare un recordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="5a1e5-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-143">Questo comando crea un recordSet denominato _sip._tcp nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-144">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-145">Contiene un singolo record DNS privato che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="5a1e5-146">Il servizio (sip) e il protocollo (tcp) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="5a1e5-147">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-148">Esempio 7: Creare un recordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="5a1e5-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-149">Questo comando crea un recordSet denominato testo nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-150">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-151">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="5a1e5-152">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-153">Esempio 8: Creare un recordSet nell'apice zone</span><span class="sxs-lookup"><span data-stu-id="5a1e5-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-154">Questo comando crea un recordSet in corrispondenza dell'apice (o radice) dell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-155">A questo scopo, il nome del set di record viene specificato come "@" (incluse le virgolette doppie).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="5a1e5-156">Non è possibile creare record CNAME nell'apice di un'area.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="5a1e5-157">Questo è un vincolo degli standard DNS; non è una limitazione del DNS privato di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="5a1e5-158">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-159">Esempio 9: Creare un set di record con caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="5a1e5-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-160">Questo comando crea un recordSet denominato \* nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-161">Si tratta di un set di record con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-161">This is a wildcard record set.</span></span> <span data-ttu-id="5a1e5-162">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="5a1e5-163">Esempio 10: Creare un set di record vuoto</span><span class="sxs-lookup"><span data-stu-id="5a1e5-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="5a1e5-164">Questo comando crea un recordSet denominato \* nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="5a1e5-165">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="5a1e5-166">Si tratta di un set di record vuoto, che funge da segnaposto a cui è possibile aggiungere in seguito i record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="5a1e5-167">Esempio 11: Creare un set di record ed eliminare tutte le conferme</span><span class="sxs-lookup"><span data-stu-id="5a1e5-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="5a1e5-168">Questo comando crea un recordSet.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-168">This command creates a RecordSet.</span></span> <span data-ttu-id="5a1e5-169">Il parametro Overwrite assicura che questo set di record sovrascriva qualsiasi set di record pre-esistente con lo stesso nome e lo stesso tipo. I record esistenti in tale set di record andranno persi.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="5a1e5-170">Il parametro Confirm con valore $False elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="5a1e5-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a1e5-171">PARAMETERS</span></span>

### <span data-ttu-id="5a1e5-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1e5-172">-DefaultProfile</span></span>
<span data-ttu-id="5a1e5-173">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a1e5-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5a1e5-174">-Metadata</span></span>
<span data-ttu-id="5a1e5-175">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-176">-Name</span><span class="sxs-lookup"><span data-stu-id="5a1e5-176">-Name</span></span>
<span data-ttu-id="5a1e5-177">Nome dei record in questo set di record (relativo al nome dell'area e senza punto di chiusura).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5a1e5-178">-Overwrite</span></span>
<span data-ttu-id="5a1e5-179">Non eseguire errori se il set di record esiste già.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="5a1e5-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5a1e5-180">-ParentResourceId</span></span>
<span data-ttu-id="5a1e5-181">ID Risorsa area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="5a1e5-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="5a1e5-183">Record DNS privati che fanno parte di questo set di record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="5a1e5-184">-RecordType</span></span>
<span data-ttu-id="5a1e5-185">Tipo di record DNS privati in questo set di record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a1e5-186">-ResourceGroupName</span></span>
<span data-ttu-id="5a1e5-187">Gruppo di risorse a cui appartiene l'area.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="5a1e5-188">-Ttl</span></span>
<span data-ttu-id="5a1e5-189">Valore TTL di tutti i record in questo set di record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="5a1e5-190">-Zone</span></span>
<span data-ttu-id="5a1e5-191">Oggetto PrivateDnsZone che rappresenta l'area in cui creare il set di record.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="5a1e5-192">-ZoneName</span></span>
<span data-ttu-id="5a1e5-193">Area in cui creare il set di record (senza punto di chiusura).</span><span class="sxs-lookup"><span data-stu-id="5a1e5-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a1e5-194">-Confirm</span></span>
<span data-ttu-id="5a1e5-195">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a1e5-196">-WhatIf</span></span>
<span data-ttu-id="5a1e5-197">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a1e5-198">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a1e5-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1e5-199">CommonParameters</span></span>
<span data-ttu-id="5a1e5-200">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a1e5-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1e5-201">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a1e5-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1e5-202">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a1e5-202">INPUTS</span></span>

### <span data-ttu-id="5a1e5-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a1e5-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="5a1e5-204">System.String</span><span class="sxs-lookup"><span data-stu-id="5a1e5-204">System.String</span></span>

## <span data-ttu-id="5a1e5-205">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a1e5-205">OUTPUTS</span></span>

### <span data-ttu-id="5a1e5-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5a1e5-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="5a1e5-207">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a1e5-207">NOTES</span></span>

## <span data-ttu-id="5a1e5-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a1e5-208">RELATED LINKS</span></span>
