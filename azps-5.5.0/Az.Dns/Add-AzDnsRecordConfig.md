---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196359"
---
# <span data-ttu-id="22f55-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="22f55-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="22f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f55-102">SYNOPSIS</span></span>
<span data-ttu-id="22f55-103">Aggiunge un record DNS a un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="22f55-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="22f55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22f55-104">SYNTAX</span></span>

### <span data-ttu-id="22f55-105">A</span><span class="sxs-lookup"><span data-stu-id="22f55-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22f55-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="22f55-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22f55-107">NS</span><span class="sxs-lookup"><span data-stu-id="22f55-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22f55-108">MX</span><span class="sxs-lookup"><span data-stu-id="22f55-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22f55-109">PTR</span><span class="sxs-lookup"><span data-stu-id="22f55-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22f55-110">TXT</span><span class="sxs-lookup"><span data-stu-id="22f55-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22f55-111">SRV</span><span class="sxs-lookup"><span data-stu-id="22f55-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22f55-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="22f55-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22f55-113">Caa</span><span class="sxs-lookup"><span data-stu-id="22f55-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22f55-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22f55-114">DESCRIPTION</span></span>
<span data-ttu-id="22f55-115">Il cmdlet **Add-AzDnsRecordConfig aggiunge** un record DNS (Domain Name System) a un **oggetto RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="22f55-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="22f55-116">**L'oggetto RecordSet** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non si esegue il cmdlet Set-AzDnsRecordSet per mantenere la modifica nel servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="22f55-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="22f55-117">I record SOA vengono creati al momento della creazione di un'area DNS e vengono rimossi quando l'area DNS viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="22f55-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="22f55-118">Non è possibile aggiungere o rimuovere record SOA, ma è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="22f55-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="22f55-119">È possibile passare **l'oggetto RecordSet** a questo cmdlet come parametro o usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="22f55-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="22f55-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22f55-120">EXAMPLES</span></span>

### <span data-ttu-id="22f55-121">Esempio 1: Aggiungere un record A a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-122">Questo esempio aggiunge un record A a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="22f55-123">Esempio 2: Aggiungere un record AAAA a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-124">Questo esempio aggiunge un record AAAA a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="22f55-125">Esempio 3: Aggiungere un record CNAME a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-126">Questo esempio aggiunge un record CNAME a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="22f55-127">Poiché un set di record CNAME può contenere al massimo un record, inizialmente deve essere un set di record vuoto o i record esistenti devono essere rimossi con Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="22f55-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="22f55-128">Esempio 4: Aggiungere un record MX a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-129">Questo esempio aggiunge un record MX a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="22f55-130">Il nome record "@" indica un set di record nell'apice della zona.</span><span class="sxs-lookup"><span data-stu-id="22f55-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="22f55-131">Esempio 5: Aggiungere un record NS a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-132">Questo esempio aggiunge un record NS a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="22f55-133">Esempio 6: Aggiungere un record PTR a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-134">Questo esempio aggiunge un record PTR a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="22f55-135">Esempio 7: Aggiungere un record SRV a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-136">Questo esempio aggiunge un record SRV a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="22f55-137">Esempio 8: Aggiungere un record TXT a un set di record</span><span class="sxs-lookup"><span data-stu-id="22f55-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="22f55-138">Questo esempio aggiunge un record TXT a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="22f55-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="22f55-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f55-139">PARAMETERS</span></span>

### <span data-ttu-id="22f55-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="22f55-140">-CaaFlags</span></span>
<span data-ttu-id="22f55-141">Contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="22f55-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="22f55-142">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="22f55-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="22f55-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="22f55-143">-CaaTag</span></span>
<span data-ttu-id="22f55-144">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="22f55-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="22f55-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="22f55-145">-CaaValue</span></span>
<span data-ttu-id="22f55-146">Campo valore del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="22f55-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="22f55-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="22f55-147">-Cname</span></span>
<span data-ttu-id="22f55-148">Specifica il nome di dominio per un record CNAME (Canonical Name).</span><span class="sxs-lookup"><span data-stu-id="22f55-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="22f55-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f55-149">-DefaultProfile</span></span>
<span data-ttu-id="22f55-150">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="22f55-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22f55-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="22f55-151">-Exchange</span></span>
<span data-ttu-id="22f55-152">Specifica il nome del server Mail Exchange per un record MX (Mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="22f55-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="22f55-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="22f55-153">-Ipv4Address</span></span>
<span data-ttu-id="22f55-154">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="22f55-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="22f55-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="22f55-155">-Ipv6Address</span></span>
<span data-ttu-id="22f55-156">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="22f55-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="22f55-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="22f55-157">-Nsdname</span></span>
<span data-ttu-id="22f55-158">Specifica il nome del server dei nomi per un record del server dei nomi( NS).</span><span class="sxs-lookup"><span data-stu-id="22f55-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="22f55-159">-Porta</span><span class="sxs-lookup"><span data-stu-id="22f55-159">-Port</span></span>
<span data-ttu-id="22f55-160">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="22f55-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="22f55-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="22f55-161">-Preference</span></span>
<span data-ttu-id="22f55-162">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="22f55-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="22f55-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="22f55-163">-Priority</span></span>
<span data-ttu-id="22f55-164">Specifica la priorità di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="22f55-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="22f55-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="22f55-165">-Ptrdname</span></span>
<span data-ttu-id="22f55-166">Specifica il nome di dominio di destinazione di un record PTR (Pointer Resource).</span><span class="sxs-lookup"><span data-stu-id="22f55-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="22f55-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="22f55-167">-RecordSet</span></span>
<span data-ttu-id="22f55-168">Specifica **l'oggetto RecordSet** da modificare.</span><span class="sxs-lookup"><span data-stu-id="22f55-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="22f55-169">-Target</span><span class="sxs-lookup"><span data-stu-id="22f55-169">-Target</span></span>
<span data-ttu-id="22f55-170">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="22f55-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="22f55-171">-Value</span><span class="sxs-lookup"><span data-stu-id="22f55-171">-Value</span></span>
<span data-ttu-id="22f55-172">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="22f55-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="22f55-173">-Spessore</span><span class="sxs-lookup"><span data-stu-id="22f55-173">-Weight</span></span>
<span data-ttu-id="22f55-174">Specifica il peso di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="22f55-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="22f55-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f55-175">CommonParameters</span></span>
<span data-ttu-id="22f55-176">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f55-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f55-177">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22f55-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f55-178">INPUT</span><span class="sxs-lookup"><span data-stu-id="22f55-178">INPUTS</span></span>

### <span data-ttu-id="22f55-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22f55-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="22f55-180">System.String</span><span class="sxs-lookup"><span data-stu-id="22f55-180">System.String</span></span>

### <span data-ttu-id="22f55-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="22f55-181">System.UInt16</span></span>

### <span data-ttu-id="22f55-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="22f55-182">System.Byte</span></span>

## <span data-ttu-id="22f55-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22f55-183">OUTPUTS</span></span>

### <span data-ttu-id="22f55-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22f55-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="22f55-185">NOTE</span><span class="sxs-lookup"><span data-stu-id="22f55-185">NOTES</span></span>

## <span data-ttu-id="22f55-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22f55-186">RELATED LINKS</span></span>

[<span data-ttu-id="22f55-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22f55-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="22f55-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="22f55-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="22f55-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="22f55-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
