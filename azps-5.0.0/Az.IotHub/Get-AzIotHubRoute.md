---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoute.md
ms.openlocfilehash: 6e72a889264efa82af343a0aab019cc3e5580dc7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203734"
---
# <span data-ttu-id="58b37-101">Get-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="58b37-101">Get-AzIotHubRoute</span></span>

## <span data-ttu-id="58b37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58b37-102">SYNOPSIS</span></span>
<span data-ttu-id="58b37-103">Ottenere informazioni sulla Route in hub molto</span><span class="sxs-lookup"><span data-stu-id="58b37-103">Get information about the route in IoT Hub</span></span>

## <span data-ttu-id="58b37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58b37-104">SYNTAX</span></span>

### <span data-ttu-id="58b37-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58b37-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58b37-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58b37-106">InputObjectSet</span></span>
```
Get-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58b37-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58b37-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58b37-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58b37-108">DESCRIPTION</span></span>
<span data-ttu-id="58b37-109">Ottenere informazioni sull'itinerario. È possibile ottenere tutte le route da un hub molto, ottenere route a un tipo di endpoint o ottenere route a un endpoint specifico.</span><span class="sxs-lookup"><span data-stu-id="58b37-109">Get information on the route.You can get all routes from an IoT Hub, get routes to a type of endpoint or get routes to a specific endpoint.</span></span>

## <span data-ttu-id="58b37-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58b37-110">EXAMPLES</span></span>

### <span data-ttu-id="58b37-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58b37-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub"

RouteName DataSource       EndpointNames IsEnabled
--------- ----------       ------------- ---------
R1        DeviceMessages   events        False
R2        TwinChangeEvents E1            True
```

<span data-ttu-id="58b37-112">Ottenere tutte le route da Hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="58b37-112">Get all route from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="58b37-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58b37-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="58b37-114">Ottenere informazioni sull'itinerario dall'hub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="58b37-114">Get route information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="58b37-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58b37-115">PARAMETERS</span></span>

### <span data-ttu-id="58b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b37-116">-DefaultProfile</span></span>
<span data-ttu-id="58b37-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b37-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58b37-118">-InputObject</span></span>
<span data-ttu-id="58b37-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="58b37-119">IotHub Object</span></span>

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

### <span data-ttu-id="58b37-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="58b37-120">-Name</span></span>
<span data-ttu-id="58b37-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="58b37-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="58b37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b37-122">-ResourceGroupName</span></span>
<span data-ttu-id="58b37-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="58b37-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58b37-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58b37-124">-ResourceId</span></span>
<span data-ttu-id="58b37-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="58b37-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="58b37-126">-RouteName</span><span class="sxs-lookup"><span data-stu-id="58b37-126">-RouteName</span></span>
<span data-ttu-id="58b37-127">Nome della route</span><span class="sxs-lookup"><span data-stu-id="58b37-127">Name of the Route</span></span>

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

### <span data-ttu-id="58b37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b37-128">CommonParameters</span></span>
<span data-ttu-id="58b37-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b37-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b37-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b37-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58b37-131">INPUTS</span></span>

### <span data-ttu-id="58b37-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="58b37-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="58b37-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58b37-133">System.String</span></span>

## <span data-ttu-id="58b37-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58b37-134">OUTPUTS</span></span>

### <span data-ttu-id="58b37-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="58b37-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

### <span data-ttu-id="58b37-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteProperties []</span><span class="sxs-lookup"><span data-stu-id="58b37-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="58b37-137">Note</span><span class="sxs-lookup"><span data-stu-id="58b37-137">NOTES</span></span>

## <span data-ttu-id="58b37-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58b37-138">RELATED LINKS</span></span>
