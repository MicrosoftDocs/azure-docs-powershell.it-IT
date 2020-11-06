---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 1e0a7de22b459f5d87c4a79bb91ef4c36f88ad77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519019"
---
# <span data-ttu-id="be490-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="be490-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="be490-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be490-102">SYNOPSIS</span></span>
<span data-ttu-id="be490-103">Rimuove un record DNS da un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="be490-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be490-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be490-104">SYNTAX</span></span>

### <span data-ttu-id="be490-105">Un</span><span class="sxs-lookup"><span data-stu-id="be490-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="be490-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-107">NS</span><span class="sxs-lookup"><span data-stu-id="be490-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-108">MX</span><span class="sxs-lookup"><span data-stu-id="be490-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-109">PTR</span><span class="sxs-lookup"><span data-stu-id="be490-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-110">TXT</span><span class="sxs-lookup"><span data-stu-id="be490-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-111">SRV</span><span class="sxs-lookup"><span data-stu-id="be490-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="be490-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be490-113">CAA</span><span class="sxs-lookup"><span data-stu-id="be490-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be490-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be490-114">DESCRIPTION</span></span>
<span data-ttu-id="be490-115">Il cmdlet **Remove-AzureRmDnsRecordConfig** rimuove un record DNS (Domain Name System) da un set di record.</span><span class="sxs-lookup"><span data-stu-id="be490-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="be490-116">L'oggetto **Recordset** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non viene eseguito il cmdlet Set-AzureRmDnsRecordSet per rendere persistente la modifica al servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="be490-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="be490-117">Per rimuovere un record, tutti i campi per il tipo di record devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="be490-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="be490-118">Non è possibile aggiungere o rimuovere record SOA.</span><span class="sxs-lookup"><span data-stu-id="be490-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="be490-119">I record SOA vengono creati automaticamente quando viene creata e eliminata automaticamente una zona DNS quando la zona DNS viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="be490-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="be490-120">Puoi passare l'oggetto **Recordset** a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="be490-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="be490-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be490-121">EXAMPLES</span></span>

### <span data-ttu-id="be490-122">Esempio 1: rimuovere un record da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-123">Questo esempio rimuove un record A da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="be490-124">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="be490-125">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-126">Esempio 2: rimuovere un record AAAA da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-127">In questo esempio viene rimosso un record AAAA da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="be490-128">Se questo è l'unico record nel set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="be490-129">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-130">Esempio 3: rimuovere un record CNAME da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-131">In questo esempio viene rimosso un record CNAME da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="be490-132">Dato che un set di record CNAME può contenere al massimo un record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="be490-133">Esempio 4: rimuovere un record MX da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-134">In questo esempio viene rimosso un record MX da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="be490-135">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="be490-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="be490-136">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="be490-137">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-138">Esempio 5: rimuovere un record NS da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-139">In questo esempio viene rimosso un record NS da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="be490-140">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="be490-141">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-142">Esempio 6: rimuovere un record PTR da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-143">In questo esempio viene rimosso un record PTR da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="be490-144">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="be490-145">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-146">Esempio 7: rimuovere un record SRV da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-147">In questo esempio viene rimosso un record SRV da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="be490-148">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="be490-149">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="be490-150">Esempio 8: rimuovere un record TXT da un set di record</span><span class="sxs-lookup"><span data-stu-id="be490-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="be490-151">In questo esempio viene rimosso un record TXT da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="be490-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="be490-152">Se questo è l'unico record nel set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="be490-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="be490-153">Per rimuovere completamente un set di record, vedere Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="be490-154">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be490-154">PARAMETERS</span></span>

### <span data-ttu-id="be490-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="be490-155">-CaaFlags</span></span>
<span data-ttu-id="be490-156">I contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="be490-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="be490-157">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="be490-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="be490-158">-CaaTag</span></span>
<span data-ttu-id="be490-159">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="be490-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="be490-160">-CaaValue</span></span>
<span data-ttu-id="be490-161">Campo valore per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="be490-161">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="be490-162">-Cname</span></span>
<span data-ttu-id="be490-163">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="be490-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be490-164">-DefaultProfile</span></span>
<span data-ttu-id="be490-165">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="be490-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be490-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="be490-166">-Exchange</span></span>
<span data-ttu-id="be490-167">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="be490-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-168">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="be490-168">-Ipv4Address</span></span>
<span data-ttu-id="be490-169">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="be490-169">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-170">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="be490-170">-Ipv6Address</span></span>
<span data-ttu-id="be490-171">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="be490-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="be490-172">-Nsdname</span></span>
<span data-ttu-id="be490-173">Specifica il server dei nomi per un record del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="be490-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-174">-Porta</span><span class="sxs-lookup"><span data-stu-id="be490-174">-Port</span></span>
<span data-ttu-id="be490-175">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="be490-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-176">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="be490-176">-Preference</span></span>
<span data-ttu-id="be490-177">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="be490-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-178">-Priorità</span><span class="sxs-lookup"><span data-stu-id="be490-178">-Priority</span></span>
<span data-ttu-id="be490-179">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="be490-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="be490-180">-Ptrdname</span></span>
<span data-ttu-id="be490-181">Specifica il nome di dominio di destinazione di un record puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="be490-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="be490-182">-RecordSet</span></span>
<span data-ttu-id="be490-183">Specifica l'oggetto **Recordset** che contiene il record da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="be490-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-184">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="be490-184">-Target</span></span>
<span data-ttu-id="be490-185">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="be490-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-186">-Valore</span><span class="sxs-lookup"><span data-stu-id="be490-186">-Value</span></span>
<span data-ttu-id="be490-187">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="be490-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-188">-Peso</span><span class="sxs-lookup"><span data-stu-id="be490-188">-Weight</span></span>
<span data-ttu-id="be490-189">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="be490-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be490-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be490-190">CommonParameters</span></span>
<span data-ttu-id="be490-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be490-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be490-192">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be490-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be490-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be490-193">INPUTS</span></span>

### <span data-ttu-id="be490-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be490-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="be490-195">Puoi reindirizzare un oggetto **DnsRecordSet** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be490-195">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="be490-196">Si tratta di una rappresentazione offline del set di record e gli aggiornamenti non cambiano le risposte DNS fino a quando non si esegue set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="be490-196">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="be490-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be490-197">OUTPUTS</span></span>

### <span data-ttu-id="be490-198">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be490-198">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="be490-199">Questo cmdlet restituisce l'oggetto **Recordset** modificato.</span><span class="sxs-lookup"><span data-stu-id="be490-199">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="be490-200">Note</span><span class="sxs-lookup"><span data-stu-id="be490-200">NOTES</span></span>

## <span data-ttu-id="be490-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be490-201">RELATED LINKS</span></span>

[<span data-ttu-id="be490-202">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="be490-202">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="be490-203">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be490-203">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="be490-204">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="be490-204">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
