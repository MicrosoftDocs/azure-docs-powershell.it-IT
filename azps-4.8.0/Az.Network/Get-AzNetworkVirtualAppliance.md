---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 657ffd65bd6dd477700002862060b931979de456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189046"
---
# <span data-ttu-id="2f10a-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2f10a-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="2f10a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2f10a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f10a-103">Ottenere o elencare gli elettrodomestici virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="2f10a-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="2f10a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f10a-104">SYNTAX</span></span>

### <span data-ttu-id="2f10a-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2f10a-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f10a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f10a-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f10a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f10a-107">DESCRIPTION</span></span>
<span data-ttu-id="2f10a-108">I comandi Get-AzNetworkVirtualAppliance ottengono o elencano le risorse di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="2f10a-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="2f10a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f10a-109">EXAMPLES</span></span>

### <span data-ttu-id="2f10a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2f10a-110">Example 1</span></span>
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

<span data-ttu-id="2f10a-111">Ottenere una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="2f10a-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2f10a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2f10a-112">PARAMETERS</span></span>

### <span data-ttu-id="2f10a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f10a-113">-DefaultProfile</span></span>
<span data-ttu-id="2f10a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f10a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f10a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f10a-115">-Name</span></span>
<span data-ttu-id="2f10a-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f10a-116">The resource name.</span></span>

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

### <span data-ttu-id="2f10a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f10a-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f10a-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2f10a-118">The resource group name.</span></span>

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

### <span data-ttu-id="2f10a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f10a-119">-ResourceId</span></span>
<span data-ttu-id="2f10a-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f10a-120">The resource Id.</span></span>

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

### <span data-ttu-id="2f10a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f10a-121">CommonParameters</span></span>
<span data-ttu-id="2f10a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f10a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f10a-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f10a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f10a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2f10a-124">INPUTS</span></span>

### <span data-ttu-id="2f10a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f10a-125">System.String</span></span>

## <span data-ttu-id="2f10a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f10a-126">OUTPUTS</span></span>

### <span data-ttu-id="2f10a-127">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="2f10a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="2f10a-128">Note</span><span class="sxs-lookup"><span data-stu-id="2f10a-128">NOTES</span></span>

## <span data-ttu-id="2f10a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f10a-129">RELATED LINKS</span></span>
