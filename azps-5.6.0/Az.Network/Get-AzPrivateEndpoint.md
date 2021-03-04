---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpoint.md
ms.openlocfilehash: 09bd7f919b953c4df09293a75c2c893df4a01b96
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954222"
---
# <span data-ttu-id="bfdb2-101">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfdb2-101">Get-AzPrivateEndpoint</span></span>

## <span data-ttu-id="bfdb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfdb2-102">SYNOPSIS</span></span>
<span data-ttu-id="bfdb2-103">Ottenere un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="bfdb2-103">Get a private endpoint</span></span>

## <span data-ttu-id="bfdb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfdb2-104">SYNTAX</span></span>

### <span data-ttu-id="bfdb2-105">NoExpand (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfdb2-105">NoExpand (Default)</span></span>
```
Get-AzPrivateEndpoint [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfdb2-106">Espandi</span><span class="sxs-lookup"><span data-stu-id="bfdb2-106">Expand</span></span>
```
Get-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfdb2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfdb2-107">DESCRIPTION</span></span>
<span data-ttu-id="bfdb2-108">Il cmdlet **Get-AzPrivateEndpoint** ottiene uno o più endpoint privati.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-108">The **Get-AzPrivateEndpoint** cmdlet gets one or more private endpoints.</span></span>

## <span data-ttu-id="bfdb2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfdb2-109">EXAMPLES</span></span>

### <span data-ttu-id="bfdb2-110">Esempio 1: Recuperare un endpoint privato</span><span class="sxs-lookup"><span data-stu-id="bfdb2-110">Example 1: Retrieve a private endpoint</span></span>
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

<span data-ttu-id="bfdb2-111">Questo comando ottiene l'endpoint privato denominato MyPrivateEndpoint1 nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bfdb2-111">This command gets the private endpoint named MyPrivateEndpoint1 in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="bfdb2-112">Esempio 2: Elencare tutti gli endpoint privati nel Gruppo Risorse</span><span class="sxs-lookup"><span data-stu-id="bfdb2-112">Example 2: List all private endpoints in ResourceGroup</span></span>
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

<span data-ttu-id="bfdb2-113">Questo comando ottiene tutti i punti finali privati nel gruppo di risorse TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bfdb2-113">This command gets all of private end points in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="bfdb2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfdb2-114">PARAMETERS</span></span>

### <span data-ttu-id="bfdb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfdb2-115">-DefaultProfile</span></span>
<span data-ttu-id="bfdb2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfdb2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="bfdb2-117">-ExpandResource</span></span>
<span data-ttu-id="bfdb2-118">Riferimento di risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-118">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="bfdb2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bfdb2-119">-Name</span></span>
<span data-ttu-id="bfdb2-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-120">The resource name.</span></span>

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

### <span data-ttu-id="bfdb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfdb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="bfdb2-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-122">The resource group name.</span></span>

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

### <span data-ttu-id="bfdb2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfdb2-123">CommonParameters</span></span>
<span data-ttu-id="bfdb2-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfdb2-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfdb2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfdb2-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfdb2-126">INPUTS</span></span>

### <span data-ttu-id="bfdb2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bfdb2-127">System.String</span></span>

## <span data-ttu-id="bfdb2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfdb2-128">OUTPUTS</span></span>

### <span data-ttu-id="bfdb2-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bfdb2-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bfdb2-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfdb2-130">NOTES</span></span>

## <span data-ttu-id="bfdb2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfdb2-131">RELATED LINKS</span></span>

[<span data-ttu-id="bfdb2-132">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfdb2-132">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="bfdb2-133">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfdb2-133">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)