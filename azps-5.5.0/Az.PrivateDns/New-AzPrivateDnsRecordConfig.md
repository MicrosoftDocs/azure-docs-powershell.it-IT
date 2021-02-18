---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202119"
---
# <span data-ttu-id="e041d-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="e041d-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="e041d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e041d-102">SYNOPSIS</span></span>
<span data-ttu-id="e041d-103">Crea un nuovo oggetto locale del record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="e041d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e041d-104">SYNTAX</span></span>

### <span data-ttu-id="e041d-105">A (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e041d-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e041d-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="e041d-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e041d-107">MX</span><span class="sxs-lookup"><span data-stu-id="e041d-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e041d-108">PTR</span><span class="sxs-lookup"><span data-stu-id="e041d-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e041d-109">TXT</span><span class="sxs-lookup"><span data-stu-id="e041d-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e041d-110">SRV</span><span class="sxs-lookup"><span data-stu-id="e041d-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e041d-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="e041d-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e041d-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e041d-112">DESCRIPTION</span></span>
<span data-ttu-id="e041d-113">Il cmdlet New-AzPrivateDnsRecordConfig crea un oggetto PSPrivateDnsRecord locale.</span><span class="sxs-lookup"><span data-stu-id="e041d-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="e041d-114">Una matrice di questi oggetti viene passata al cmdlet New-AzPrivateDnsRecordSet l'uso del parametro PrivateDnsRecord per specificare i record da creare nel set di record.</span><span class="sxs-lookup"><span data-stu-id="e041d-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="e041d-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e041d-115">EXAMPLES</span></span>

### <span data-ttu-id="e041d-116">Esempio 1: Creare un recordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="e041d-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="e041d-117">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-118">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-119">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="e041d-120">Esempio 2: Creare un recordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="e041d-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="e041d-121">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-122">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-123">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="e041d-124">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="e041d-125">Esempio 3: Creare un recordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="e041d-125">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="e041d-126">In questo esempio viene creato un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-127">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-128">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="e041d-129">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="e041d-130">Esempio 4: Creare un recordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="e041d-130">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="e041d-131">Questo comando crea un recordSet denominato www nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-132">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-133">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="e041d-134">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="e041d-135">Esempio 5: Creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="e041d-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="e041d-136">Questo comando crea un recordSet denominato 4 nell'area privata 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="e041d-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="e041d-137">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-138">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="e041d-139">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="e041d-140">Esempio 6: Creare un recordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="e041d-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="e041d-141">Questo comando crea un recordSet denominato _sip._tcp nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-142">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-143">Contiene un singolo record DNS privato che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="e041d-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="e041d-144">Il servizio (sip) e il protocollo (tcp) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="e041d-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="e041d-145">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="e041d-146">Esempio 7: Creare un recordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="e041d-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="e041d-147">Questo comando crea un recordSet denominato testo nell'area privata myzone.com.</span><span class="sxs-lookup"><span data-stu-id="e041d-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="e041d-148">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="e041d-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="e041d-149">Contiene un singolo record DNS privato.</span><span class="sxs-lookup"><span data-stu-id="e041d-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="e041d-150">Per creare un record RecordSet usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e041d-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="e041d-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e041d-151">PARAMETERS</span></span>

### <span data-ttu-id="e041d-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="e041d-152">-Cname</span></span>
<span data-ttu-id="e041d-153">Nome canonico del record CNAME da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="e041d-154">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="e041d-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e041d-155">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="e041d-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e041d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e041d-156">-DefaultProfile</span></span>
<span data-ttu-id="e041d-157">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e041d-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e041d-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="e041d-158">-Exchange</span></span>
<span data-ttu-id="e041d-159">Host Mail Exchange per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="e041d-160">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="e041d-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e041d-161">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="e041d-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e041d-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="e041d-162">-Ipv4Address</span></span>
<span data-ttu-id="e041d-163">Indirizzo IPv4 del record A da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="e041d-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="e041d-164">-Ipv6Address</span></span>
<span data-ttu-id="e041d-165">Indirizzo IPv6 del record AAAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="e041d-166">-Porta</span><span class="sxs-lookup"><span data-stu-id="e041d-166">-Port</span></span>
<span data-ttu-id="e041d-167">Numero di porta per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="e041d-168">-Preference</span><span class="sxs-lookup"><span data-stu-id="e041d-168">-Preference</span></span>
<span data-ttu-id="e041d-169">Valore della preferenza per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="e041d-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="e041d-170">-Priority</span></span>
<span data-ttu-id="e041d-171">Il record SRV del valore di priorità da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="e041d-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="e041d-172">-Ptrdname</span></span>
<span data-ttu-id="e041d-173">Host di destinazione per il record PTR da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="e041d-174">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="e041d-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e041d-175">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="e041d-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e041d-176">-Target</span><span class="sxs-lookup"><span data-stu-id="e041d-176">-Target</span></span>
<span data-ttu-id="e041d-177">Host di destinazione per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="e041d-178">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="e041d-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="e041d-179">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="e041d-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="e041d-180">-Value</span><span class="sxs-lookup"><span data-stu-id="e041d-180">-Value</span></span>
<span data-ttu-id="e041d-181">Valore di testo per il record TXT da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="e041d-182">-Spessore</span><span class="sxs-lookup"><span data-stu-id="e041d-182">-Weight</span></span>
<span data-ttu-id="e041d-183">Valore del peso del record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e041d-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="e041d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e041d-184">CommonParameters</span></span>
<span data-ttu-id="e041d-185">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e041d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e041d-186">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e041d-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e041d-187">INPUT</span><span class="sxs-lookup"><span data-stu-id="e041d-187">INPUTS</span></span>

### <span data-ttu-id="e041d-188">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e041d-188">None</span></span>

## <span data-ttu-id="e041d-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e041d-189">OUTPUTS</span></span>

### <span data-ttu-id="e041d-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e041d-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="e041d-191">NOTE</span><span class="sxs-lookup"><span data-stu-id="e041d-191">NOTES</span></span>

## <span data-ttu-id="e041d-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e041d-192">RELATED LINKS</span></span>
