---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a0b527a0931c5c3423e5e64bad0abb7128fc3497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855910"
---
# <span data-ttu-id="e1ad1-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e1ad1-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="e1ad1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ad1-103">Ottiene un set di record da una zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="e1ad1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-104">SYNTAX</span></span>

### <span data-ttu-id="e1ad1-105">FieldsWithNoName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1ad1-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ad1-106">Campi</span><span class="sxs-lookup"><span data-stu-id="e1ad1-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ad1-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e1ad1-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ad1-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="e1ad1-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ad1-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1ad1-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ad1-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="e1ad1-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ad1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1ad1-111">DESCRIPTION</span></span>
<span data-ttu-id="e1ad1-112">Il cmdlet Get-AzPrivateDnsRecordSet ottiene il record DNS (private Domain Name System) impostato con il nome e il tipo specificati nell'area privata specificata.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="e1ad1-113">Se non specifichi i parametri Name o RecordType, questo cmdlet restituisce tutti i set di record del tipo specificato nell'area privata.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="e1ad1-114">Se specifichi il parametro RecordType ma non il parametro Name, questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="e1ad1-115">Puoi usare l'operatore pipeline per passare un oggetto PSPrivateDnsZone a questo cmdlet oppure puoi passare un oggetto PSPrivateDnsZone come parametro di zona o in alternativa puoi specificare il gruppo zona e risorsa per nome.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="e1ad1-116">È anche possibile specificare l'area privata usando l'ID risorsa dell'area privata.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="e1ad1-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-117">EXAMPLES</span></span>

### <span data-ttu-id="e1ad1-118">Esempio 1: ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="e1ad1-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="e1ad1-119">Questo comando ottiene il set di record del tipo di record un www denominato nel gruppo di risorse e nell'area privata specificati e lo archivia nella variabile $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="e1ad1-120">Poiché vengono specificati i parametri Name e RecordType, viene restituito un solo oggetto RecordSet.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="e1ad1-121">Esempio 2: ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="e1ad1-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e1ad1-122">Questo comando ottiene una matrice di tutti i set di record del tipo di record a nella zona privata denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e1ad1-123">Esempio 3: ottenere tutti i set di record in un'area privata</span><span class="sxs-lookup"><span data-stu-id="e1ad1-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e1ad1-124">Questo comando consente di ottenere una matrice di tutti i set di record nella zona privata denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi di archiviarli nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e1ad1-125">Esempio 4: ottenere tutti i set di record in un'area privata, usando un oggetto PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e1ad1-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="e1ad1-126">Questo esempio equivale all'esempio 3 precedente.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="e1ad1-127">Questa volta, l'area privata viene specificata usando un oggetto zone privato.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="e1ad1-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-128">PARAMETERS</span></span>

### <span data-ttu-id="e1ad1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ad1-129">-DefaultProfile</span></span>
<span data-ttu-id="e1ad1-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ad1-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1ad1-131">-Name</span></span>
<span data-ttu-id="e1ad1-132">Nome dei record nel set di record (relativo al nome della zona e senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="e1ad1-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e1ad1-133">-ParentResourceId</span></span>
<span data-ttu-id="e1ad1-134">Area DNS privata ResourceID.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="e1ad1-135">-RecordType</span></span>
<span data-ttu-id="e1ad1-136">Tipo di record DNS nel set di record.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ad1-137">-ResourceGroupName</span></span>
<span data-ttu-id="e1ad1-138">Il gruppo di risorse a cui appartiene la zona.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="e1ad1-139">-Zone</span></span>
<span data-ttu-id="e1ad1-140">Oggetto DnsZone che rappresenta la zona in cui creare il set di record.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-141">-Zonename</span><span class="sxs-lookup"><span data-stu-id="e1ad1-141">-ZoneName</span></span>
<span data-ttu-id="e1ad1-142">La zona in cui creare il record impostato (senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="e1ad1-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ad1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ad1-143">CommonParameters</span></span>
<span data-ttu-id="e1ad1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ad1-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ad1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ad1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-146">INPUTS</span></span>

### <span data-ttu-id="e1ad1-147">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e1ad1-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="e1ad1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ad1-148">System.String</span></span>

## <span data-ttu-id="e1ad1-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1ad1-149">OUTPUTS</span></span>

### <span data-ttu-id="e1ad1-150">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e1ad1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="e1ad1-151">Note</span><span class="sxs-lookup"><span data-stu-id="e1ad1-151">NOTES</span></span>

## <span data-ttu-id="e1ad1-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-152">RELATED LINKS</span></span>
