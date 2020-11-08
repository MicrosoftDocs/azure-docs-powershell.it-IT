---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188982"
---
# <span data-ttu-id="8eaa7-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8eaa7-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="8eaa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8eaa7-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaa7-103">Rimuove un record DNS privato da un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="8eaa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eaa7-104">SYNTAX</span></span>

### <span data-ttu-id="8eaa7-105">A (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8eaa7-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="8eaa7-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-107">MX</span><span class="sxs-lookup"><span data-stu-id="8eaa7-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-108">PTR</span><span class="sxs-lookup"><span data-stu-id="8eaa7-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-109">TXT</span><span class="sxs-lookup"><span data-stu-id="8eaa7-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-110">SRV</span><span class="sxs-lookup"><span data-stu-id="8eaa7-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eaa7-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="8eaa7-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eaa7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-112">DESCRIPTION</span></span>
<span data-ttu-id="8eaa7-113">Il cmdlet Remove-AzPrivateDnsRecordConfig rimuove un record DNS (Domain Name System) privato da un set di record.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="8eaa7-114">L'oggetto RecordSet è un oggetto offline e le modifiche apportate non modificano le risposte DNS private finché non viene eseguito il cmdlet Set-AzPrivateDnsRecordSet per rendere persistente la modifica al servizio DNS privato di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="8eaa7-115">Per rimuovere un record, tutti i campi per il tipo di record devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="8eaa7-116">Non è possibile aggiungere o rimuovere record SOA.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="8eaa7-117">I record SOA vengono creati automaticamente quando viene creata e eliminata automaticamente una zona DNS privata quando viene eliminata la zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="8eaa7-118">Puoi passare l'oggetto RecordSet a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="8eaa7-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eaa7-119">EXAMPLES</span></span>

### <span data-ttu-id="8eaa7-120">Esempio 1: rimuovere un record da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-121">Questo esempio rimuove un record A da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="8eaa7-122">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="8eaa7-123">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8eaa7-124">Esempio 2: rimuovere un record AAAA da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-125">In questo esempio viene rimosso un record AAAA da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="8eaa7-126">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="8eaa7-127">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8eaa7-128">Esempio 3: rimuovere un record CNAME da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-129">In questo esempio viene rimosso un record CNAME da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="8eaa7-130">Dato che un set di record CNAME può contenere al massimo un record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="8eaa7-131">Esempio 4: rimuovere un record MX da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-132">In questo esempio viene rimosso un record MX da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="8eaa7-133">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="8eaa7-134">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8eaa7-135">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8eaa7-136">Esempio 5: rimuovere un record PTR da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-137">In questo esempio viene rimosso un record PTR da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="8eaa7-138">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8eaa7-139">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8eaa7-140">Esempio 6: rimuovere un record SRV da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-141">In questo esempio viene rimosso un record SRV da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="8eaa7-142">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8eaa7-143">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="8eaa7-144">Esempio 7: rimuovere un record TXT da un set di record</span><span class="sxs-lookup"><span data-stu-id="8eaa7-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="8eaa7-145">In questo esempio viene rimosso un record TXT da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="8eaa7-146">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="8eaa7-147">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="8eaa7-148">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8eaa7-148">PARAMETERS</span></span>

### <span data-ttu-id="8eaa7-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="8eaa7-149">-Cname</span></span>
<span data-ttu-id="8eaa7-150">Nome canonico del record CNAME da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="8eaa7-151">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8eaa7-152">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8eaa7-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eaa7-153">-DefaultProfile</span></span>
<span data-ttu-id="8eaa7-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eaa7-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8eaa7-155">-Exchange</span></span>
<span data-ttu-id="8eaa7-156">L'host di Exchange mail del record MX da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="8eaa7-157">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8eaa7-158">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8eaa7-159">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="8eaa7-159">-Ipv4Address</span></span>
<span data-ttu-id="8eaa7-160">Indirizzo IPv4 del record a da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-161">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="8eaa7-161">-Ipv6Address</span></span>
<span data-ttu-id="8eaa7-162">Indirizzo IPv6 del record AAAA da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-163">-Porta</span><span class="sxs-lookup"><span data-stu-id="8eaa7-163">-Port</span></span>
<span data-ttu-id="8eaa7-164">Numero di porta del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-165">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="8eaa7-165">-Preference</span></span>
<span data-ttu-id="8eaa7-166">Valore di preferenza del record MX da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-167">-Priorità</span><span class="sxs-lookup"><span data-stu-id="8eaa7-167">-Priority</span></span>
<span data-ttu-id="8eaa7-168">Valore Priority del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8eaa7-169">-Ptrdname</span></span>
<span data-ttu-id="8eaa7-170">L'host di destinazione del record PTR da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="8eaa7-171">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8eaa7-172">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8eaa7-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaa7-173">-RecordSet</span></span>
<span data-ttu-id="8eaa7-174">Set di record da cui rimuovere il record.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-174">The record set from which to remove the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaa7-175">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-175">-Target</span></span>
<span data-ttu-id="8eaa7-176">L'host di destinazione del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="8eaa7-177">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="8eaa7-178">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="8eaa7-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="8eaa7-179">-Valore</span><span class="sxs-lookup"><span data-stu-id="8eaa7-179">-Value</span></span>
<span data-ttu-id="8eaa7-180">Valore di testo del record TXT da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-181">-Peso</span><span class="sxs-lookup"><span data-stu-id="8eaa7-181">-Weight</span></span>
<span data-ttu-id="8eaa7-182">Valore di peso del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="8eaa7-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaa7-183">CommonParameters</span></span>
<span data-ttu-id="8eaa7-184">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eaa7-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaa7-185">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaa7-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaa7-186">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8eaa7-186">INPUTS</span></span>

### <span data-ttu-id="8eaa7-187">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaa7-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8eaa7-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eaa7-188">OUTPUTS</span></span>

### <span data-ttu-id="8eaa7-189">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8eaa7-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="8eaa7-190">Note</span><span class="sxs-lookup"><span data-stu-id="8eaa7-190">NOTES</span></span>

## <span data-ttu-id="8eaa7-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eaa7-191">RELATED LINKS</span></span>
