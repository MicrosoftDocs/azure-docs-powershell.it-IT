---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: a311d64fbdb086ca1d52ab5a1db725e278c6cc16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519912"
---
# <span data-ttu-id="9d77f-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d77f-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="9d77f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d77f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d77f-103">Crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d77f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d77f-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-DisableBgpRoutePropagation] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d77f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d77f-105">DESCRIPTION</span></span>
<span data-ttu-id="9d77f-106">Il cmdlet **New-AzureRmRouteTable** crea una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="9d77f-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="9d77f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d77f-107">EXAMPLES</span></span>

### <span data-ttu-id="9d77f-108">Esempio 1: creare una tabella di route che contiene una route</span><span class="sxs-lookup"><span data-stu-id="9d77f-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="9d77f-109">Il primo comando crea una route denominata Route07 usando il cmdlet New-AzureRmRouteConfig e lo archivia nella variabile $Route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="9d77f-110">Questa route inoltra i pacchetti alla rete virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="9d77f-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="9d77f-111">Il secondo comando crea una tabella di route denominata RouteTable01 e aggiunge la route archiviata in $Route alla nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="9d77f-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="9d77f-112">Il comando specifica il gruppo di risorse a cui appartiene la tabella e la posizione della tabella.</span><span class="sxs-lookup"><span data-stu-id="9d77f-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="9d77f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d77f-113">PARAMETERS</span></span>

### <span data-ttu-id="9d77f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d77f-114">-AsJob</span></span>
<span data-ttu-id="9d77f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d77f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d77f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d77f-116">-DefaultProfile</span></span>
<span data-ttu-id="9d77f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d77f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d77f-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="9d77f-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="9d77f-119">Disabilitare la propagazione automatica della route BGP.</span><span class="sxs-lookup"><span data-stu-id="9d77f-119">Disable BGP Route auto propagation.</span></span>

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

### <span data-ttu-id="9d77f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9d77f-120">-Force</span></span>
<span data-ttu-id="9d77f-121">Indica che questo cmdlet crea una tabella di route anche se esiste già una tabella di route con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="9d77f-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="9d77f-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9d77f-122">-Location</span></span>
<span data-ttu-id="9d77f-123">Specifica l'area di Azure in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="9d77f-124">Per altre informazioni, Vedi [aree di Azure](https://azure.microsoft.com/en-us/regions/).</span><span class="sxs-lookup"><span data-stu-id="9d77f-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="9d77f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d77f-125">-Name</span></span>
<span data-ttu-id="9d77f-126">Specifica un nome per la tabella di route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-126">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="9d77f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d77f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d77f-128">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="9d77f-129">-Route</span><span class="sxs-lookup"><span data-stu-id="9d77f-129">-Route</span></span>
<span data-ttu-id="9d77f-130">Specifica una matrice di oggetti **Route** da associare alla tabella route.</span><span class="sxs-lookup"><span data-stu-id="9d77f-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="9d77f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9d77f-131">-Tag</span></span>
<span data-ttu-id="9d77f-132">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9d77f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9d77f-133">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="9d77f-133">For example:</span></span>

<span data-ttu-id="9d77f-134">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9d77f-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9d77f-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d77f-135">-Confirm</span></span>
<span data-ttu-id="9d77f-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d77f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d77f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d77f-137">-WhatIf</span></span>
<span data-ttu-id="9d77f-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d77f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d77f-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d77f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d77f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d77f-140">CommonParameters</span></span>
<span data-ttu-id="9d77f-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d77f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d77f-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d77f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d77f-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d77f-143">INPUTS</span></span>

### <span data-ttu-id="9d77f-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9d77f-144">None</span></span>
<span data-ttu-id="9d77f-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9d77f-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d77f-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d77f-146">OUTPUTS</span></span>

### <span data-ttu-id="9d77f-147">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d77f-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9d77f-148">Note</span><span class="sxs-lookup"><span data-stu-id="9d77f-148">NOTES</span></span>

## <span data-ttu-id="9d77f-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d77f-149">RELATED LINKS</span></span>

[<span data-ttu-id="9d77f-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d77f-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="9d77f-151">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9d77f-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="9d77f-152">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d77f-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="9d77f-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="9d77f-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
