---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: c85cc0b4ad60529cc57becb9ca864751d90a37c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984800"
---
# <span data-ttu-id="d5716-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d5716-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="d5716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5716-102">SYNOPSIS</span></span>
<span data-ttu-id="d5716-103">Crea un nuovo oggetto locale del record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="d5716-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5716-104">SYNTAX</span></span>

### <span data-ttu-id="d5716-105">A</span><span class="sxs-lookup"><span data-stu-id="d5716-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="d5716-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-107">Ns</span><span class="sxs-lookup"><span data-stu-id="d5716-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-108">Mx</span><span class="sxs-lookup"><span data-stu-id="d5716-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5716-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="d5716-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-110">Txt</span><span class="sxs-lookup"><span data-stu-id="d5716-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-111">Srv</span><span class="sxs-lookup"><span data-stu-id="d5716-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-112">CName</span><span class="sxs-lookup"><span data-stu-id="d5716-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5716-113">Caa</span><span class="sxs-lookup"><span data-stu-id="d5716-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5716-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5716-114">DESCRIPTION</span></span>
<span data-ttu-id="d5716-115">Il cmdlet **New-AzDnsRecordConfig crea** un **oggetto DnsRecord** locale.</span><span class="sxs-lookup"><span data-stu-id="d5716-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="d5716-116">Una matrice di questi oggetti viene passata al cmdlet New-AzDnsRecordSet usando il parametro *DnsRecords* per specificare i record da creare nel set di record.</span><span class="sxs-lookup"><span data-stu-id="d5716-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="d5716-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5716-117">EXAMPLES</span></span>

### <span data-ttu-id="d5716-118">Esempio 1: Creare un recordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="d5716-118">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-119">In questo esempio viene **creato un recordSet** denominato www nell'myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-120">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-121">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="d5716-122">Esempio 2: Creare un recordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="d5716-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-123">In questo esempio viene **creato un recordSet** denominato www nell'myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-124">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-125">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-125">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-126">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-127">Esempio 3: Creare un recordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="d5716-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-128">In questo esempio viene **creato un recordSet** denominato www nell'myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-129">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-130">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-130">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-131">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-132">Esempio 4: Creare un recordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="d5716-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-133">Questo comando crea un **recordSet** denominato www nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-134">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-135">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-135">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-136">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-137">Esempio 5: Creare un recordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="d5716-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-138">Questo comando crea un **recordSet** denominato ns1 nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-139">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-140">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-140">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-141">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-142">Esempio 6: Creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="d5716-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="d5716-143">Questo comando crea un **recordSet** denominato 4 nell'3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="d5716-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="d5716-144">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-145">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-145">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-146">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-147">Esempio 7: Creare un recordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="d5716-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-148">Questo comando crea un **recordSet** denominato _sip._tcp nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-149">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-150">Contiene un singolo record DNS che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="d5716-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="d5716-151">Il servizio (sip) e il protocollo (tcp) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="d5716-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="d5716-152">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="d5716-153">Esempio 8: Creare un recordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="d5716-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="d5716-154">Questo comando crea un **recordSet** denominato testo nell'area myzone.com.</span><span class="sxs-lookup"><span data-stu-id="d5716-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="d5716-155">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="d5716-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="d5716-156">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="d5716-156">It contains a single DNS record.</span></span>
<span data-ttu-id="d5716-157">Per creare un **record RecordSet** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="d5716-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="d5716-158">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5716-158">PARAMETERS</span></span>

### <span data-ttu-id="d5716-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="d5716-159">-CaaFlags</span></span>
<span data-ttu-id="d5716-160">Contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d5716-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="d5716-161">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="d5716-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="d5716-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="d5716-162">-CaaTag</span></span>
<span data-ttu-id="d5716-163">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d5716-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="d5716-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="d5716-164">-CaaValue</span></span>
<span data-ttu-id="d5716-165">Campo valore del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d5716-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="d5716-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="d5716-166">-Cname</span></span>
<span data-ttu-id="d5716-167">Specifica il nome di dominio per un record CNAME (Canonical Name).</span><span class="sxs-lookup"><span data-stu-id="d5716-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5716-168">-DefaultProfile</span></span>
<span data-ttu-id="d5716-169">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d5716-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5716-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d5716-170">-Exchange</span></span>
<span data-ttu-id="d5716-171">Specifica il nome del server Mail Exchange per un record MX (Mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="d5716-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="d5716-172">-Ipv4Address</span></span>
<span data-ttu-id="d5716-173">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="d5716-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="d5716-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="d5716-174">-Ipv6Address</span></span>
<span data-ttu-id="d5716-175">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="d5716-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="d5716-176">-Nsdname</span></span>
<span data-ttu-id="d5716-177">Specifica il nome del server dei nomi per un record del server dei nomi (NS).</span><span class="sxs-lookup"><span data-stu-id="d5716-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-178">-Port</span><span class="sxs-lookup"><span data-stu-id="d5716-178">-Port</span></span>
<span data-ttu-id="d5716-179">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="d5716-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-180">-Preference</span><span class="sxs-lookup"><span data-stu-id="d5716-180">-Preference</span></span>
<span data-ttu-id="d5716-181">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="d5716-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="d5716-182">-Priority</span></span>
<span data-ttu-id="d5716-183">Specifica la priorità di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="d5716-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="d5716-184">-Ptrdname</span></span>
<span data-ttu-id="d5716-185">Specifica il nome di dominio di destinazione di un record PTR (Pointer Resource).</span><span class="sxs-lookup"><span data-stu-id="d5716-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-186">-Target</span><span class="sxs-lookup"><span data-stu-id="d5716-186">-Target</span></span>
<span data-ttu-id="d5716-187">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="d5716-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-188">-Value</span><span class="sxs-lookup"><span data-stu-id="d5716-188">-Value</span></span>
<span data-ttu-id="d5716-189">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="d5716-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-190">-Spessore</span><span class="sxs-lookup"><span data-stu-id="d5716-190">-Weight</span></span>
<span data-ttu-id="d5716-191">Specifica il peso di un record SRV.</span><span class="sxs-lookup"><span data-stu-id="d5716-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5716-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5716-192">CommonParameters</span></span>
<span data-ttu-id="d5716-193">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5716-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5716-194">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5716-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5716-195">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5716-195">INPUTS</span></span>

### <span data-ttu-id="d5716-196">System.String</span><span class="sxs-lookup"><span data-stu-id="d5716-196">System.String</span></span>

### <span data-ttu-id="d5716-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="d5716-197">System.UInt16</span></span>

### <span data-ttu-id="d5716-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="d5716-198">System.Byte</span></span>

## <span data-ttu-id="d5716-199">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5716-199">OUTPUTS</span></span>

### <span data-ttu-id="d5716-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="d5716-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="d5716-201">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5716-201">NOTES</span></span>

## <span data-ttu-id="d5716-202">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5716-202">RELATED LINKS</span></span>

[<span data-ttu-id="d5716-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d5716-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="d5716-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d5716-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="d5716-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="d5716-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
