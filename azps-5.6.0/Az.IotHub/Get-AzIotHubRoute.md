---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: d627460da42d5d5710aa9931d2e831320378b082
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987880"
---
# <span data-ttu-id="06a10-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="06a10-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="06a10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a10-102">SYNOPSIS</span></span>
<span data-ttu-id="06a10-103">Ottenere informazioni sul percorso nell'Hub IoT</span><span class="sxs-lookup"><span data-stu-id="06a10-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="06a10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06a10-104">SYNTAX</span></span>

### <span data-ttu-id="06a10-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06a10-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06a10-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="06a10-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06a10-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="06a10-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06a10-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06a10-108">DESCRIPTION</span></span>
<span data-ttu-id="06a10-109">Ottenere informazioni sul percorso. È possibile ottenere tutte le route da un Hub IoT, ottenere route a un tipo di endpoint o a uno specifico endpoint.</span><span class="sxs-lookup"><span data-stu-id="06a10-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="06a10-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06a10-110">EXAMPLES</span></span>

### <span data-ttu-id="06a10-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="06a10-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="06a10-112">Ottenere tutte le route dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="06a10-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="06a10-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="06a10-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="06a10-114">Ottenere informazioni sulle route dall'Hub IoT di "myiothub".</span><span class="sxs-lookup"><span data-stu-id="06a10-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="06a10-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06a10-115">PARAMETERS</span></span>

### <span data-ttu-id="06a10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a10-116">-DefaultProfile</span></span>
<span data-ttu-id="06a10-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06a10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06a10-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a10-118">-InputObject</span></span>
<span data-ttu-id="06a10-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="06a10-119">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06a10-120">-Name</span><span class="sxs-lookup"><span data-stu-id="06a10-120">-Name</span></span>
<span data-ttu-id="06a10-121">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="06a10-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a10-122">-ResourceGroupName</span></span>
<span data-ttu-id="06a10-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="06a10-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a10-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06a10-124">-ResourceId</span></span>
<span data-ttu-id="06a10-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="06a10-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a10-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="06a10-126">-RouteName</span></span>
<span data-ttu-id="06a10-127">Nome del percorso</span><span class="sxs-lookup"><span data-stu-id="06a10-127">Name of the Route</span></span>

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

### <span data-ttu-id="06a10-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a10-128">CommonParameters</span></span>
<span data-ttu-id="06a10-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a10-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a10-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a10-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a10-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="06a10-131">INPUTS</span></span>

### <span data-ttu-id="06a10-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="06a10-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="06a10-133">System.String</span><span class="sxs-lookup"><span data-stu-id="06a10-133">System.String</span></span>

## <span data-ttu-id="06a10-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06a10-134">OUTPUTS</span></span>

### <span data-ttu-id="06a10-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="06a10-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="06a10-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span><span class="sxs-lookup"><span data-stu-id="06a10-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="06a10-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="06a10-137">NOTES</span></span>

## <span data-ttu-id="06a10-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06a10-138">RELATED LINKS</span></span>
