---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678238"
---
# <span data-ttu-id="d1dc6-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-101">New-AzRouteTable</span></span>

## <span data-ttu-id="d1dc6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d1dc6-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-103">Creates a route table.</span></span>

## <span data-ttu-id="d1dc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1dc6-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1dc6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="d1dc6-106">Il cmdlet **New-AzRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="d1dc6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1dc6-107">EXAMPLES</span></span>

### <span data-ttu-id="d1dc6-108">Esempio 1: creare una tabella di route che contiene una route</span><span class="sxs-lookup"><span data-stu-id="d1dc6-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="d1dc6-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzRouteConfig e lo archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="d1dc6-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="d1dc6-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="d1dc6-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione della tabella.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="d1dc6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1dc6-113">PARAMETERS</span></span>

### <span data-ttu-id="d1dc6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1dc6-114">-AsJob</span></span>
<span data-ttu-id="d1dc6-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d1dc6-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1dc6-116">-DefaultProfile</span></span>
<span data-ttu-id="d1dc6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1dc6-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="d1dc6-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="d1dc6-119">Disabilitare la propagazione automatica della route BGP.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d1dc6-120">-Force</span></span>
<span data-ttu-id="d1dc6-121">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d1dc6-122">-Location</span></span>
<span data-ttu-id="d1dc6-123">Specifica l'area di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="d1dc6-124">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="d1dc6-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="d1dc6-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1dc6-125">-Name</span></span>
<span data-ttu-id="d1dc6-126">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1dc6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d1dc6-128">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="d1dc6-129">-Route</span><span class="sxs-lookup"><span data-stu-id="d1dc6-129">-Route</span></span>
<span data-ttu-id="d1dc6-130">Specifica una matrice di oggetti **Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1dc6-131">-Tag</span></span>
<span data-ttu-id="d1dc6-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d1dc6-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d1dc6-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1dc6-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1dc6-134">-Confirm</span></span>
<span data-ttu-id="d1dc6-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1dc6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1dc6-136">-WhatIf</span></span>
<span data-ttu-id="d1dc6-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1dc6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1dc6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1dc6-139">CommonParameters</span></span>
<span data-ttu-id="d1dc6-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1dc6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1dc6-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1dc6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1dc6-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1dc6-142">INPUTS</span></span>

### <span data-ttu-id="d1dc6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d1dc6-143">System.String</span></span>

### <span data-ttu-id="d1dc6-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d1dc6-145">Microsoft. Azure. Commands. Network. Models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="d1dc6-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="d1dc6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1dc6-146">OUTPUTS</span></span>

### <span data-ttu-id="d1dc6-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d1dc6-148">Note</span><span class="sxs-lookup"><span data-stu-id="d1dc6-148">NOTES</span></span>

## <span data-ttu-id="d1dc6-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1dc6-149">RELATED LINKS</span></span>

[<span data-ttu-id="d1dc6-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="d1dc6-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d1dc6-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="d1dc6-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="d1dc6-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d1dc6-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)