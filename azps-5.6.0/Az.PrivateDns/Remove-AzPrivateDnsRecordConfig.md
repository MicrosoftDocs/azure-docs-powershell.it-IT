---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: cd0e2f2913a950e677b1f7294076351556b81c80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005869"
---
# <span data-ttu-id="6e89a-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6e89a-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="6e89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e89a-102">SYNOPSIS</span></span>
<span data-ttu-id="6e89a-103">Rimuove un record DNS privato da un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="6e89a-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="6e89a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e89a-104">SYNTAX</span></span>

### <span data-ttu-id="6e89a-105">A (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e89a-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6e89a-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-107">MX</span><span class="sxs-lookup"><span data-stu-id="6e89a-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-108">PTR</span><span class="sxs-lookup"><span data-stu-id="6e89a-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-109">TXT</span><span class="sxs-lookup"><span data-stu-id="6e89a-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-110">SRV</span><span class="sxs-lookup"><span data-stu-id="6e89a-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e89a-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="6e89a-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e89a-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e89a-112">DESCRIPTION</span></span>
<span data-ttu-id="6e89a-113">Il cmdlet Remove-AzPrivateDnsRecordConfig rimuove un record DNS (Domain Name System) privato da un set di record.</span><span class="sxs-lookup"><span data-stu-id="6e89a-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="6e89a-114">L'oggetto RecordSet è un oggetto offline e le modifiche apportate non modificano le risposte DNS private finché non si esegue il cmdlet Set-AzPrivateDnsRecordSet per mantenere la modifica nel servizio DNS privato di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6e89a-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="6e89a-115">Per rimuovere un record, tutti i campi di quel tipo di record devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="6e89a-116">Non è possibile aggiungere o rimuovere record SOA.</span><span class="sxs-lookup"><span data-stu-id="6e89a-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="6e89a-117">I record SOA vengono creati automaticamente quando viene creata un'area DNS privata ed eliminata automaticamente quando l'area DNS privata viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="6e89a-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="6e89a-118">È possibile passare l'oggetto RecordSet a questo cmdlet come parametro o usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e89a-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6e89a-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e89a-119">EXAMPLES</span></span>

### <span data-ttu-id="6e89a-120">Esempio 1: Rimuovere un record A da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-120">Example 1: Remove an A record from a record set</span></span>
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

<span data-ttu-id="6e89a-121">Questo esempio rimuove un record A da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="6e89a-122">Se questo è l'unico record del set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="6e89a-123">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="6e89a-124">Esempio 2: Rimuovere un record AAAA da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-124">Example 2: Remove an AAAA record from a record set</span></span>
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

<span data-ttu-id="6e89a-125">Questo esempio rimuove un record AAAA da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="6e89a-126">Se questo è l'unico record del set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="6e89a-127">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="6e89a-128">Esempio 3: Rimuovere un record CNAME da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-128">Example 3: Remove a CNAME record from a record set</span></span>
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

<span data-ttu-id="6e89a-129">Questo esempio rimuove un record CNAME da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="6e89a-130">Poiché un set di record CNAME può contenere al massimo un record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="6e89a-131">Esempio 4: Rimuovere un record MX da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-131">Example 4: Remove a MX record from a record set</span></span>
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

<span data-ttu-id="6e89a-132">Questo esempio rimuove un record MX da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="6e89a-133">Il nome record "@" indica un set di record nell'apice della zona.</span><span class="sxs-lookup"><span data-stu-id="6e89a-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="6e89a-134">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="6e89a-135">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="6e89a-136">Esempio 5: Rimuovere un record PTR da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-136">Example 5: Remove a PTR record from a record set</span></span>
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

<span data-ttu-id="6e89a-137">Questo esempio rimuove un record PTR da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="6e89a-138">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="6e89a-139">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="6e89a-140">Esempio 6: Rimuovere un record SRV da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-140">Example 6: Remove a SRV record from a record set</span></span>
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

<span data-ttu-id="6e89a-141">Questo esempio rimuove un record SRV da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="6e89a-142">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="6e89a-143">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="6e89a-144">Esempio 7: Rimuovere un record TXT da un set di record</span><span class="sxs-lookup"><span data-stu-id="6e89a-144">Example 7: Remove a TXT record from a record set</span></span>
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

<span data-ttu-id="6e89a-145">Questo esempio rimuove un record TXT da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="6e89a-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="6e89a-146">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="6e89a-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="6e89a-147">Per rimuovere completamente un set di record, vedere Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="6e89a-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="6e89a-148">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e89a-148">PARAMETERS</span></span>

### <span data-ttu-id="6e89a-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="6e89a-149">-Cname</span></span>
<span data-ttu-id="6e89a-150">Nome canonico del record CNAME da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="6e89a-151">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="6e89a-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="6e89a-152">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="6e89a-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="6e89a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e89a-153">-DefaultProfile</span></span>
<span data-ttu-id="6e89a-154">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e89a-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e89a-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6e89a-155">-Exchange</span></span>
<span data-ttu-id="6e89a-156">Host mail exchange del record MX da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="6e89a-157">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="6e89a-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="6e89a-158">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="6e89a-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="6e89a-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6e89a-159">-Ipv4Address</span></span>
<span data-ttu-id="6e89a-160">Indirizzo IPv4 del record A da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="6e89a-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="6e89a-161">-Ipv6Address</span></span>
<span data-ttu-id="6e89a-162">Indirizzo IPv6 del record AAAA da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="6e89a-163">-Port</span><span class="sxs-lookup"><span data-stu-id="6e89a-163">-Port</span></span>
<span data-ttu-id="6e89a-164">Numero di porta del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="6e89a-165">-Preference</span><span class="sxs-lookup"><span data-stu-id="6e89a-165">-Preference</span></span>
<span data-ttu-id="6e89a-166">Valore della preferenza per il record MX da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="6e89a-167">-Priority</span><span class="sxs-lookup"><span data-stu-id="6e89a-167">-Priority</span></span>
<span data-ttu-id="6e89a-168">Valore di priorità del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="6e89a-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6e89a-169">-Ptrdname</span></span>
<span data-ttu-id="6e89a-170">Host di destinazione del record PTR da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="6e89a-171">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="6e89a-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="6e89a-172">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="6e89a-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="6e89a-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="6e89a-173">-RecordSet</span></span>
<span data-ttu-id="6e89a-174">Set di record da cui rimuovere il record.</span><span class="sxs-lookup"><span data-stu-id="6e89a-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="6e89a-175">-Target</span><span class="sxs-lookup"><span data-stu-id="6e89a-175">-Target</span></span>
<span data-ttu-id="6e89a-176">Host di destinazione del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="6e89a-177">Non deve essere relativo al nome dell'area.</span><span class="sxs-lookup"><span data-stu-id="6e89a-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="6e89a-178">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="6e89a-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="6e89a-179">-Value</span><span class="sxs-lookup"><span data-stu-id="6e89a-179">-Value</span></span>
<span data-ttu-id="6e89a-180">Valore di testo del record TXT da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="6e89a-181">-Spessore</span><span class="sxs-lookup"><span data-stu-id="6e89a-181">-Weight</span></span>
<span data-ttu-id="6e89a-182">Valore del peso del record SRV da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e89a-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="6e89a-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e89a-183">CommonParameters</span></span>
<span data-ttu-id="6e89a-184">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e89a-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e89a-185">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e89a-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e89a-186">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e89a-186">INPUTS</span></span>

### <span data-ttu-id="6e89a-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e89a-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="6e89a-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e89a-188">OUTPUTS</span></span>

### <span data-ttu-id="6e89a-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e89a-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="6e89a-190">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e89a-190">NOTES</span></span>

## <span data-ttu-id="6e89a-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e89a-191">RELATED LINKS</span></span>
