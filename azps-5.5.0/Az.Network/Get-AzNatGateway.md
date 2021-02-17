---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 650ffdfd557780727a4f3bc4c69a7be6f2783cb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206954"
---
# <span data-ttu-id="c2afa-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="c2afa-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="c2afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2afa-102">SYNOPSIS</span></span>
<span data-ttu-id="c2afa-103">Ottiene una risorsa Gateway Nat in un gruppo di risorse per nome o ID NatGateway o per tutte le risorse di Nat Gateway in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2afa-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="c2afa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2afa-104">SYNTAX</span></span>

### <span data-ttu-id="c2afa-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2afa-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2afa-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2afa-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2afa-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2afa-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2afa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c2afa-108">DESCRIPTION</span></span>
<span data-ttu-id="c2afa-109">Ottiene una risorsa Gateway Nat in un gruppo di risorse per nome O ID NatGateway O per tutte le risorse di Nat Gateway in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2afa-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="c2afa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2afa-110">EXAMPLES</span></span>

### <span data-ttu-id="c2afa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2afa-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="c2afa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2afa-112">PARAMETERS</span></span>

### <span data-ttu-id="c2afa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2afa-113">-DefaultProfile</span></span>
<span data-ttu-id="c2afa-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2afa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2afa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c2afa-115">-Name</span></span>
<span data-ttu-id="c2afa-116">Nome del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="c2afa-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2afa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2afa-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2afa-118">Nome del gruppo di risorse del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="c2afa-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2afa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2afa-119">-ResourceId</span></span>
<span data-ttu-id="c2afa-120">Nat Gateway Id</span><span class="sxs-lookup"><span data-stu-id="c2afa-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2afa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2afa-121">CommonParameters</span></span>
<span data-ttu-id="c2afa-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2afa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2afa-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2afa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2afa-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c2afa-124">INPUTS</span></span>

### <span data-ttu-id="c2afa-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c2afa-125">System.String</span></span>

## <span data-ttu-id="c2afa-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2afa-126">OUTPUTS</span></span>

### <span data-ttu-id="c2afa-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="c2afa-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="c2afa-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="c2afa-128">NOTES</span></span>

## <span data-ttu-id="c2afa-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2afa-129">RELATED LINKS</span></span>
