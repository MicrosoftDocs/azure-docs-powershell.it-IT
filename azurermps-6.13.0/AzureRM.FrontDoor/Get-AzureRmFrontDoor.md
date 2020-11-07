---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686396"
---
# <span data-ttu-id="de423-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="de423-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="de423-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de423-102">SYNOPSIS</span></span>
<span data-ttu-id="de423-103">Ottenere il bilanciamento del carico della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="de423-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de423-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de423-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de423-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de423-105">DESCRIPTION</span></span>
<span data-ttu-id="de423-106">Il cmdletGet **Get-AzureRmFrontDoor** ottiene tutte le porte anteriori esistenti nell'abbonamento corrente che corrisponde alle informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="de423-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="de423-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de423-107">EXAMPLES</span></span>

### <span data-ttu-id="de423-108">Esempio 1: ottenere tutti i FrontDoors nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

FriendlyName          : frontdoor1
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

<span data-ttu-id="de423-109">Ottenere tutti i FrontDoors nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="de423-110">Esempio 2: ottenere tutti i FrontDoors nel gruppo di risorse "RG1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
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

<span data-ttu-id="de423-111">Ottenere tutti i FrontDoors nel gruppo di risorse "RG1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="de423-112">Esempio 3: ottenere il FrontDoors nel gruppo di risorse "RG1" con il nome "frontDoor1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
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

<span data-ttu-id="de423-113">Ottenere il FrontDoors nel gruppo di risorse "RG1" con il nome "frontDoor1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="de423-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="de423-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de423-114">PARAMETERS</span></span>

### <span data-ttu-id="de423-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de423-115">-DefaultProfile</span></span>
<span data-ttu-id="de423-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de423-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de423-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="de423-117">-Name</span></span>
<span data-ttu-id="de423-118">Nome porta principale.</span><span class="sxs-lookup"><span data-stu-id="de423-118">Front Door name.</span></span>

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

### <span data-ttu-id="de423-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de423-119">-ResourceGroupName</span></span>
<span data-ttu-id="de423-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de423-120">The resource group name.</span></span>

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

### <span data-ttu-id="de423-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de423-121">CommonParameters</span></span>
<span data-ttu-id="de423-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de423-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de423-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de423-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de423-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de423-124">INPUTS</span></span>

### <span data-ttu-id="de423-125">System. String</span><span class="sxs-lookup"><span data-stu-id="de423-125">System.String</span></span>

## <span data-ttu-id="de423-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de423-126">OUTPUTS</span></span>

### <span data-ttu-id="de423-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="de423-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="de423-128">Note</span><span class="sxs-lookup"><span data-stu-id="de423-128">NOTES</span></span>

## <span data-ttu-id="de423-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de423-129">RELATED LINKS</span></span>

<span data-ttu-id="de423-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="de423-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
