---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3ca8c522e3aa4d31e5718d09fffe0ff22fd4cab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006301"
---
# <span data-ttu-id="12a11-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="12a11-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="12a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12a11-102">SYNOPSIS</span></span>
<span data-ttu-id="12a11-103">Ottenere o elencare appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="12a11-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="12a11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12a11-104">SYNTAX</span></span>

### <span data-ttu-id="12a11-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12a11-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12a11-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12a11-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12a11-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12a11-107">DESCRIPTION</span></span>
<span data-ttu-id="12a11-108">I Get-AzNetworkVirtualAppliance di rete recuperano o elencano le risorse di Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="12a11-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="12a11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12a11-109">EXAMPLES</span></span>

### <span data-ttu-id="12a11-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12a11-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="12a11-111">Ottenere una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="12a11-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="12a11-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12a11-112">PARAMETERS</span></span>

### <span data-ttu-id="12a11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a11-113">-DefaultProfile</span></span>
<span data-ttu-id="12a11-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12a11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12a11-115">-Name</span><span class="sxs-lookup"><span data-stu-id="12a11-115">-Name</span></span>
<span data-ttu-id="12a11-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="12a11-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a11-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a11-117">-ResourceGroupName</span></span>
<span data-ttu-id="12a11-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12a11-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a11-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12a11-119">-ResourceId</span></span>
<span data-ttu-id="12a11-120">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="12a11-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a11-121">CommonParameters</span></span>
<span data-ttu-id="12a11-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a11-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12a11-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a11-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="12a11-124">INPUTS</span></span>

### <span data-ttu-id="12a11-125">System.String</span><span class="sxs-lookup"><span data-stu-id="12a11-125">System.String</span></span>

## <span data-ttu-id="12a11-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12a11-126">OUTPUTS</span></span>

### <span data-ttu-id="12a11-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="12a11-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="12a11-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="12a11-128">NOTES</span></span>

## <span data-ttu-id="12a11-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12a11-129">RELATED LINKS</span></span>
