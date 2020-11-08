---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 11a0b65118fc9b580a885510f1e5ffa337b1d2e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199670"
---
# <span data-ttu-id="625ae-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="625ae-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="625ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="625ae-102">SYNOPSIS</span></span>
<span data-ttu-id="625ae-103">Ottenere un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="625ae-103">Get a private endpoint</span></span>

## <span data-ttu-id="625ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="625ae-104">SYNTAX</span></span>

### <span data-ttu-id="625ae-105">NOEXPAND (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="625ae-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="625ae-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="625ae-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="625ae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="625ae-107">DESCRIPTION</span></span>
<span data-ttu-id="625ae-108">Il cmdlet **Get-AzPrivateEndpoint** ottiene uno o più endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="625ae-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="625ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="625ae-109">EXAMPLES</span></span>

### <span data-ttu-id="625ae-110">Esempio 1: recuperare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="625ae-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="625ae-111">Questo comando ottiene l'endpoint privato denominato MyPrivateEndpoint1 nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="625ae-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="625ae-112">Esempio 2: elencare tutti gli endpoint privati in ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="625ae-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="625ae-113">Questo comando ottiene tutti i punti finali privati nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="625ae-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="625ae-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="625ae-114">PARAMETERS</span></span>

### <span data-ttu-id="625ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625ae-115">-DefaultProfile</span></span>
<span data-ttu-id="625ae-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="625ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625ae-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="625ae-117">-ExpandResource</span></span>
<span data-ttu-id="625ae-118">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="625ae-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="625ae-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="625ae-119">-Name</span></span>
<span data-ttu-id="625ae-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="625ae-120">The resource name.</span></span>

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

### <span data-ttu-id="625ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="625ae-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="625ae-122">The resource group name.</span></span>

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

### <span data-ttu-id="625ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625ae-123">CommonParameters</span></span>
<span data-ttu-id="625ae-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="625ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625ae-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="625ae-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625ae-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="625ae-126">INPUTS</span></span>

### <span data-ttu-id="625ae-127">System. String</span><span class="sxs-lookup"><span data-stu-id="625ae-127">System.String</span></span>

## <span data-ttu-id="625ae-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="625ae-128">OUTPUTS</span></span>

### <span data-ttu-id="625ae-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="625ae-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="625ae-130">Note</span><span class="sxs-lookup"><span data-stu-id="625ae-130">NOTES</span></span>

## <span data-ttu-id="625ae-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="625ae-131">RELATED LINKS</span></span>

[<span data-ttu-id="625ae-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="625ae-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="625ae-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="625ae-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)