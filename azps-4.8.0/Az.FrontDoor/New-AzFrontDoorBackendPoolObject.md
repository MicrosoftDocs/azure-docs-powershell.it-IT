---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031225"
---
# <span data-ttu-id="a6db8-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="a6db8-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="a6db8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6db8-102">SYNOPSIS</span></span>
<span data-ttu-id="a6db8-103">Creare un oggetto PSBackendPool per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a6db8-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="a6db8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6db8-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6db8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6db8-105">DESCRIPTION</span></span>
<span data-ttu-id="a6db8-106">Creare un oggetto PSBackendPool per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a6db8-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="a6db8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6db8-107">EXAMPLES</span></span>

### <span data-ttu-id="a6db8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6db8-108">Example 1</span></span>
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

<span data-ttu-id="a6db8-109">Creare un oggetto PSBackendPool per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="a6db8-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="a6db8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6db8-110">PARAMETERS</span></span>

### <span data-ttu-id="a6db8-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="a6db8-111">-Backend</span></span>
<span data-ttu-id="a6db8-112">Il set di backend per questo pool.</span><span class="sxs-lookup"><span data-stu-id="a6db8-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="a6db8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6db8-113">-DefaultProfile</span></span>
<span data-ttu-id="a6db8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6db8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6db8-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a6db8-115">-FrontDoorName</span></span>
<span data-ttu-id="a6db8-116">Nome dello sportello anteriore a cui appartiene la regola di routing.</span><span class="sxs-lookup"><span data-stu-id="a6db8-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="a6db8-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="a6db8-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="a6db8-118">Nome delle impostazioni della sonda di integrità per il pool di backend</span><span class="sxs-lookup"><span data-stu-id="a6db8-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="a6db8-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="a6db8-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="a6db8-120">Nome delle impostazioni di bilanciamento del carico per il pool back-end</span><span class="sxs-lookup"><span data-stu-id="a6db8-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="a6db8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6db8-121">-Name</span></span>
<span data-ttu-id="a6db8-122">Nome BackendPool.</span><span class="sxs-lookup"><span data-stu-id="a6db8-122">BackendPool name.</span></span>

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

### <span data-ttu-id="a6db8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6db8-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6db8-124">Nome del gruppo di risorse in cui verrà creato il RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="a6db8-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="a6db8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6db8-125">CommonParameters</span></span>
<span data-ttu-id="a6db8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6db8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6db8-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6db8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6db8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6db8-128">INPUTS</span></span>

### <span data-ttu-id="a6db8-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6db8-129">None</span></span>

## <span data-ttu-id="a6db8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6db8-130">OUTPUTS</span></span>

### <span data-ttu-id="a6db8-131">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="a6db8-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="a6db8-132">Note</span><span class="sxs-lookup"><span data-stu-id="a6db8-132">NOTES</span></span>

## <span data-ttu-id="a6db8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6db8-133">RELATED LINKS</span></span>

<span data-ttu-id="a6db8-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="a6db8-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
