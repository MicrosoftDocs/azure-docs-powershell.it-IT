---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f44472ac83c1d92baab5d4c7c3b4c8d325e3dfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519468"
---
# <span data-ttu-id="6df3a-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6df3a-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="6df3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6df3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6df3a-103">Crea un nuovo oggetto local record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6df3a-104">SYNTAX</span></span>

### <span data-ttu-id="6df3a-105">Un</span><span class="sxs-lookup"><span data-stu-id="6df3a-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6df3a-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="6df3a-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6df3a-107">NS</span><span class="sxs-lookup"><span data-stu-id="6df3a-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-108">MX</span><span class="sxs-lookup"><span data-stu-id="6df3a-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6df3a-109">PTR</span><span class="sxs-lookup"><span data-stu-id="6df3a-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-110">Txt</span><span class="sxs-lookup"><span data-stu-id="6df3a-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-111">SRV</span><span class="sxs-lookup"><span data-stu-id="6df3a-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-112">CName</span><span class="sxs-lookup"><span data-stu-id="6df3a-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df3a-113">CAA</span><span class="sxs-lookup"><span data-stu-id="6df3a-113">Caa</span></span>
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df3a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6df3a-114">DESCRIPTION</span></span>
<span data-ttu-id="6df3a-115">Il cmdlet **New-AzureRmDnsRecordConfig** crea un oggetto **DnsRecord** locale.</span><span class="sxs-lookup"><span data-stu-id="6df3a-115">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="6df3a-116">Una matrice di questi oggetti viene passata al cmdlet New-AzureRmDnsRecordSet usando il parametro *DnsRecords* per specificare i record da creare nel set di record.</span><span class="sxs-lookup"><span data-stu-id="6df3a-116">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="6df3a-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6df3a-117">EXAMPLES</span></span>

### <span data-ttu-id="6df3a-118">Esempio 1: creare un RecordSet di tipo A</span><span class="sxs-lookup"><span data-stu-id="6df3a-118">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-119">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-120">Il set di record è di tipo A e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-121">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="6df3a-122">Esempio 2: creare un RecordSet di tipo AAAA</span><span class="sxs-lookup"><span data-stu-id="6df3a-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-123">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-124">Il set di record è di tipo AAAA e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-125">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-125">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-126">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-127">Esempio 3: creare un RecordSet di tipo CNAME</span><span class="sxs-lookup"><span data-stu-id="6df3a-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-128">Questo esempio crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-129">Il set di record è di tipo CNAME e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-130">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-130">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-131">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-132">Esempio 4: creare un RecordSet di tipo MX</span><span class="sxs-lookup"><span data-stu-id="6df3a-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-133">Questo comando crea un **Recordset** denominato www nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-134">Il set di record è di tipo MX e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-135">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-135">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-136">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-137">Esempio 5: creare un RecordSet di tipo NS</span><span class="sxs-lookup"><span data-stu-id="6df3a-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-138">Questo comando crea un **Recordset** denominato NS1 nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-139">Il set di record è di tipo NS e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-140">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-140">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-141">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-142">Esempio 6: creare un RecordSet di tipo PTR</span><span class="sxs-lookup"><span data-stu-id="6df3a-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="6df3a-143">Questo comando crea un **Recordset** denominato 4 nella zona 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="6df3a-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="6df3a-144">Il set di record è di tipo PTR e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-145">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-145">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-146">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-147">Esempio 7: creare un RecordSet di tipo SRV</span><span class="sxs-lookup"><span data-stu-id="6df3a-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-148">Questo comando crea un **Recordset** denominato _sip. _tcp nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-149">Il set di record è di tipo SRV e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-150">Contiene un singolo record DNS, che punta all'indirizzo IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="6df3a-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="6df3a-151">Il servizio (SIP) e il protocollo (TCP) vengono specificati come parte del nome del set di record, non come parte dei dati del record.</span><span class="sxs-lookup"><span data-stu-id="6df3a-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="6df3a-152">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="6df3a-153">Esempio 8: creare un RecordSet di tipo TXT</span><span class="sxs-lookup"><span data-stu-id="6df3a-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="6df3a-154">Questo comando crea un **Recordset** denominato Text nella zona MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="6df3a-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="6df3a-155">Il set di record è di tipo TXT e ha un TTL di 1 ora (3600 secondi).</span><span class="sxs-lookup"><span data-stu-id="6df3a-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="6df3a-156">Contiene un singolo record DNS.</span><span class="sxs-lookup"><span data-stu-id="6df3a-156">It contains a single DNS record.</span></span>

<span data-ttu-id="6df3a-157">Per creare un **Recordset** usando una sola riga di pn_PowerShell_short oppure per creare un set di record con più record, vedere l'esempio 1.</span><span class="sxs-lookup"><span data-stu-id="6df3a-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="6df3a-158">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6df3a-158">PARAMETERS</span></span>

### <span data-ttu-id="6df3a-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="6df3a-159">-CaaFlags</span></span>
<span data-ttu-id="6df3a-160">I contrassegni per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6df3a-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="6df3a-161">Deve essere un numero compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="6df3a-161">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="6df3a-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="6df3a-162">-CaaTag</span></span>
<span data-ttu-id="6df3a-163">Campo tag del record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6df3a-163">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="6df3a-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="6df3a-164">-CaaValue</span></span>
<span data-ttu-id="6df3a-165">Campo valore per il record CAA da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="6df3a-165">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="6df3a-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="6df3a-166">-Cname</span></span>
<span data-ttu-id="6df3a-167">Specifica il nome di dominio per un record di nome canonico (CNAME).</span><span class="sxs-lookup"><span data-stu-id="6df3a-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df3a-168">-DefaultProfile</span></span>
<span data-ttu-id="6df3a-169">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6df3a-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6df3a-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6df3a-170">-Exchange</span></span>
<span data-ttu-id="6df3a-171">Specifica il nome del server di posta Exchange per un record MX (mail Exchange).</span><span class="sxs-lookup"><span data-stu-id="6df3a-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-172">-Indirizzoipv4</span><span class="sxs-lookup"><span data-stu-id="6df3a-172">-Ipv4Address</span></span>
<span data-ttu-id="6df3a-173">Specifica un indirizzo IPv4 per un record A.</span><span class="sxs-lookup"><span data-stu-id="6df3a-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="6df3a-174">-Indirizzoipv6</span><span class="sxs-lookup"><span data-stu-id="6df3a-174">-Ipv6Address</span></span>
<span data-ttu-id="6df3a-175">Specifica un indirizzo IPv6 per un record AAAA.</span><span class="sxs-lookup"><span data-stu-id="6df3a-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="6df3a-176">-Nsdname</span></span>
<span data-ttu-id="6df3a-177">Specifica il nome del server dei nomi per un record NS (Name Server).</span><span class="sxs-lookup"><span data-stu-id="6df3a-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-178">-Porta</span><span class="sxs-lookup"><span data-stu-id="6df3a-178">-Port</span></span>
<span data-ttu-id="6df3a-179">Specifica la porta per un record di servizio (SRV).</span><span class="sxs-lookup"><span data-stu-id="6df3a-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-180">-Preferenza</span><span class="sxs-lookup"><span data-stu-id="6df3a-180">-Preference</span></span>
<span data-ttu-id="6df3a-181">Specifica la preferenza per un record MX.</span><span class="sxs-lookup"><span data-stu-id="6df3a-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-182">-Priorità</span><span class="sxs-lookup"><span data-stu-id="6df3a-182">-Priority</span></span>
<span data-ttu-id="6df3a-183">Specifica la priorità per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="6df3a-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6df3a-184">-Ptrdname</span></span>
<span data-ttu-id="6df3a-185">Specifica il nome di dominio di destinazione di un record di risorsa puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="6df3a-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-186">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="6df3a-186">-Target</span></span>
<span data-ttu-id="6df3a-187">Specifica la destinazione per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="6df3a-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-188">-Valore</span><span class="sxs-lookup"><span data-stu-id="6df3a-188">-Value</span></span>
<span data-ttu-id="6df3a-189">Specifica il valore per un record TXT.</span><span class="sxs-lookup"><span data-stu-id="6df3a-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-190">-Peso</span><span class="sxs-lookup"><span data-stu-id="6df3a-190">-Weight</span></span>
<span data-ttu-id="6df3a-191">Specifica il peso per un record SRV.</span><span class="sxs-lookup"><span data-stu-id="6df3a-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df3a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df3a-192">CommonParameters</span></span>
<span data-ttu-id="6df3a-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df3a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df3a-194">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df3a-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df3a-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6df3a-195">INPUTS</span></span>

### <span data-ttu-id="6df3a-196">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="6df3a-196">None.</span></span>

## <span data-ttu-id="6df3a-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6df3a-197">OUTPUTS</span></span>

### <span data-ttu-id="6df3a-198">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="6df3a-198">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="6df3a-199">Note</span><span class="sxs-lookup"><span data-stu-id="6df3a-199">NOTES</span></span>

## <span data-ttu-id="6df3a-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6df3a-200">RELATED LINKS</span></span>

[<span data-ttu-id="6df3a-201">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6df3a-201">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="6df3a-202">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6df3a-202">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6df3a-203">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6df3a-203">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
