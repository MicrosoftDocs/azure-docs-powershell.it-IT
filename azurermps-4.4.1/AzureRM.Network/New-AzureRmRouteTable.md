---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513252"
---
# <span data-ttu-id="79ef7-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="79ef7-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="79ef7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="79ef7-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ef7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ef7-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79ef7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="79ef7-106">Il cmdlet **New-AzureRmRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="79ef7-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="79ef7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="79ef7-108">Esempio 1: creare una tabella di route che contiene una route</span><span class="sxs-lookup"><span data-stu-id="79ef7-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="79ef7-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzureRmRouteConfig e lo archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="79ef7-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="79ef7-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="79ef7-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="79ef7-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="79ef7-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione della tabella.</span><span class="sxs-lookup"><span data-stu-id="79ef7-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="79ef7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79ef7-113">PARAMETERS</span></span>

### <span data-ttu-id="79ef7-114">-Force</span><span class="sxs-lookup"><span data-stu-id="79ef7-114">-Force</span></span>
<span data-ttu-id="79ef7-115">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="79ef7-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="79ef7-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79ef7-116">-Location</span></span>
<span data-ttu-id="79ef7-117">Specifica l'area di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="79ef7-118">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="79ef7-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="79ef7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="79ef7-119">-Name</span></span>
<span data-ttu-id="79ef7-120">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="79ef7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ef7-121">-ResourceGroupName</span></span>
<span data-ttu-id="79ef7-122">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="79ef7-123">-Route</span><span class="sxs-lookup"><span data-stu-id="79ef7-123">-Route</span></span>
<span data-ttu-id="79ef7-124">Specifica una matrice di oggetti **Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="79ef7-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ef7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="79ef7-125">-Tag</span></span>
<span data-ttu-id="79ef7-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="79ef7-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79ef7-127">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="79ef7-127">For example:</span></span>

<span data-ttu-id="79ef7-128">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="79ef7-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="79ef7-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79ef7-129">-Confirm</span></span>
<span data-ttu-id="79ef7-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ef7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79ef7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ef7-131">-WhatIf</span></span>
<span data-ttu-id="79ef7-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ef7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79ef7-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ef7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79ef7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ef7-134">-DefaultProfile</span></span>
<span data-ttu-id="79ef7-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79ef7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79ef7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ef7-136">CommonParameters</span></span>
<span data-ttu-id="79ef7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ef7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ef7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ef7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ef7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79ef7-139">INPUTS</span></span>

## <span data-ttu-id="79ef7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ef7-140">OUTPUTS</span></span>

### <span data-ttu-id="79ef7-141">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="79ef7-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="79ef7-142">Note</span><span class="sxs-lookup"><span data-stu-id="79ef7-142">NOTES</span></span>

## <span data-ttu-id="79ef7-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ef7-143">RELATED LINKS</span></span>

[<span data-ttu-id="79ef7-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="79ef7-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="79ef7-145">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="79ef7-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="79ef7-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="79ef7-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="79ef7-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="79ef7-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
