---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202135"
---
# <span data-ttu-id="ed8be-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ed8be-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ed8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8be-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8be-103">Ottiene un set di record da un'area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="ed8be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed8be-104">SYNTAX</span></span>

### <span data-ttu-id="ed8be-105">FieldsWithNoName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed8be-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8be-106">Campi</span><span class="sxs-lookup"><span data-stu-id="ed8be-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8be-107">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ed8be-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8be-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="ed8be-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8be-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8be-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8be-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="ed8be-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed8be-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed8be-111">DESCRIPTION</span></span>
<span data-ttu-id="ed8be-112">Il cmdlet Get-AzPrivateDnsRecordSet ottiene il set di record DNS (Domain Name System) privato con il nome e il tipo specificati nell'area privata specificata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="ed8be-113">Se non si specificano i parametri Name o RecordType, questo cmdlet restituisce tutti i set di record del tipo specificato nell'area privata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="ed8be-114">Se si specifica il parametro RecordType ma non il parametro Name, questo cmdlet restituisce tutti i set di record del tipo di record specificato.</span><span class="sxs-lookup"><span data-stu-id="ed8be-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="ed8be-115">È possibile usare l'operatore della pipeline per passare un oggetto PSPrivateDnsZone a questo cmdlet oppure passare un oggetto PSPrivateDnsZone come parametro Zone oppure, in alternativa, è possibile specificare l'area e il gruppo di risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ed8be-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="ed8be-116">È anche possibile specificare l'area privata usando l'ID risorsa dell'area privata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="ed8be-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed8be-117">EXAMPLES</span></span>

### <span data-ttu-id="ed8be-118">Esempio 1: Ottenere set di record con un nome e un tipo specificati</span><span class="sxs-lookup"><span data-stu-id="ed8be-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="ed8be-119">Questo comando recupera il set di record A denominato www nel gruppo di risorse e nell'area privata specificati e quindi lo archivia nella variabile $RecordSet locale.</span><span class="sxs-lookup"><span data-stu-id="ed8be-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ed8be-120">Poiché sono specificati i parametri Name e RecordType, viene restituito un solo oggetto RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ed8be-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="ed8be-121">Esempio 2: Ottenere set di record di un tipo specificato</span><span class="sxs-lookup"><span data-stu-id="ed8be-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="ed8be-122">Questo comando recupera una matrice di tutti i set di record di tipo A nell'area privata denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="ed8be-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ed8be-123">Esempio 3: Ottenere tutti i set di record in un'area privata</span><span class="sxs-lookup"><span data-stu-id="ed8be-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="ed8be-124">Questo comando recupera una matrice di tutti i set di record nell'area privata denominata myzone.com nel gruppo di risorse denominato MyResourceGroup e quindi li archivia nella variabile $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="ed8be-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ed8be-125">Esempio 4: Ottenere tutti i set di record in un'area privata, usando un oggetto PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ed8be-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="ed8be-126">Questo esempio equivale all'esempio 3 riportato sopra.</span><span class="sxs-lookup"><span data-stu-id="ed8be-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="ed8be-127">Questa volta l'area privata viene specificata usando un oggetto area privata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="ed8be-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed8be-128">PARAMETERS</span></span>

### <span data-ttu-id="ed8be-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8be-129">-DefaultProfile</span></span>
<span data-ttu-id="ed8be-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8be-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8be-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8be-131">-Name</span></span>
<span data-ttu-id="ed8be-132">Nome dei record in questo set di record (relativo al nome dell'area e senza punto di chiusura).</span><span class="sxs-lookup"><span data-stu-id="ed8be-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="ed8be-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8be-133">-ParentResourceId</span></span>
<span data-ttu-id="ed8be-134">ID Risorsa area DNS privata.</span><span class="sxs-lookup"><span data-stu-id="ed8be-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="ed8be-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ed8be-135">-RecordType</span></span>
<span data-ttu-id="ed8be-136">Tipo di record DNS in questo set di record.</span><span class="sxs-lookup"><span data-stu-id="ed8be-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="ed8be-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8be-137">-ResourceGroupName</span></span>
<span data-ttu-id="ed8be-138">Gruppo di risorse a cui appartiene l'area.</span><span class="sxs-lookup"><span data-stu-id="ed8be-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="ed8be-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="ed8be-139">-Zone</span></span>
<span data-ttu-id="ed8be-140">Oggetto DnsZone che rappresenta l'area in cui creare il set di record.</span><span class="sxs-lookup"><span data-stu-id="ed8be-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="ed8be-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ed8be-141">-ZoneName</span></span>
<span data-ttu-id="ed8be-142">Area in cui creare il set di record (senza punto di chiusura).</span><span class="sxs-lookup"><span data-stu-id="ed8be-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="ed8be-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8be-143">CommonParameters</span></span>
<span data-ttu-id="ed8be-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8be-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8be-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8be-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8be-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed8be-146">INPUTS</span></span>

### <span data-ttu-id="ed8be-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ed8be-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="ed8be-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ed8be-148">System.String</span></span>

## <span data-ttu-id="ed8be-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed8be-149">OUTPUTS</span></span>

### <span data-ttu-id="ed8be-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ed8be-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ed8be-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed8be-151">NOTES</span></span>

## <span data-ttu-id="ed8be-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed8be-152">RELATED LINKS</span></span>
