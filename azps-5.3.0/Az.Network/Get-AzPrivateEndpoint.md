---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475488"
---
# <span data-ttu-id="304fa-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="304fa-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="304fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="304fa-102">SYNOPSIS</span></span>
<span data-ttu-id="304fa-103">Ottenere un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="304fa-103">Get a private endpoint</span></span>

## <span data-ttu-id="304fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="304fa-104">SYNTAX</span></span>

### <span data-ttu-id="304fa-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="304fa-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="304fa-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="304fa-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="304fa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="304fa-107">DESCRIPTION</span></span>
<span data-ttu-id="304fa-108">Il cmdlet **Get-AzPrivateEndpoint** ottiene uno o più endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="304fa-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="304fa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="304fa-109">EXAMPLES</span></span>

### <span data-ttu-id="304fa-110">Esempio 1: recuperare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="304fa-110">Example 1: Retrieve a private endpoint</span></span>
```powershell
Get-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="304fa-111">Questo comando ottiene l'endpoint privato denominato MyPrivateEndpoint1 nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="304fa-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="304fa-112">Esempio 2: elencare tutti gli endpoint privati in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="304fa-112">Example 2: List all private endpoints in ResourceGroup</span></span>
```powershell
Get-AzPrivateEndpoint -ResourceGroupName TestResourceGroup

Name                                : MyPrivateEndpoint1
ResourceGroupName                   : TestResourceGroup
Location                            : eastus2euap
Id                                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/provi
                                      ders/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1
Etag                                : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                   : Succeeded
Subnet                              : {
                                        "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1/subnets/backendSubnet",
                                      }
NetworkInterfaces                   : [
                                        {

                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/MyNic1",
                                        }
                                      ]
PrivateLinkServiceConnections       : []
ManualPrivateLinkServiceConnections : [
                                        {
                                          "Name": "MyPrivateLinkServiceConnection",
                                          "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateEndpoints/MyPrivateEndpoint1/manualPrivateLinkServi
                                      ceConnections/MyPrivateLinkServiceConnection",
                                          "PrivateLinkServiceId": "/subscriptions/00000000-0000-0000-0000-000000000000/
                                      resourceGroups/TestResourceGroup/providers/Microsoft.Network/priv
                                      ateLinkServices/MyPrivateLinkService",
                                          "PrivateLinkServiceConnectionState": {
                                            "Status": "Pending",
                                            "Description": "Awaiting approval"
                                          }
                                        }
                                      ]
```

<span data-ttu-id="304fa-113">Questo comando ottiene tutti i punti finali privati nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="304fa-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="304fa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="304fa-114">PARAMETERS</span></span>

### <span data-ttu-id="304fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304fa-115">-DefaultProfile</span></span>
<span data-ttu-id="304fa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="304fa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304fa-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="304fa-117">-ExpandResource</span></span>
<span data-ttu-id="304fa-118">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="304fa-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="304fa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="304fa-119">-Name</span></span>
<span data-ttu-id="304fa-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="304fa-120">The resource name.</span></span>

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

### <span data-ttu-id="304fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="304fa-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="304fa-122">The resource group name.</span></span>

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

### <span data-ttu-id="304fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304fa-123">CommonParameters</span></span>
<span data-ttu-id="304fa-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304fa-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304fa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304fa-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="304fa-126">INPUTS</span></span>

### <span data-ttu-id="304fa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="304fa-127">System.String</span></span>

## <span data-ttu-id="304fa-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="304fa-128">OUTPUTS</span></span>

### <span data-ttu-id="304fa-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="304fa-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="304fa-130">Note</span><span class="sxs-lookup"><span data-stu-id="304fa-130">NOTES</span></span>

## <span data-ttu-id="304fa-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="304fa-131">RELATED LINKS</span></span>

[<span data-ttu-id="304fa-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="304fa-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="304fa-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="304fa-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)