---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: f00840afac4a4d1f0d92316bc859e0a66e7806ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860425"
---
# <span data-ttu-id="ce424-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce424-101">New-AzRouteTable</span></span>

## <span data-ttu-id="ce424-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce424-102">SYNOPSIS</span></span>
<span data-ttu-id="ce424-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ce424-103">Creates a route table.</span></span>

## <span data-ttu-id="ce424-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce424-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce424-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce424-105">DESCRIPTION</span></span>
<span data-ttu-id="ce424-106">Il cmdlet **New-AzRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce424-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="ce424-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce424-107">EXAMPLES</span></span>

### <span data-ttu-id="ce424-108">Esempio 1: creare una tabella di route che contiene una route</span><span class="sxs-lookup"><span data-stu-id="ce424-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="ce424-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzRouteConfig e lo archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="ce424-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="ce424-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="ce424-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="ce424-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="ce424-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="ce424-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione della tabella.</span><span class="sxs-lookup"><span data-stu-id="ce424-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="ce424-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce424-113">PARAMETERS</span></span>

### <span data-ttu-id="ce424-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce424-114">-AsJob</span></span>
<span data-ttu-id="ce424-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce424-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce424-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce424-116">-DefaultProfile</span></span>
<span data-ttu-id="ce424-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce424-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce424-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce424-118">-Force</span></span>
<span data-ttu-id="ce424-119">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="ce424-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="ce424-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ce424-120">-Location</span></span>
<span data-ttu-id="ce424-121">Specifica l'area di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ce424-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="ce424-122">Per altre informazioni, Vedi [aree di Azure](http://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="ce424-122">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="ce424-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce424-123">-Name</span></span>
<span data-ttu-id="ce424-124">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ce424-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="ce424-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce424-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce424-126">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="ce424-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="ce424-127">-Route</span><span class="sxs-lookup"><span data-stu-id="ce424-127">-Route</span></span>
<span data-ttu-id="ce424-128">Specifica una matrice di oggetti **Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="ce424-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="ce424-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce424-129">-Tag</span></span>
<span data-ttu-id="ce424-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ce424-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ce424-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ce424-131">For example:</span></span>

<span data-ttu-id="ce424-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ce424-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ce424-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce424-133">-Confirm</span></span>
<span data-ttu-id="ce424-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce424-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce424-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce424-135">-WhatIf</span></span>
<span data-ttu-id="ce424-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce424-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce424-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce424-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce424-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce424-138">CommonParameters</span></span>
<span data-ttu-id="ce424-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce424-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce424-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce424-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce424-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce424-141">INPUTS</span></span>

## <span data-ttu-id="ce424-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce424-142">OUTPUTS</span></span>

### <span data-ttu-id="ce424-143">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce424-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ce424-144">Note</span><span class="sxs-lookup"><span data-stu-id="ce424-144">NOTES</span></span>

## <span data-ttu-id="ce424-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce424-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce424-146">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce424-146">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="ce424-147">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ce424-147">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="ce424-148">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce424-148">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="ce424-149">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce424-149">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
