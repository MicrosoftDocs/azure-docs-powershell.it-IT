---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRoute.md
ms.openlocfilehash: 0711bd1d6290191c2d5311a7375e6f81c4ecd573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687849"
---
# <span data-ttu-id="d9803-101">Get-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="d9803-101">Get-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="d9803-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9803-102">SYNOPSIS</span></span>
<span data-ttu-id="d9803-103">Ottenere informazioni sulla Route in hub molto</span><span class="sxs-lookup"><span data-stu-id="d9803-103">Get information about the route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9803-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9803-104">SYNTAX</span></span>

### <span data-ttu-id="d9803-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9803-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9803-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9803-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9803-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9803-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9803-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9803-108">DESCRIPTION</span></span>
<span data-ttu-id="d9803-109">Ottenere informazioni sull'itinerario. È possibile ottenere tutte le route da un hub molto, ottenere route a un tipo di endpoint o ottenere route a un endpoint specifico.</span><span class="sxs-lookup"><span data-stu-id="d9803-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="d9803-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9803-110">EXAMPLES</span></span>

### <span data-ttu-id="d9803-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9803-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="d9803-112">Ottenere tutte le route da Hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d9803-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="d9803-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d9803-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="d9803-114">Ottenere informazioni sull'itinerario dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="d9803-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="d9803-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9803-115">PARAMETERS</span></span>

### <span data-ttu-id="d9803-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9803-116">-DefaultProfile</span></span>
<span data-ttu-id="d9803-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9803-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9803-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9803-118">-InputObject</span></span>
<span data-ttu-id="d9803-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d9803-119">IotHub Object</span></span>

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

### <span data-ttu-id="d9803-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9803-120">-Name</span></span>
<span data-ttu-id="d9803-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="d9803-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9803-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9803-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9803-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9803-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9803-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9803-124">-ResourceId</span></span>
<span data-ttu-id="d9803-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d9803-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9803-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="d9803-126">-RouteName</span></span>
<span data-ttu-id="d9803-127">Nome della route</span><span class="sxs-lookup"><span data-stu-id="d9803-127">Name of the Route</span></span>

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

### <span data-ttu-id="d9803-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9803-128">CommonParameters</span></span>
<span data-ttu-id="d9803-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9803-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9803-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9803-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9803-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9803-131">INPUTS</span></span>

### <span data-ttu-id="d9803-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9803-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="d9803-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d9803-133">System.String</span></span>

## <span data-ttu-id="d9803-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9803-134">OUTPUTS</span></span>

### <span data-ttu-id="d9803-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="d9803-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>
<span data-ttu-id="d9803-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties, Microsoft. Azure. Commands. IotHub, Version = 3.1.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d9803-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d9803-137">Note</span><span class="sxs-lookup"><span data-stu-id="d9803-137">NOTES</span></span>

## <span data-ttu-id="d9803-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9803-138">RELATED LINKS</span></span>
