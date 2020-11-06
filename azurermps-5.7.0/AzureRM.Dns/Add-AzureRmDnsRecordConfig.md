---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: c9e824160b04b183414c6b99fce4b09b6d70766a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511184"
---
# <span data-ttu-id="f27ce-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f27ce-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="f27ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f27ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f27ce-103">Aggiunge un record DNS a un oggetto set di record locale.</span><span class="sxs-lookup"><span data-stu-id="f27ce-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f27ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f27ce-104">SYNTAX</span></span>

### <span data-ttu-id="f27ce-105">Un</span><span class="sxs-lookup"><span data-stu-id="f27ce-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f27ce-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-107">NS</span><span class="sxs-lookup"><span data-stu-id="f27ce-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-108">MX</span><span class="sxs-lookup"><span data-stu-id="f27ce-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-109">PTR</span><span class="sxs-lookup"><span data-stu-id="f27ce-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-110">TXT</span><span class="sxs-lookup"><span data-stu-id="f27ce-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f27ce-111">SRV</span><span class="sxs-lookup"><span data-stu-id="f27ce-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f27ce-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="f27ce-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f27ce-113">CAA</span><span class="sxs-lookup"><span data-stu-id="f27ce-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f27ce-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f27ce-114">DESCRIPTION</span></span>
<span data-ttu-id="f27ce-115">Il cmdlet **Add-AzureRmDnsRecordConfig** aggiunge un record DNS (Domain Name System) a un oggetto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f27ce-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="f27ce-116">L'oggetto **Recordset** è un oggetto offline e le modifiche apportate non modificano le risposte DNS finché non viene eseguito il cmdlet Set-AzureRmDnsRecordSet per rendere persistente la modifica al servizio DNS di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f27ce-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="f27ce-117">I record SOA vengono creati quando viene creata una zona DNS e vengono rimossi quando viene eliminata la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="f27ce-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="f27ce-118">Non è possibile aggiungere o rimuovere record SOA, ma è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="f27ce-118">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="f27ce-119">Puoi passare l'oggetto **Recordset** a questo cmdlet come parametro o usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="f27ce-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f27ce-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f27ce-120">EXAMPLES</span></span>

### <span data-ttu-id="f27ce-121">Esempio 1: aggiungere un record a in un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-122">Questo esempio aggiunge un record a a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="f27ce-123">Esempio 2: aggiungere un record AAAA a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-124">Questo esempio aggiunge un record AAAA a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="f27ce-125">Esempio 3: aggiungere un record CNAME a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-126">Questo esempio aggiunge un record CNAME a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="f27ce-127">Dato che un set di record CNAME può contenere al massimo un record, deve essere inizialmente un set di record vuoto o i record esistenti devono essere rimossi usando Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="f27ce-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="f27ce-128">Esempio 4: aggiungere un record MX a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-129">Questo esempio aggiunge un record MX a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="f27ce-130">Il nome record "@" indica un set di record nella zona Apex.</span><span class="sxs-lookup"><span data-stu-id="f27ce-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="f27ce-131">Esempio 5: aggiungere un record NS a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-132">Questo esempio aggiunge un record NS a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="f27ce-133">Esempio 6: aggiungere un record PTR a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-134">Questo esempio aggiunge un record PTR a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="f27ce-135">Esempio 7: aggiungere un record SRV a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-136">Questo esempio aggiunge un record SRV a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="f27ce-137">Esempio 8: aggiungere un record TXT a un set di record</span><span class="sxs-lookup"><span data-stu-id="f27ce-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="f27ce-138">Questo esempio aggiunge un record TXT a un set di record esistente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="f27ce-139">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f27ce-139">PARAMETERS</span></span>

### <span data-ttu-id="f27ce-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="f27ce-140">-CaaFlags</span></span>
<span data-ttu-id="f27ce-141">I contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f27ce-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="f27ce-142">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="f27ce-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="f27ce-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="f27ce-143">-CaaTag</span></span>
<span data-ttu-id="f27ce-144">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f27ce-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="f27ce-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="f27ce-145">-CaaValue</span></span>
<span data-ttu-id="f27ce-146">Campo valore per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f27ce-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="f27ce-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f27ce-147">-Cname</span></span>
<span data-ttu-id="f27ce-148">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="f27ce-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="f27ce-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27ce-149">-DefaultProfile</span></span>
<span data-ttu-id="f27ce-150">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f27ce-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f27ce-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f27ce-151">-Exchange</span></span>
<span data-ttu-id="f27ce-152">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="f27ce-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="f27ce-153">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="f27ce-153">-Ipv4Address</span></span>
<span data-ttu-id="f27ce-154">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="f27ce-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="f27ce-155">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="f27ce-155">-Ipv6Address</span></span>
<span data-ttu-id="f27ce-156">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="f27ce-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="f27ce-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="f27ce-157">-Nsdname</span></span>
<span data-ttu-id="f27ce-158">Specifica il nome del server dei nomi per un record NS (Name Server).</span><span class="sxs-lookup"><span data-stu-id="f27ce-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="f27ce-159">-Porta</span><span class="sxs-lookup"><span data-stu-id="f27ce-159">-Port</span></span>
<span data-ttu-id="f27ce-160">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="f27ce-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="f27ce-161">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="f27ce-161">-Preference</span></span>
<span data-ttu-id="f27ce-162">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="f27ce-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="f27ce-163">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f27ce-163">-Priority</span></span>
<span data-ttu-id="f27ce-164">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f27ce-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="f27ce-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f27ce-165">-Ptrdname</span></span>
<span data-ttu-id="f27ce-166">Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="f27ce-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="f27ce-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f27ce-167">-RecordSet</span></span>
<span data-ttu-id="f27ce-168">Specifica l'oggetto **Recordset** da modificare.</span><span class="sxs-lookup"><span data-stu-id="f27ce-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="f27ce-169">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="f27ce-169">-Target</span></span>
<span data-ttu-id="f27ce-170">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f27ce-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="f27ce-171">-Valore</span><span class="sxs-lookup"><span data-stu-id="f27ce-171">-Value</span></span>
<span data-ttu-id="f27ce-172">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="f27ce-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="f27ce-173">-Peso</span><span class="sxs-lookup"><span data-stu-id="f27ce-173">-Weight</span></span>
<span data-ttu-id="f27ce-174">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="f27ce-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="f27ce-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27ce-175">CommonParameters</span></span>
<span data-ttu-id="f27ce-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27ce-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27ce-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27ce-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27ce-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f27ce-178">INPUTS</span></span>

### <span data-ttu-id="f27ce-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f27ce-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f27ce-180">È possibile reindirizzare un oggetto **Recordset** a questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f27ce-180">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="f27ce-181">Si tratta di una rappresentazione offline del **Recordset** e le modifiche apportate non modificano le risposte DNS finché non si esegue il cmdlet Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f27ce-181">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="f27ce-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f27ce-182">OUTPUTS</span></span>

### <span data-ttu-id="f27ce-183">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f27ce-183">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="f27ce-184">Questo cmdlet restituisce l'oggetto **Recordset** modificato.</span><span class="sxs-lookup"><span data-stu-id="f27ce-184">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="f27ce-185">Inoltre, l'oggetto passato viene modificato direttamente.</span><span class="sxs-lookup"><span data-stu-id="f27ce-185">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="f27ce-186">Note</span><span class="sxs-lookup"><span data-stu-id="f27ce-186">NOTES</span></span>

## <span data-ttu-id="f27ce-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f27ce-187">RELATED LINKS</span></span>

[<span data-ttu-id="f27ce-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f27ce-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="f27ce-189">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f27ce-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="f27ce-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f27ce-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
