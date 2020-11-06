---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: ed438e3e649d26db5b0da85b833794ad1872fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516651"
---
# <span data-ttu-id="99f61-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="99f61-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="99f61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99f61-102">SYNOPSIS</span></span>
<span data-ttu-id="99f61-103">Crea una nuova zona DNS.</span><span class="sxs-lookup"><span data-stu-id="99f61-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99f61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99f61-104">SYNTAX</span></span>

### <span data-ttu-id="99f61-105">ID (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99f61-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f61-106">Oggetti</span><span class="sxs-lookup"><span data-stu-id="99f61-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99f61-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99f61-107">DESCRIPTION</span></span>
<span data-ttu-id="99f61-108">Il cmdlet **New-AzureRmDnsZone** crea una nuova area DNS (Domain Name System) nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="99f61-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="99f61-109">Devi specificare un nome di zona DNS univoco per il parametro *Name* o il cmdlet restituirà un errore.</span><span class="sxs-lookup"><span data-stu-id="99f61-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="99f61-110">Dopo aver creato la zona, usare il cmdlet New-AzureRmDnsRecordSet per creare set di record nella zona.</span><span class="sxs-lookup"><span data-stu-id="99f61-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="99f61-111">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="99f61-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="99f61-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99f61-112">EXAMPLES</span></span>

### <span data-ttu-id="99f61-113">Esempio 1: creare una zona DNS</span><span class="sxs-lookup"><span data-stu-id="99f61-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="99f61-114">Questo comando crea una nuova zona DNS denominata myzone.com nel gruppo di risorse specificato e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="99f61-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="99f61-115">Esempio 2: creare una zona DNS privata specificando gli ID di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="99f61-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="99f61-116">Questo comando crea una nuova zona DNS privata denominata myprivatezone.com nel gruppo di risorse specificato con una rete virtuale di risoluzione associata (specificando il relativo ID) e la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="99f61-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="99f61-117">Esempio 3: creare una zona DNS privata specificando gli oggetti di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="99f61-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="99f61-118">Questo comando crea una nuova zona DNS privata denominata myprivatezone.com nel gruppo di risorse specificato con una rete virtuale di risoluzione associata (a cui fa riferimento la variabile $ResVirtualNetwork), quindi la archivia nella variabile $Zone.</span><span class="sxs-lookup"><span data-stu-id="99f61-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="99f61-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99f61-119">PARAMETERS</span></span>

### <span data-ttu-id="99f61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f61-120">-DefaultProfile</span></span>
<span data-ttu-id="99f61-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="99f61-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f61-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="99f61-122">-Name</span></span>
<span data-ttu-id="99f61-123">Specifica il nome della zona DNS da creare.</span><span class="sxs-lookup"><span data-stu-id="99f61-123">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="99f61-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99f61-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="99f61-125">L'elenco delle reti virtuali che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="99f61-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="99f61-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="99f61-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="99f61-127">Elenco di ID di rete virtuale che registreranno i record hostname della macchina virtuale in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="99f61-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="99f61-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="99f61-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="99f61-129">L'elenco delle reti virtuali in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="99f61-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="99f61-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="99f61-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="99f61-131">Elenco di ID di rete virtuale in grado di risolvere i record in questa zona DNS, disponibile solo per le aree private.</span><span class="sxs-lookup"><span data-stu-id="99f61-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="99f61-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f61-132">-ResourceGroupName</span></span>
<span data-ttu-id="99f61-133">Specifica il gruppo di risorse in cui creare la zona.</span><span class="sxs-lookup"><span data-stu-id="99f61-133">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="99f61-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="99f61-134">-Tag</span></span>
<span data-ttu-id="99f61-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="99f61-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="99f61-136">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="99f61-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99f61-137">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="99f61-137">-ZoneType</span></span>
<span data-ttu-id="99f61-138">Tipo della zona, pubblico o privato.</span><span class="sxs-lookup"><span data-stu-id="99f61-138">The type of the zone, Public or Private.</span></span> <span data-ttu-id="99f61-139">Le aree senza un tipo o con un tipo di pubblico vengono messe a disposizione nel piano di servizio DNS pubblico per l'uso nella gerarchia DNS.</span><span class="sxs-lookup"><span data-stu-id="99f61-139">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="99f61-140">Le aree con un tipo di privato sono visibili solo con il set di reti virtuali associate (questa funzionalità è in anteprima).</span><span class="sxs-lookup"><span data-stu-id="99f61-140">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="99f61-141">Questa proprietà non può essere modificata per una zona.</span><span class="sxs-lookup"><span data-stu-id="99f61-141">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="99f61-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99f61-142">-Confirm</span></span>
<span data-ttu-id="99f61-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f61-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f61-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f61-144">-WhatIf</span></span>
<span data-ttu-id="99f61-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99f61-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99f61-146">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99f61-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99f61-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99f61-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f61-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f61-148">CommonParameters</span></span>
<span data-ttu-id="99f61-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f61-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f61-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f61-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f61-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99f61-151">INPUTS</span></span>

### <span data-ttu-id="99f61-152">System. String</span><span class="sxs-lookup"><span data-stu-id="99f61-152">System.String</span></span>

### <span data-ttu-id="99f61-153">System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, Version = 2.1.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="99f61-153">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="99f61-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99f61-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="99f61-155">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="99f61-155">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="99f61-156">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. Commands. Common. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="99f61-156">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.Commands.Common.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="99f61-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99f61-157">OUTPUTS</span></span>

### <span data-ttu-id="99f61-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="99f61-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="99f61-159">Note</span><span class="sxs-lookup"><span data-stu-id="99f61-159">NOTES</span></span>
<span data-ttu-id="99f61-160">Puoi usare il parametro *Confirm* per controllare se questo cmdlet richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="99f61-160">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="99f61-161">Per impostazione predefinita, il cmdlet richiede conferma se la $ConfirmPreference variabile di Windows PowerShell ha un valore medio o inferiore.</span><span class="sxs-lookup"><span data-stu-id="99f61-161">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="99f61-162">Se si specifica *Confirm* o *Confirm: $true* , questo cmdlet richiede la conferma prima della sua esecuzione.</span><span class="sxs-lookup"><span data-stu-id="99f61-162">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="99f61-163">Se si specifica *Confirm: $false* , il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="99f61-163">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="99f61-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99f61-164">RELATED LINKS</span></span>

[<span data-ttu-id="99f61-165">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="99f61-165">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="99f61-166">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="99f61-166">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="99f61-167">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="99f61-167">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)