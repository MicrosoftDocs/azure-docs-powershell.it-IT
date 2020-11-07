---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866871"
---
# <span data-ttu-id="695c2-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="695c2-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="695c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="695c2-102">SYNOPSIS</span></span>
<span data-ttu-id="695c2-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="695c2-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="695c2-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="695c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="695c2-105">DESCRIPTION</span></span>
<span data-ttu-id="695c2-106">Il cmdlet **New-AzureRmRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="695c2-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="695c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="695c2-107">EXAMPLES</span></span>

### <span data-ttu-id="695c2-108">Esempio 1: creare una tabella di route che contiene una route</span><span class="sxs-lookup"><span data-stu-id="695c2-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="695c2-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzureRmRouteConfig e lo archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="695c2-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="695c2-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="695c2-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="695c2-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="695c2-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="695c2-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione della tabella.</span><span class="sxs-lookup"><span data-stu-id="695c2-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="695c2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="695c2-113">PARAMETERS</span></span>

### <span data-ttu-id="695c2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="695c2-114">-AsJob</span></span>
<span data-ttu-id="695c2-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="695c2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695c2-116">-DefaultProfile</span></span>
<span data-ttu-id="695c2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="695c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="695c2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="695c2-118">-Force</span></span>
<span data-ttu-id="695c2-119">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="695c2-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="695c2-120">-Location</span></span>
<span data-ttu-id="695c2-121">Specifica l'area di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="695c2-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="695c2-122">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="695c2-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="695c2-123">-Name</span></span>
<span data-ttu-id="695c2-124">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="695c2-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="695c2-126">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="695c2-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-127">-Route</span><span class="sxs-lookup"><span data-stu-id="695c2-127">-Route</span></span>
<span data-ttu-id="695c2-128">Specifica una matrice di oggetti **Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="695c2-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="695c2-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="695c2-129">-Tag</span></span>
<span data-ttu-id="695c2-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="695c2-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="695c2-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="695c2-131">For example:</span></span>

<span data-ttu-id="695c2-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="695c2-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="695c2-133">-Confirm</span></span>
<span data-ttu-id="695c2-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="695c2-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695c2-135">-WhatIf</span></span>
<span data-ttu-id="695c2-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="695c2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="695c2-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="695c2-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695c2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695c2-138">CommonParameters</span></span>
<span data-ttu-id="695c2-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695c2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695c2-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695c2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695c2-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="695c2-141">INPUTS</span></span>

## <span data-ttu-id="695c2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="695c2-142">OUTPUTS</span></span>

### <span data-ttu-id="695c2-143">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="695c2-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="695c2-144">Note</span><span class="sxs-lookup"><span data-stu-id="695c2-144">NOTES</span></span>

## <span data-ttu-id="695c2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="695c2-145">RELATED LINKS</span></span>

[<span data-ttu-id="695c2-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="695c2-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="695c2-147">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="695c2-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="695c2-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="695c2-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="695c2-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="695c2-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
