---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855913"
---
# <span data-ttu-id="f73ae-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f73ae-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f73ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f73ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f73ae-103">Aggiunge un record DNS privato a un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="f73ae-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="f73ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f73ae-104">SYNTAX</span></span>

### <span data-ttu-id="f73ae-105">A (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f73ae-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f73ae-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-107">MX</span><span class="sxs-lookup"><span data-stu-id="f73ae-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-108">PTR</span><span class="sxs-lookup"><span data-stu-id="f73ae-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-109">TXT</span><span class="sxs-lookup"><span data-stu-id="f73ae-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f73ae-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f73ae-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="f73ae-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f73ae-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f73ae-112">DESCRIPTION</span></span>
<span data-ttu-id="f73ae-113">Il cmdlet Add-AzPrivateDnsRecordConfig aggiunge un record DNS (Domain Name System) privato a un oggetto RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f73ae-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="f73ae-114">L'oggetto RecordSet è un oggetto offline e le modifiche apportate non modificano le risposte DNS private finché non viene eseguito il cmdlet Set-AzPrivateDnsRecordSet per rendere persistente la modifica al servizio DNS privato di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f73ae-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="f73ae-115">I record SOA vengono creati quando viene creata una zona DNS privata e vengono rimossi quando viene eliminata la zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="f73ae-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="f73ae-116">Non è possibile aggiungere o rimuovere record SOA, ma è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="f73ae-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="f73ae-117">Puoi passare l'oggetto RecordSet a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f73ae-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f73ae-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f73ae-118">EXAMPLES</span></span>

### <span data-ttu-id="f73ae-119">Esempio 1: aggiungere un record a in un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f73ae-120">Questo esempio aggiunge un record a a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-121">Esempio 2: aggiungere un record AAAA a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f73ae-122">Questo esempio aggiunge un record AAAAa a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-123">Esempio 3: aggiungere un record CNAME a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="f73ae-124">Questo esempio aggiunge un record CNAME a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-125">Esempio 4: aggiungere un record MX a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="f73ae-126">Questo esempio aggiunge un record MX a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-127">Esempio 5: aggiungere un record PTR a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="f73ae-128">Questo esempio aggiunge un record PTR a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-129">Esempio 6: aggiungere un record SRV a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="f73ae-130">Questo esempio aggiunge un record SRV a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="f73ae-131">Esempio 7: aggiungere un record TXT a un set di record</span><span class="sxs-lookup"><span data-stu-id="f73ae-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

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

<span data-ttu-id="f73ae-132">Questo esempio aggiunge un record TXT a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f73ae-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="f73ae-133">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f73ae-133">PARAMETERS</span></span>

### <span data-ttu-id="f73ae-134">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f73ae-134">-Cname</span></span>
<span data-ttu-id="f73ae-135">Il nome canonico per il record CNAME da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="f73ae-136">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="f73ae-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f73ae-137">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="f73ae-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f73ae-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73ae-138">-DefaultProfile</span></span>
<span data-ttu-id="f73ae-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f73ae-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f73ae-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f73ae-140">-Exchange</span></span>
<span data-ttu-id="f73ae-141">L'host di Exchange Mail per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="f73ae-142">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="f73ae-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f73ae-143">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="f73ae-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f73ae-144">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="f73ae-144">-Ipv4Address</span></span>
<span data-ttu-id="f73ae-145">Indirizzo IPv4 per il record a da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="f73ae-146">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="f73ae-146">-Ipv6Address</span></span>
<span data-ttu-id="f73ae-147">Indirizzo IPv6 per il record AAAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="f73ae-148">-Porta</span><span class="sxs-lookup"><span data-stu-id="f73ae-148">-Port</span></span>
<span data-ttu-id="f73ae-149">Numero di porta per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="f73ae-150">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="f73ae-150">-Preference</span></span>
<span data-ttu-id="f73ae-151">Valore di preferenza per il record MX da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="f73ae-152">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f73ae-152">-Priority</span></span>
<span data-ttu-id="f73ae-153">Record SRV del valore Priority da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="f73ae-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f73ae-154">-Ptrdname</span></span>
<span data-ttu-id="f73ae-155">L'host di destinazione per il record PTR da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="f73ae-156">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="f73ae-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f73ae-157">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="f73ae-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f73ae-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f73ae-158">-RecordSet</span></span>
<span data-ttu-id="f73ae-159">Set di record in cui aggiungere il record.</span><span class="sxs-lookup"><span data-stu-id="f73ae-159">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="f73ae-160">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="f73ae-160">-Target</span></span>
<span data-ttu-id="f73ae-161">L'host di destinazione per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="f73ae-162">Non deve essere relativo al nome della zona.</span><span class="sxs-lookup"><span data-stu-id="f73ae-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f73ae-163">Non deve avere un punto di terminazione</span><span class="sxs-lookup"><span data-stu-id="f73ae-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f73ae-164">-Valore</span><span class="sxs-lookup"><span data-stu-id="f73ae-164">-Value</span></span>
<span data-ttu-id="f73ae-165">Valore di testo per il record TXT da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="f73ae-166">-Peso</span><span class="sxs-lookup"><span data-stu-id="f73ae-166">-Weight</span></span>
<span data-ttu-id="f73ae-167">Valore di peso per il record SRV da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f73ae-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="f73ae-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73ae-168">CommonParameters</span></span>
<span data-ttu-id="f73ae-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73ae-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73ae-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73ae-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73ae-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f73ae-171">INPUTS</span></span>

### <span data-ttu-id="f73ae-172">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f73ae-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f73ae-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f73ae-173">OUTPUTS</span></span>

### <span data-ttu-id="f73ae-174">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f73ae-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f73ae-175">Note</span><span class="sxs-lookup"><span data-stu-id="f73ae-175">NOTES</span></span>

## <span data-ttu-id="f73ae-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f73ae-176">RELATED LINKS</span></span>
