---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 04e50033a304918eb37d28c2ef5ea5328d5744c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515080"
---
# <span data-ttu-id="1a0d2-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a0d2-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="1a0d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0d2-103">Ottiene le tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a0d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a0d2-104">SYNTAX</span></span>

### <span data-ttu-id="1a0d2-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a0d2-105">NoExpand (Default)</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a0d2-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="1a0d2-106">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a0d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a0d2-107">DESCRIPTION</span></span>
<span data-ttu-id="1a0d2-108">Il cmdlet **Get-AzureRmRouteTable** ottiene le tabelle di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="1a0d2-109">È possibile ottenere una singola tabella di route o ottenere tutte le tabelle di route in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="1a0d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a0d2-110">EXAMPLES</span></span>

### <span data-ttu-id="1a0d2-111">Esempio 1: ottenere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="1a0d2-111">Example 1: Get a route table</span></span>
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

<span data-ttu-id="1a0d2-112">Questo comando consente di ottenere la tabella route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1a0d2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a0d2-113">PARAMETERS</span></span>

### <span data-ttu-id="1a0d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0d2-114">-DefaultProfile</span></span>
<span data-ttu-id="1a0d2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0d2-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1a0d2-116">-ExpandResource</span></span>
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

### <span data-ttu-id="1a0d2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a0d2-117">-Name</span></span>
<span data-ttu-id="1a0d2-118">Specifica il nome della tabella di route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-118">Specifies the name of the route table that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a0d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a0d2-120">Specifica il nome del gruppo di risorse che contiene le tabelle di route ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1a0d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0d2-121">CommonParameters</span></span>
<span data-ttu-id="1a0d2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0d2-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0d2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a0d2-124">INPUTS</span></span>

### <span data-ttu-id="1a0d2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0d2-125">System.String</span></span>

## <span data-ttu-id="1a0d2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a0d2-126">OUTPUTS</span></span>

### <span data-ttu-id="1a0d2-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a0d2-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="1a0d2-128">Note</span><span class="sxs-lookup"><span data-stu-id="1a0d2-128">NOTES</span></span>

## <span data-ttu-id="1a0d2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a0d2-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a0d2-130">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a0d2-130">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="1a0d2-131">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a0d2-131">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="1a0d2-132">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="1a0d2-132">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


