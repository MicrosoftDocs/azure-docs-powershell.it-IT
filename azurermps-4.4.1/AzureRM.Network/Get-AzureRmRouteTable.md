---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: fb675f1d834160bd1fcf5e2dde60dc00e697d629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686225"
---
# <span data-ttu-id="bb8aa-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb8aa-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="bb8aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8aa-103">Ottiene le tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb8aa-104">SYNTAX</span></span>

### <span data-ttu-id="bb8aa-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="bb8aa-105">NoExpand</span></span>
```
Get-AzureRmRouteTable [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb8aa-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="bb8aa-106">Expand</span></span>
```
Get-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb8aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="bb8aa-108">Il cmdlet **Get-AzureRmRouteTable** ottiene le tabelle di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="bb8aa-109">È possibile ottenere una singola tabella di route o ottenere tutte le tabelle di route in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="bb8aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb8aa-110">EXAMPLES</span></span>

### <span data-ttu-id="bb8aa-111">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="bb8aa-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
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

<span data-ttu-id="bb8aa-112">Questo comando consente di ottenere la tabella route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="bb8aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb8aa-113">PARAMETERS</span></span>

### <span data-ttu-id="bb8aa-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bb8aa-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb8aa-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb8aa-115">-Name</span></span>
<span data-ttu-id="bb8aa-116">Specifica il nome della tabella di route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-116">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb8aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb8aa-118">Specifica il nome del gruppo di risorse che contiene le tabelle di route ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-118">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb8aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8aa-119">-DefaultProfile</span></span>
<span data-ttu-id="bb8aa-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb8aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8aa-121">CommonParameters</span></span>
<span data-ttu-id="bb8aa-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb8aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8aa-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8aa-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb8aa-124">INPUTS</span></span>

## <span data-ttu-id="bb8aa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb8aa-125">OUTPUTS</span></span>

### <span data-ttu-id="bb8aa-126">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb8aa-126">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="bb8aa-127">Note</span><span class="sxs-lookup"><span data-stu-id="bb8aa-127">NOTES</span></span>

## <span data-ttu-id="bb8aa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb8aa-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb8aa-129">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb8aa-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="bb8aa-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb8aa-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="bb8aa-131">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bb8aa-131">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


