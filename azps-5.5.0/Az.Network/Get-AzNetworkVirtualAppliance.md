---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191951"
---
# <span data-ttu-id="16222-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="16222-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="16222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16222-102">SYNOPSIS</span></span>
<span data-ttu-id="16222-103">Ottenere o elencare appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="16222-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="16222-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16222-104">SYNTAX</span></span>

### <span data-ttu-id="16222-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16222-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16222-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="16222-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16222-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16222-107">DESCRIPTION</span></span>
<span data-ttu-id="16222-108">I Get-AzNetworkVirtualAppliance di rete recuperano o elencano le risorse di Network Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="16222-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="16222-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16222-109">EXAMPLES</span></span>

### <span data-ttu-id="16222-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16222-110">Example 1</span></span>
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

<span data-ttu-id="16222-111">Ottenere una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="16222-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="16222-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16222-112">PARAMETERS</span></span>

### <span data-ttu-id="16222-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16222-113">-DefaultProfile</span></span>
<span data-ttu-id="16222-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16222-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16222-115">-Name</span><span class="sxs-lookup"><span data-stu-id="16222-115">-Name</span></span>
<span data-ttu-id="16222-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="16222-116">The resource name.</span></span>

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

### <span data-ttu-id="16222-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16222-117">-ResourceGroupName</span></span>
<span data-ttu-id="16222-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16222-118">The resource group name.</span></span>

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

### <span data-ttu-id="16222-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16222-119">-ResourceId</span></span>
<span data-ttu-id="16222-120">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="16222-120">The resource Id.</span></span>

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

### <span data-ttu-id="16222-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16222-121">CommonParameters</span></span>
<span data-ttu-id="16222-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16222-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16222-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="16222-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16222-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="16222-124">INPUTS</span></span>

### <span data-ttu-id="16222-125">System.String</span><span class="sxs-lookup"><span data-stu-id="16222-125">System.String</span></span>

## <span data-ttu-id="16222-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16222-126">OUTPUTS</span></span>

### <span data-ttu-id="16222-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="16222-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="16222-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="16222-128">NOTES</span></span>

## <span data-ttu-id="16222-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16222-129">RELATED LINKS</span></span>
