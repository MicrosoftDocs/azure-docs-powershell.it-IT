---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200935"
---
# <span data-ttu-id="759b0-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="759b0-101">New-AzDnsZone</span></span>

## <span data-ttu-id="759b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="759b0-102">SYNOPSIS</span></span>
<span data-ttu-id="759b0-103">Crea una nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="759b0-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="759b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="759b0-104">SYNTAX</span></span>

### <span data-ttu-id="759b0-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="759b0-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="759b0-106">Nomi</span><span class="sxs-lookup"><span data-stu-id="759b0-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="759b0-107">Oggetti</span><span class="sxs-lookup"><span data-stu-id="759b0-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="759b0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="759b0-108">DESCRIPTION</span></span>
<span data-ttu-id="759b0-109">Il cmdlet **New-AzDnsZone** crea una nuova area DNS (Domain Name System) nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="759b0-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="759b0-110">Devi specificare un nome di zona DNS univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="759b0-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="759b0-111">Dopo aver creato la zona, usare il cmdlet New-AzDnsRecordSet per creare set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="759b0-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="759b0-112">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="759b0-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="759b0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="759b0-113">EXAMPLES</span></span>

### <span data-ttu-id="759b0-114">Esempio 1: creare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="759b0-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="759b0-115">Questo comando crea una nuova zona DNS denominata myzone.com nel gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="759b0-116">Esempio 2: creare una zona DNS privata specificando gli ID di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="759b0-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="759b0-117">Questo comando crea una nuova zona DNS privata denominata myprivatezone.com nel gruppo di risorse specificato con una rete virtuale di risoluzione associata (specificando il relativo ID) e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="759b0-118">Esempio 3: creare una zona DNS privata specificando gli oggetti di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="759b0-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="759b0-119">Questo comando crea una nuova zona DNS privata denominata myprivatezone.com nel gruppo di risorse specificato con una rete virtuale di risoluzione associata (a cui fa riferimento la variabile $ResVirtualNetwork), quindi la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="759b0-120">Esempio 4: creare una zona DNS con delega specificando il nome della zona padre</span><span class="sxs-lookup"><span data-stu-id="759b0-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="759b0-121">Questo comando crea una nuova zona DNS figlio denominata mychild.zone.com nel gruppo di risorse specificato e archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="759b0-122">Viene inoltre aggiunta la delega nella zona DNS padre denominata zone.com che risiede nello stesso gruppo di abbonamenti e risorse dell'area figlio.</span><span class="sxs-lookup"><span data-stu-id="759b0-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="759b0-123">Esempio 5: creare una zona DNS con delega specificando l'ID zona padre</span><span class="sxs-lookup"><span data-stu-id="759b0-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="759b0-124">Questo comando crea una nuova zona DNS figlio denominata mychild.zone.com nel gruppo di risorse specificato e archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="759b0-125">La delega viene aggiunta anche nella zona DNS padre denominata zone.com nel gruppo di risorse altro-l'abbonamento fornito da RG è uguale a quello dell'area figlio creata.</span><span class="sxs-lookup"><span data-stu-id="759b0-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="759b0-126">Esempio 6: creare una zona DNS con delega specificando l'oggetto zona padre</span><span class="sxs-lookup"><span data-stu-id="759b0-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="759b0-127">Questo comando crea una nuova zona DNS figlio denominata mychild.zone.com nel gruppo di risorse specificato e archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="759b0-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="759b0-128">Viene inoltre aggiunta la delega nella zona DNS padre denominata zone.com come passato nell'oggetto ParentZone.</span><span class="sxs-lookup"><span data-stu-id="759b0-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="759b0-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="759b0-129">PARAMETERS</span></span>

### <span data-ttu-id="759b0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759b0-130">-DefaultProfile</span></span>
<span data-ttu-id="759b0-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="759b0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="759b0-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="759b0-132">-Name</span></span>
<span data-ttu-id="759b0-133">Specifica il nome della zona DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="759b0-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="759b0-134">-ParentZone</span></span>
<span data-ttu-id="759b0-135">Nome completo dell'area padre per aggiungere la delega (senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="759b0-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="759b0-136">-ParentZoneId</span></span>
<span data-ttu-id="759b0-137">ID risorsa della zona padre per aggiungere la delega (senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="759b0-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="759b0-138">-ParentZoneName</span></span>
<span data-ttu-id="759b0-139">Nome completo dell'area padre per aggiungere la delega (senza un punto di terminazione).</span><span class="sxs-lookup"><span data-stu-id="759b0-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="759b0-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="759b0-141">L'elenco delle reti virtuali che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="759b0-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="759b0-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="759b0-143">Elenco di ID di rete virtuale che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="759b0-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="759b0-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="759b0-145">L'elenco delle reti virtuali in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="759b0-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="759b0-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="759b0-147">Elenco di ID di rete virtuale in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="759b0-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759b0-148">-ResourceGroupName</span></span>
<span data-ttu-id="759b0-149">Specifica il gruppo di risorse in cui creare la zona.</span><span class="sxs-lookup"><span data-stu-id="759b0-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="759b0-150">-Tag</span></span>
<span data-ttu-id="759b0-151">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="759b0-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="759b0-152">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="759b0-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="759b0-153">-ZoneType</span></span>
<span data-ttu-id="759b0-154">Tipo della zona, pubblico o privato.</span><span class="sxs-lookup"><span data-stu-id="759b0-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="759b0-155">Le aree senza un tipo o con un tipo di pubblico vengono messe a disposizione nel piano di servizio DNS pubblico per l'uso nella gerarchia DNS.</span><span class="sxs-lookup"><span data-stu-id="759b0-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="759b0-156">Le aree con un tipo di privato sono visibili solo con il set di reti virtuali associate (questa funzionalità è in anteprima).</span><span class="sxs-lookup"><span data-stu-id="759b0-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="759b0-157">Questa proprietà non può essere modificata per una zona.</span><span class="sxs-lookup"><span data-stu-id="759b0-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="759b0-158">-Confirm</span></span>
<span data-ttu-id="759b0-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="759b0-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759b0-160">-WhatIf</span></span>
<span data-ttu-id="759b0-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="759b0-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="759b0-162">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="759b0-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="759b0-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="759b0-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="759b0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759b0-164">CommonParameters</span></span>
<span data-ttu-id="759b0-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="759b0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759b0-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759b0-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759b0-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="759b0-167">INPUTS</span></span>

### <span data-ttu-id="759b0-168">System. String</span><span class="sxs-lookup"><span data-stu-id="759b0-168">System.String</span></span>

### <span data-ttu-id="759b0-169">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="759b0-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="759b0-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="759b0-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="759b0-171">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="759b0-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="759b0-172">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="759b0-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="759b0-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="759b0-173">OUTPUTS</span></span>

### <span data-ttu-id="759b0-174">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="759b0-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="759b0-175">Note</span><span class="sxs-lookup"><span data-stu-id="759b0-175">NOTES</span></span>
<span data-ttu-id="759b0-176">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="759b0-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="759b0-177">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="759b0-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="759b0-178">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="759b0-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="759b0-179">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="759b0-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="759b0-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="759b0-180">RELATED LINKS</span></span>

[<span data-ttu-id="759b0-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="759b0-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="759b0-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="759b0-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="759b0-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="759b0-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
