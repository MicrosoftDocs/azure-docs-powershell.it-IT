---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 45966042a2c2c6a660f052280039204a1d5eb908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988033"
---
# <span data-ttu-id="d5894-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d5894-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="d5894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5894-102">SYNOPSIS</span></span>
<span data-ttu-id="d5894-103">Ottiene un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5894-103">Gets a device twin.</span></span>

## <span data-ttu-id="d5894-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5894-104">SYNTAX</span></span>

### <span data-ttu-id="d5894-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5894-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5894-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5894-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5894-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5894-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5894-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5894-108">DESCRIPTION</span></span>
<span data-ttu-id="d5894-109">Ottiene un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5894-109">Gets a device twin.</span></span> <span data-ttu-id="d5894-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="d5894-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="d5894-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5894-111">EXAMPLES</span></span>

### <span data-ttu-id="d5894-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5894-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="d5894-113">Restituisce l'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5894-113">Returns the device twin object.</span></span>

## <span data-ttu-id="d5894-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5894-114">PARAMETERS</span></span>

### <span data-ttu-id="d5894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5894-115">-DefaultProfile</span></span>
<span data-ttu-id="d5894-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5894-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5894-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d5894-117">-DeviceId</span></span>
<span data-ttu-id="d5894-118">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d5894-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5894-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5894-119">-InputObject</span></span>
<span data-ttu-id="d5894-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d5894-120">IotHub object</span></span>

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

### <span data-ttu-id="d5894-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d5894-121">-IotHubName</span></span>
<span data-ttu-id="d5894-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="d5894-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d5894-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5894-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5894-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d5894-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5894-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5894-125">-ResourceId</span></span>
<span data-ttu-id="d5894-126">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d5894-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d5894-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5894-127">CommonParameters</span></span>
<span data-ttu-id="d5894-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5894-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5894-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5894-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5894-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5894-130">INPUTS</span></span>

### <span data-ttu-id="d5894-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d5894-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d5894-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d5894-132">System.String</span></span>

## <span data-ttu-id="d5894-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5894-133">OUTPUTS</span></span>

### <span data-ttu-id="d5894-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d5894-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="d5894-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5894-135">NOTES</span></span>

## <span data-ttu-id="d5894-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5894-136">RELATED LINKS</span></span>
