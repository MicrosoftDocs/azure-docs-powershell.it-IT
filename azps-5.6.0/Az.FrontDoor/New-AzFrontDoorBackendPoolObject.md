---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965902"
---
# <span data-ttu-id="c35d0-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="c35d0-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="c35d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c35d0-102">SYNOPSIS</span></span>
<span data-ttu-id="c35d0-103">Creare un oggetto PSBackendPool per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="c35d0-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="c35d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c35d0-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c35d0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c35d0-105">DESCRIPTION</span></span>
<span data-ttu-id="c35d0-106">Creare un oggetto PSBackendPool per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="c35d0-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="c35d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c35d0-107">EXAMPLES</span></span>

### <span data-ttu-id="c35d0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c35d0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="c35d0-109">Creare un oggetto PSBackendPool per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="c35d0-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="c35d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c35d0-110">PARAMETERS</span></span>

### <span data-ttu-id="c35d0-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="c35d0-111">-Backend</span></span>
<span data-ttu-id="c35d0-112">Set di back-end per il pool.</span><span class="sxs-lookup"><span data-stu-id="c35d0-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35d0-113">-DefaultProfile</span></span>
<span data-ttu-id="c35d0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c35d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c35d0-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c35d0-115">-FrontDoorName</span></span>
<span data-ttu-id="c35d0-116">Nome della porta a cui appartiene questa regola di routing.</span><span class="sxs-lookup"><span data-stu-id="c35d0-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="c35d0-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="c35d0-118">Nome delle impostazioni di integrità per questo pool back-end</span><span class="sxs-lookup"><span data-stu-id="c35d0-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="c35d0-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="c35d0-120">Nome delle impostazioni di bilanciamento del carico per questo pool back-end</span><span class="sxs-lookup"><span data-stu-id="c35d0-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c35d0-121">-Name</span></span>
<span data-ttu-id="c35d0-122">Nome BackendPool.</span><span class="sxs-lookup"><span data-stu-id="c35d0-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c35d0-124">Nome del gruppo di risorse con cui verrà creata la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="c35d0-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35d0-125">CommonParameters</span></span>
<span data-ttu-id="c35d0-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c35d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35d0-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c35d0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35d0-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c35d0-128">INPUTS</span></span>

### <span data-ttu-id="c35d0-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c35d0-129">None</span></span>

## <span data-ttu-id="c35d0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c35d0-130">OUTPUTS</span></span>

### <span data-ttu-id="c35d0-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="c35d0-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="c35d0-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c35d0-132">NOTES</span></span>

## <span data-ttu-id="c35d0-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c35d0-133">RELATED LINKS</span></span>

<span data-ttu-id="c35d0-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="c35d0-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
