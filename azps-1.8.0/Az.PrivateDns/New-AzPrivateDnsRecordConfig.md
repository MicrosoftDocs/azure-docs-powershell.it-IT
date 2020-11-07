---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677742"
---
# <span data-ttu-id="bfa7a-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="bfa7a-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="bfa7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfa7a-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa7a-103">Crea un nuovo oggetto locale record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="bfa7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfa7a-104">SYNTAX</span></span>

### <span data-ttu-id="bfa7a-105">A (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfa7a-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="bfa7a-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-107">MX</span><span class="sxs-lookup"><span data-stu-id="bfa7a-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-108">PTR</span><span class="sxs-lookup"><span data-stu-id="bfa7a-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-109">TXT</span><span class="sxs-lookup"><span data-stu-id="bfa7a-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-110">SRV</span><span class="sxs-lookup"><span data-stu-id="bfa7a-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfa7a-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="bfa7a-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfa7a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-112">DESCRIPTION</span></span>
<span data-ttu-id="bfa7a-113">Il cmdlet New-AzPrivateDnsRecordConfig crea un oggetto PSPrivateDnsRecord locale.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="bfa7a-114">Una matrice di questi oggetti viene passata al cmdlet New-AzPrivateDnsRecordSet usando il parametro PrivateDnsRecord per specificare i record da creare nel set di record.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="bfa7a-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfa7a-115">EXAMPLES</span></span>

### <span data-ttu-id="bfa7a-116">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="bfa7a-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="bfa7a-117">Questo esempio crea un RecordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-118">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-119">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="bfa7a-120">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="bfa7a-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="bfa7a-121">Questo esempio crea un RecordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-122">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-123">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="bfa7a-124">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bfa7a-125">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="bfa7a-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="bfa7a-126">Questo esempio crea un RecordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-127">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-128">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="bfa7a-129">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bfa7a-130">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="bfa7a-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="bfa7a-131">Questo comando crea un RecordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-132">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-133">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="bfa7a-134">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bfa7a-135">Esempio 5: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="bfa7a-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="bfa7a-136">Questo comando crea un RecordSet denominato 4 nella zona privata 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="bfa7a-137">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-138">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="bfa7a-139">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bfa7a-140">Esempio 6: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="bfa7a-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="bfa7a-141">Questo comando crea un RecordSet denominato _sip. _tcp nella zona privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-142">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-143">Contiene un singolo record DNS privato, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="bfa7a-144">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="bfa7a-145">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="bfa7a-146">Esempio 7: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="bfa7a-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="bfa7a-147">Questo comando crea un RecordSet denominato Text nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="bfa7a-148">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="bfa7a-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="bfa7a-149">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="bfa7a-150">Per creare un RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="bfa7a-151">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfa7a-151">PARAMETERS</span></span>

### <span data-ttu-id="bfa7a-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="bfa7a-152">-Cname</span></span>
<span data-ttu-id="bfa7a-153">Il nome canonico per il record CNAME da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="bfa7a-154">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="bfa7a-155">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-155">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa7a-156">-DefaultProfile</span></span>
<span data-ttu-id="bfa7a-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa7a-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="bfa7a-158">-Exchange</span></span>
<span data-ttu-id="bfa7a-159">L'host di Exchange Mail per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="bfa7a-160">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="bfa7a-161">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-161">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-162">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="bfa7a-162">-Ipv4Address</span></span>
<span data-ttu-id="bfa7a-163">Indirizzo IPv4 per il record a da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-163">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-164">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="bfa7a-164">-Ipv6Address</span></span>
<span data-ttu-id="bfa7a-165">Indirizzo IPv6 per il record AAAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-165">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-166">-Porta</span><span class="sxs-lookup"><span data-stu-id="bfa7a-166">-Port</span></span>
<span data-ttu-id="bfa7a-167">Numero di porta per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-167">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-168">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="bfa7a-168">-Preference</span></span>
<span data-ttu-id="bfa7a-169">Valore di preferenza per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-169">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-170">-Priorità</span><span class="sxs-lookup"><span data-stu-id="bfa7a-170">-Priority</span></span>
<span data-ttu-id="bfa7a-171">Record SRV del valore Priority da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-171">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="bfa7a-172">-Ptrdname</span></span>
<span data-ttu-id="bfa7a-173">L'host di destinazione per il record PTR da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="bfa7a-174">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="bfa7a-175">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-175">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-176">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-176">-Target</span></span>
<span data-ttu-id="bfa7a-177">L'host di destinazione per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="bfa7a-178">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="bfa7a-179">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="bfa7a-179">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-180">-Valore</span><span class="sxs-lookup"><span data-stu-id="bfa7a-180">-Value</span></span>
<span data-ttu-id="bfa7a-181">Valore di testo per il record TXT da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-181">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-182">-Peso</span><span class="sxs-lookup"><span data-stu-id="bfa7a-182">-Weight</span></span>
<span data-ttu-id="bfa7a-183">Valore di peso per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-183">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfa7a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa7a-184">CommonParameters</span></span>
<span data-ttu-id="bfa7a-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa7a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa7a-186">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa7a-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa7a-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfa7a-187">INPUTS</span></span>

### <span data-ttu-id="bfa7a-188">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bfa7a-188">None</span></span>

## <span data-ttu-id="bfa7a-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfa7a-189">OUTPUTS</span></span>

### <span data-ttu-id="bfa7a-190">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="bfa7a-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="bfa7a-191">Note</span><span class="sxs-lookup"><span data-stu-id="bfa7a-191">NOTES</span></span>

## <span data-ttu-id="bfa7a-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfa7a-192">RELATED LINKS</span></span>
