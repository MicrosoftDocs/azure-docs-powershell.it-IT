---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196350"
---
# <span data-ttu-id="ef871-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef871-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="ef871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef871-102">SYNOPSIS</span></span>
<span data-ttu-id="ef871-103">Ottiene un set di record DNS.</span><span class="sxs-lookup"><span data-stu-id="ef871-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="ef871-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef871-104">SYNTAX</span></span>

### <span data-ttu-id="ef871-105">Campi</span><span class="sxs-lookup"><span data-stu-id="ef871-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef871-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ef871-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef871-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef871-107">DESCRIPTION</span></span>
<span data-ttu-id="ef871-108">Il cmdlet **Get-AzDnsRecordSet** ottiene il set di record DNS (Domain Name System) con il nome e il tipo specificati nell'area specificata.</span><span class="sxs-lookup"><span data-stu-id="ef871-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="ef871-109">Se non si specificano i parametri *Name* o *RecordType,* questo cmdlet restituisce tutti i set di record del tipo specificato nell'area.</span><span class="sxs-lookup"><span data-stu-id="ef871-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="ef871-110">Se si specifica il *parametro RecordType* ma non il *parametro Name,* questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="ef871-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="ef871-111">È possibile usare l'operatore della pipeline per passare un oggetto **DnsZone** a questo cmdlet oppure passare un oggetto **DnsZone** come parametro *Zone* oppure, in alternativa, è possibile specificare l'area e il gruppo di risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ef871-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="ef871-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef871-112">EXAMPLES</span></span>

### <span data-ttu-id="ef871-113">Esempio 1: Ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="ef871-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="ef871-114">Questo comando recupera il set di record di tipo A denominato www nel gruppo di risorse e nell'area specificati e quindi lo archivia nella $RecordSet variabile.</span><span class="sxs-lookup"><span data-stu-id="ef871-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ef871-115">Poiché sono *specificati i* parametri Name e *RecordType,* viene restituito un solo **oggetto RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="ef871-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="ef871-116">Esempio 2: Ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="ef871-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="ef871-117">Questo comando recupera una matrice di tutti i set di record di tipo A nell'area denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella variabile $RecordSets variabile.</span><span class="sxs-lookup"><span data-stu-id="ef871-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ef871-118">Esempio 3: Ottenere tutti i set di record in un'area</span><span class="sxs-lookup"><span data-stu-id="ef871-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="ef871-119">Questo comando recupera una matrice di tutti i set di record nell'area denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella variabile $RecordSets locale.</span><span class="sxs-lookup"><span data-stu-id="ef871-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ef871-120">Esempio 4: Ottenere tutti i set di record in un'area, usando un oggetto DnsZone</span><span class="sxs-lookup"><span data-stu-id="ef871-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="ef871-121">Questo esempio equivale all'esempio 3 riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="ef871-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="ef871-122">Questa volta, il fuso viene specificato usando un oggetto zona.</span><span class="sxs-lookup"><span data-stu-id="ef871-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="ef871-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef871-123">PARAMETERS</span></span>

### <span data-ttu-id="ef871-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef871-124">-DefaultProfile</span></span>
<span data-ttu-id="ef871-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ef871-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef871-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ef871-126">-Name</span></span>
<span data-ttu-id="ef871-127">Specifica il nome del **recordSet** da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ef871-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="ef871-128">Se non si specifica il parametro *Name,* vengono restituiti tutti i set di record del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="ef871-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef871-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ef871-129">-RecordType</span></span>
<span data-ttu-id="ef871-130">Specifica il tipo di record DNS che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef871-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="ef871-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ef871-131">Valid values are:</span></span> 
- <span data-ttu-id="ef871-132">A</span><span class="sxs-lookup"><span data-stu-id="ef871-132">A</span></span>
- <span data-ttu-id="ef871-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="ef871-133">AAAA</span></span>
- <span data-ttu-id="ef871-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="ef871-134">CNAME</span></span>
- <span data-ttu-id="ef871-135">MX</span><span class="sxs-lookup"><span data-stu-id="ef871-135">MX</span></span>
- <span data-ttu-id="ef871-136">NS</span><span class="sxs-lookup"><span data-stu-id="ef871-136">NS</span></span>
- <span data-ttu-id="ef871-137">PTR</span><span class="sxs-lookup"><span data-stu-id="ef871-137">PTR</span></span>
- <span data-ttu-id="ef871-138">SOA</span><span class="sxs-lookup"><span data-stu-id="ef871-138">SOA</span></span>
- <span data-ttu-id="ef871-139">SRV</span><span class="sxs-lookup"><span data-stu-id="ef871-139">SRV</span></span>
- <span data-ttu-id="ef871-140">TXT Se non si specifica il *parametro RecordType,* è necessario omettere *anche il parametro Name.*</span><span class="sxs-lookup"><span data-stu-id="ef871-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="ef871-141">Questo cmdlet restituisce quindi tutti i set di record nell'area (di tutti i nomi e i tipi).</span><span class="sxs-lookup"><span data-stu-id="ef871-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef871-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef871-142">-ResourceGroupName</span></span>
<span data-ttu-id="ef871-143">Specifica il gruppo di risorse che contiene l'area DNS.</span><span class="sxs-lookup"><span data-stu-id="ef871-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="ef871-144">È necessario specificare anche il nome dell'area, usando il *parametro ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="ef871-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="ef871-145">In alternativa, è possibile specificare l'area e il gruppo di risorse passando un **oggetto DnsZone** usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="ef871-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef871-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="ef871-146">-Zone</span></span>
<span data-ttu-id="ef871-147">Specifica l'area DNS che contiene il set di record che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef871-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="ef871-148">In alternativa, è possibile specificare l'area usando *i parametri ZoneName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ef871-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef871-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ef871-149">-ZoneName</span></span>
<span data-ttu-id="ef871-150">Specifica il nome dell'area DNS che contiene il set di record da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ef871-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="ef871-151">È necessario specificare anche il gruppo di risorse che contiene l'area, usando il *parametro ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="ef871-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ef871-152">In alternativa, è possibile specificare l'area e il gruppo di risorse passando un oggetto Dns Zone usando il *parametro Zone.*</span><span class="sxs-lookup"><span data-stu-id="ef871-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef871-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef871-153">CommonParameters</span></span>
<span data-ttu-id="ef871-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef871-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef871-155">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef871-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef871-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef871-156">INPUTS</span></span>

### <span data-ttu-id="ef871-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ef871-157">System.String</span></span>

### <span data-ttu-id="ef871-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="ef871-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="ef871-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ef871-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ef871-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef871-160">OUTPUTS</span></span>

### <span data-ttu-id="ef871-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef871-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ef871-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef871-162">NOTES</span></span>

## <span data-ttu-id="ef871-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef871-163">RELATED LINKS</span></span>

[<span data-ttu-id="ef871-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef871-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="ef871-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef871-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="ef871-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ef871-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


