---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: 2c001da52c50f89aedea12b6049bce3ae5c42d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982333"
---
# <span data-ttu-id="47d86-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="47d86-101">New-AzRouteTable</span></span>

## <span data-ttu-id="47d86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47d86-102">SYNOPSIS</span></span>
<span data-ttu-id="47d86-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="47d86-103">Creates a route table.</span></span>

## <span data-ttu-id="47d86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47d86-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47d86-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47d86-105">DESCRIPTION</span></span>
<span data-ttu-id="47d86-106">Il cmdlet **New-AzRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="47d86-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="47d86-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47d86-107">EXAMPLES</span></span>

### <span data-ttu-id="47d86-108">Esempio 1: Creare una tabella di route contenente un percorso</span><span class="sxs-lookup"><span data-stu-id="47d86-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="47d86-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzRouteConfig, quindi la archivia nella $Route variabile.</span><span class="sxs-lookup"><span data-stu-id="47d86-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="47d86-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="47d86-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="47d86-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="47d86-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="47d86-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione per la tabella.</span><span class="sxs-lookup"><span data-stu-id="47d86-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="47d86-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47d86-113">PARAMETERS</span></span>

### <span data-ttu-id="47d86-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47d86-114">-AsJob</span></span>
<span data-ttu-id="47d86-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="47d86-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47d86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d86-116">-DefaultProfile</span></span>
<span data-ttu-id="47d86-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47d86-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47d86-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="47d86-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="47d86-119">Disabilitare la propagazione automatica delle route BGP.</span><span class="sxs-lookup"><span data-stu-id="47d86-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="47d86-120">-Force</span><span class="sxs-lookup"><span data-stu-id="47d86-120">-Force</span></span>
<span data-ttu-id="47d86-121">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="47d86-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="47d86-122">-Location</span><span class="sxs-lookup"><span data-stu-id="47d86-122">-Location</span></span>
<span data-ttu-id="47d86-123">Specifica l'area geografica di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="47d86-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="47d86-124">Per altre informazioni, vedere [Aree geografiche di Azure.](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="47d86-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="47d86-125">-Name</span><span class="sxs-lookup"><span data-stu-id="47d86-125">-Name</span></span>
<span data-ttu-id="47d86-126">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="47d86-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="47d86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d86-127">-ResourceGroupName</span></span>
<span data-ttu-id="47d86-128">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="47d86-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="47d86-129">-Route</span><span class="sxs-lookup"><span data-stu-id="47d86-129">-Route</span></span>
<span data-ttu-id="47d86-130">Specifica una matrice di **oggetti Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="47d86-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="47d86-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="47d86-131">-Tag</span></span>
<span data-ttu-id="47d86-132">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47d86-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="47d86-133">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="47d86-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="47d86-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47d86-134">-Confirm</span></span>
<span data-ttu-id="47d86-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47d86-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47d86-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47d86-136">-WhatIf</span></span>
<span data-ttu-id="47d86-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47d86-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47d86-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47d86-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47d86-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d86-139">CommonParameters</span></span>
<span data-ttu-id="47d86-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d86-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d86-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d86-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d86-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="47d86-142">INPUTS</span></span>

### <span data-ttu-id="47d86-143">System.String</span><span class="sxs-lookup"><span data-stu-id="47d86-143">System.String</span></span>

### <span data-ttu-id="47d86-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="47d86-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="47d86-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span><span class="sxs-lookup"><span data-stu-id="47d86-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="47d86-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47d86-146">OUTPUTS</span></span>

### <span data-ttu-id="47d86-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="47d86-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="47d86-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="47d86-148">NOTES</span></span>

## <span data-ttu-id="47d86-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47d86-149">RELATED LINKS</span></span>

[<span data-ttu-id="47d86-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="47d86-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="47d86-151">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="47d86-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="47d86-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="47d86-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="47d86-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="47d86-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
