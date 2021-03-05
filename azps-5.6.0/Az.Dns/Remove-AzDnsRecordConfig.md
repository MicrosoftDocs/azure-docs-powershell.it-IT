---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: 07af143e1a1582670d15a15c356f673fef1f7590
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984785"
---
# <span data-ttu-id="67b80-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="67b80-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="67b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67b80-102">SYNOPSIS</span></span>
<span data-ttu-id="67b80-103">Rimuove un record DNS da un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="67b80-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="67b80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67b80-104">SYNTAX</span></span>

### <span data-ttu-id="67b80-105">A</span><span class="sxs-lookup"><span data-stu-id="67b80-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b80-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="67b80-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b80-107">NS</span><span class="sxs-lookup"><span data-stu-id="67b80-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b80-108">MX</span><span class="sxs-lookup"><span data-stu-id="67b80-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b80-109">PTR</span><span class="sxs-lookup"><span data-stu-id="67b80-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b80-110">TXT</span><span class="sxs-lookup"><span data-stu-id="67b80-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b80-111">SRV</span><span class="sxs-lookup"><span data-stu-id="67b80-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67b80-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="67b80-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67b80-113">Caa</span><span class="sxs-lookup"><span data-stu-id="67b80-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67b80-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67b80-114">DESCRIPTION</span></span>
<span data-ttu-id="67b80-115">Il cmdlet **Remove-AzDnsRecordConfig** rimuove un record DNS (Domain Name System) da un set di record.</span><span class="sxs-lookup"><span data-stu-id="67b80-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="67b80-116">L'oggetto **RecordSet** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non si esegue il cmdlet Set-AzDnsRecordSet per mantenere la modifica nel servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="67b80-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="67b80-117">Per rimuovere un record, tutti i campi di quel tipo di record devono corrispondere esattamente.</span><span class="sxs-lookup"><span data-stu-id="67b80-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="67b80-118">Non è possibile aggiungere o rimuovere record SOA.</span><span class="sxs-lookup"><span data-stu-id="67b80-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="67b80-119">I record SOA vengono creati automaticamente quando viene creata un'area DNS ed eliminata automaticamente quando l'area DNS viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="67b80-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="67b80-120">È possibile passare **l'oggetto RecordSet** a questo cmdlet come parametro o usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="67b80-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="67b80-121">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67b80-121">EXAMPLES</span></span>

### <span data-ttu-id="67b80-122">Esempio 1: Rimuovere un record A da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-123">Questo esempio rimuove un record A da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="67b80-124">Se questo è l'unico record del set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="67b80-125">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-126">Esempio 2: Rimuovere un record AAAA da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-127">Questo esempio rimuove un record AAAA da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="67b80-128">Se questo è l'unico record del set di record, il risultato sarà un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="67b80-129">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-130">Esempio 3: Rimuovere un record CNAME da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-131">Questo esempio rimuove un record CNAME da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="67b80-132">Poiché un set di record CNAME può contenere al massimo un record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="67b80-133">Esempio 4: Rimuovere un record MX da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-134">Questo esempio rimuove un record MX da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="67b80-135">Il nome record "@" indica un set di record nell'apice della zona.</span><span class="sxs-lookup"><span data-stu-id="67b80-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="67b80-136">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="67b80-137">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-138">Esempio 5: Rimuovere un record NS da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-139">Questo esempio rimuove un record NS da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="67b80-140">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="67b80-141">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-142">Esempio 6: Rimuovere un record PTR da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-143">Questo esempio rimuove un record PTR da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="67b80-144">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="67b80-145">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-146">Esempio 7: Rimuovere un record SRV da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-147">Questo esempio rimuove un record SRV da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="67b80-148">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="67b80-149">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="67b80-150">Esempio 8: Rimuovere un record TXT da un set di record</span><span class="sxs-lookup"><span data-stu-id="67b80-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="67b80-151">Questo esempio rimuove un record TXT da un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="67b80-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="67b80-152">Se questo è l'unico record del set di record, il risultato è un set di record vuoto.</span><span class="sxs-lookup"><span data-stu-id="67b80-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="67b80-153">Per rimuovere completamente un set di record, vedere Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="67b80-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="67b80-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67b80-154">PARAMETERS</span></span>

### <span data-ttu-id="67b80-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="67b80-155">-CaaFlags</span></span>
<span data-ttu-id="67b80-156">Contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="67b80-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="67b80-157">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="67b80-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="67b80-158">-CaaTag</span></span>
<span data-ttu-id="67b80-159">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="67b80-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="67b80-160">-CaaValue</span></span>
<span data-ttu-id="67b80-161">Campo valore del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="67b80-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="67b80-162">-Cname</span></span>
<span data-ttu-id="67b80-163">Specifica il nome di dominio per un record CNAME (Canonical Name).</span><span class="sxs-lookup"><span data-stu-id="67b80-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b80-164">-DefaultProfile</span></span>
<span data-ttu-id="67b80-165">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="67b80-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67b80-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="67b80-166">-Exchange</span></span>
<span data-ttu-id="67b80-167">Specifica il nome del server Mail Exchange per un record MX (Mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="67b80-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="67b80-168">-Ipv4Address</span></span>
<span data-ttu-id="67b80-169">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="67b80-169">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="67b80-170">-Ipv6Address</span></span>
<span data-ttu-id="67b80-171">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="67b80-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="67b80-172">-Nsdname</span></span>
<span data-ttu-id="67b80-173">Specifica il server dei nomi per un record del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="67b80-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-174">-Porta</span><span class="sxs-lookup"><span data-stu-id="67b80-174">-Port</span></span>
<span data-ttu-id="67b80-175">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="67b80-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-176">-Preference</span><span class="sxs-lookup"><span data-stu-id="67b80-176">-Preference</span></span>
<span data-ttu-id="67b80-177">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="67b80-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-178">-Priority</span><span class="sxs-lookup"><span data-stu-id="67b80-178">-Priority</span></span>
<span data-ttu-id="67b80-179">Specifica la priorità di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="67b80-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="67b80-180">-Ptrdname</span></span>
<span data-ttu-id="67b80-181">Specifica il nome di dominio di destinazione di un record puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="67b80-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="67b80-182">-RecordSet</span></span>
<span data-ttu-id="67b80-183">Specifica **l'oggetto RecordSet** che contiene il record da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="67b80-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-184">-Target</span><span class="sxs-lookup"><span data-stu-id="67b80-184">-Target</span></span>
<span data-ttu-id="67b80-185">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="67b80-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-186">-Value</span><span class="sxs-lookup"><span data-stu-id="67b80-186">-Value</span></span>
<span data-ttu-id="67b80-187">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="67b80-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-188">-Spessore</span><span class="sxs-lookup"><span data-stu-id="67b80-188">-Weight</span></span>
<span data-ttu-id="67b80-189">Specifica il peso di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="67b80-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b80-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b80-190">CommonParameters</span></span>
<span data-ttu-id="67b80-191">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b80-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b80-192">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b80-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b80-193">INPUT</span><span class="sxs-lookup"><span data-stu-id="67b80-193">INPUTS</span></span>

### <span data-ttu-id="67b80-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="67b80-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="67b80-195">System.String</span><span class="sxs-lookup"><span data-stu-id="67b80-195">System.String</span></span>

### <span data-ttu-id="67b80-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="67b80-196">System.UInt16</span></span>

### <span data-ttu-id="67b80-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="67b80-197">System.Byte</span></span>

## <span data-ttu-id="67b80-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67b80-198">OUTPUTS</span></span>

### <span data-ttu-id="67b80-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="67b80-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="67b80-200">NOTE</span><span class="sxs-lookup"><span data-stu-id="67b80-200">NOTES</span></span>

## <span data-ttu-id="67b80-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67b80-201">RELATED LINKS</span></span>

[<span data-ttu-id="67b80-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="67b80-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="67b80-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="67b80-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="67b80-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="67b80-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
