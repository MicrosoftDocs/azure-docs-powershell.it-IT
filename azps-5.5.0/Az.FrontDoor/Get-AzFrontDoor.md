---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6cc7de36f51bc2fcb61950aa112c2f426358a506
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209523"
---
# <span data-ttu-id="c3940-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c3940-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="c3940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3940-102">SYNOPSIS</span></span>
<span data-ttu-id="c3940-103">Ottenere una bilanciamento del carico anteriore</span><span class="sxs-lookup"><span data-stu-id="c3940-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="c3940-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3940-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3940-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3940-105">DESCRIPTION</span></span>
<span data-ttu-id="c3940-106">Il **cmdlet Get-AzFrontDoorGet** ottiene tutte le porte anteriore esistenti nell'abbonamento corrente che corrispondono alle informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="c3940-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="c3940-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3940-107">EXAMPLES</span></span>

### <span data-ttu-id="c3940-108">Esempio 1: Ottenere tutti i FrontDoor nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="c3940-109">Ottieni tutti gli elementi FrontDoors nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="c3940-110">Esempio 2: Ottenere tutti i FrontDoor nel gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="c3940-111">Ottenere tutti i FrontDoor nel gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="c3940-112">Esempio 3: Ottenere i FrontDoors nel gruppo di risorse "rg1" con il nome "frontDoor1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
FrontDoorId           : {guid}
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="c3940-113">Ottenere i FrontDoor nel gruppo di risorse "rg1" con il nome "frontDoor1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="c3940-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="c3940-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3940-114">PARAMETERS</span></span>

### <span data-ttu-id="c3940-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3940-115">-DefaultProfile</span></span>
<span data-ttu-id="c3940-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3940-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3940-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c3940-117">-Name</span></span>
<span data-ttu-id="c3940-118">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="c3940-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3940-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3940-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3940-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3940-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3940-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3940-121">CommonParameters</span></span>
<span data-ttu-id="c3940-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3940-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3940-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3940-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3940-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3940-124">INPUTS</span></span>

### <span data-ttu-id="c3940-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3940-125">None</span></span>

## <span data-ttu-id="c3940-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3940-126">OUTPUTS</span></span>

### <span data-ttu-id="c3940-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c3940-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="c3940-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3940-128">NOTES</span></span>

## <span data-ttu-id="c3940-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3940-129">RELATED LINKS</span></span>

<span data-ttu-id="c3940-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="c3940-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
