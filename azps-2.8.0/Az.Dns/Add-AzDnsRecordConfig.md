---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: ebf4efd627b904216cce239ccfee48f7ef97e35f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674519"
---
# <span data-ttu-id="2610b-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2610b-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="2610b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2610b-102">SYNOPSIS</span></span>
<span data-ttu-id="2610b-103">Aggiunge un record DNS a un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="2610b-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="2610b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2610b-104">SYNTAX</span></span>

### <span data-ttu-id="2610b-105">Un</span><span class="sxs-lookup"><span data-stu-id="2610b-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2610b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="2610b-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2610b-107">NS</span><span class="sxs-lookup"><span data-stu-id="2610b-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2610b-108">MX</span><span class="sxs-lookup"><span data-stu-id="2610b-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2610b-109">PTR</span><span class="sxs-lookup"><span data-stu-id="2610b-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2610b-110">TXT</span><span class="sxs-lookup"><span data-stu-id="2610b-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2610b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="2610b-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2610b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="2610b-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2610b-113">CAA</span><span class="sxs-lookup"><span data-stu-id="2610b-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2610b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2610b-114">DESCRIPTION</span></span>
<span data-ttu-id="2610b-115">Il cmdlet **Add-AzDnsRecordConfig** aggiunge un record DNS (Domain Name System) a un oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2610b-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="2610b-116">L'oggetto **Recordset** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non viene eseguito il cmdlet Set-AzDnsRecordSet per rendere persistente la modifica al servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2610b-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="2610b-117">I record SOA vengono creati quando viene creata una zona DNS e vengono rimossi quando viene eliminata la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="2610b-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="2610b-118">Non è possibile aggiungere o rimuovere record SOA, ma è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="2610b-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="2610b-119">Puoi passare l'oggetto **Recordset** a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2610b-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="2610b-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2610b-120">EXAMPLES</span></span>

### <span data-ttu-id="2610b-121">Esempio 1: aggiungere un record a in un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-122">Questo esempio aggiunge un record a a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="2610b-123">Esempio 2: aggiungere un record AAAA a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-124">Questo esempio aggiunge un record AAAA a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="2610b-125">Esempio 3: aggiungere un record CNAME a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-126">Questo esempio aggiunge un record CNAME a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="2610b-127">Dato che un set di record CNAME può contenere al massimo un record, deve essere inizialmente un set di record vuoto o i record esistenti devono essere rimossi usando Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="2610b-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="2610b-128">Esempio 4: aggiungere un record MX a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-129">Questo esempio aggiunge un record MX a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="2610b-130">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="2610b-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="2610b-131">Esempio 5: aggiungere un record NS a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-132">Questo esempio aggiunge un record NS a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="2610b-133">Esempio 6: aggiungere un record PTR a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-134">Questo esempio aggiunge un record PTR a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="2610b-135">Esempio 7: aggiungere un record SRV a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-136">Questo esempio aggiunge un record SRV a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="2610b-137">Esempio 8: aggiungere un record TXT a un set di record</span><span class="sxs-lookup"><span data-stu-id="2610b-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="2610b-138">Questo esempio aggiunge un record TXT a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="2610b-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="2610b-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2610b-139">PARAMETERS</span></span>

### <span data-ttu-id="2610b-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="2610b-140">-CaaFlags</span></span>
<span data-ttu-id="2610b-141">I contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="2610b-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="2610b-142">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="2610b-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="2610b-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="2610b-143">-CaaTag</span></span>
<span data-ttu-id="2610b-144">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="2610b-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="2610b-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="2610b-145">-CaaValue</span></span>
<span data-ttu-id="2610b-146">Campo valore per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="2610b-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="2610b-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="2610b-147">-Cname</span></span>
<span data-ttu-id="2610b-148">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="2610b-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="2610b-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2610b-149">-DefaultProfile</span></span>
<span data-ttu-id="2610b-150">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2610b-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2610b-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="2610b-151">-Exchange</span></span>
<span data-ttu-id="2610b-152">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="2610b-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="2610b-153">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="2610b-153">-Ipv4Address</span></span>
<span data-ttu-id="2610b-154">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="2610b-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="2610b-155">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="2610b-155">-Ipv6Address</span></span>
<span data-ttu-id="2610b-156">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="2610b-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="2610b-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="2610b-157">-Nsdname</span></span>
<span data-ttu-id="2610b-158">Specifica il nome del server dei nomi per un record NS (Name Server).</span><span class="sxs-lookup"><span data-stu-id="2610b-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="2610b-159">-Porta</span><span class="sxs-lookup"><span data-stu-id="2610b-159">-Port</span></span>
<span data-ttu-id="2610b-160">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="2610b-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="2610b-161">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="2610b-161">-Preference</span></span>
<span data-ttu-id="2610b-162">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="2610b-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="2610b-163">-Priorità</span><span class="sxs-lookup"><span data-stu-id="2610b-163">-Priority</span></span>
<span data-ttu-id="2610b-164">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="2610b-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="2610b-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="2610b-165">-Ptrdname</span></span>
<span data-ttu-id="2610b-166">Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="2610b-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="2610b-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2610b-167">-RecordSet</span></span>
<span data-ttu-id="2610b-168">Specifica l'oggetto **Recordset** da modificare.</span><span class="sxs-lookup"><span data-stu-id="2610b-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="2610b-169">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="2610b-169">-Target</span></span>
<span data-ttu-id="2610b-170">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="2610b-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="2610b-171">-Valore</span><span class="sxs-lookup"><span data-stu-id="2610b-171">-Value</span></span>
<span data-ttu-id="2610b-172">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="2610b-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="2610b-173">-Peso</span><span class="sxs-lookup"><span data-stu-id="2610b-173">-Weight</span></span>
<span data-ttu-id="2610b-174">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="2610b-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="2610b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2610b-175">CommonParameters</span></span>
<span data-ttu-id="2610b-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2610b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2610b-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2610b-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2610b-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2610b-178">INPUTS</span></span>

### <span data-ttu-id="2610b-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2610b-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="2610b-180">System. String</span><span class="sxs-lookup"><span data-stu-id="2610b-180">System.String</span></span>

### <span data-ttu-id="2610b-181">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="2610b-181">System.UInt16</span></span>

### <span data-ttu-id="2610b-182">System. byte</span><span class="sxs-lookup"><span data-stu-id="2610b-182">System.Byte</span></span>

## <span data-ttu-id="2610b-183">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2610b-183">OUTPUTS</span></span>

### <span data-ttu-id="2610b-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2610b-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="2610b-185">Note</span><span class="sxs-lookup"><span data-stu-id="2610b-185">NOTES</span></span>

## <span data-ttu-id="2610b-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2610b-186">RELATED LINKS</span></span>

[<span data-ttu-id="2610b-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2610b-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="2610b-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="2610b-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="2610b-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2610b-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)