---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201211"
---
# <span data-ttu-id="d9470-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d9470-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="d9470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9470-102">SYNOPSIS</span></span>
<span data-ttu-id="d9470-103">Ottiene un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="d9470-103">Gets a device twin.</span></span>

## <span data-ttu-id="d9470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9470-104">SYNTAX</span></span>

### <span data-ttu-id="d9470-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9470-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9470-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9470-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9470-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9470-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9470-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9470-108">DESCRIPTION</span></span>
<span data-ttu-id="d9470-109">Ottiene un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="d9470-109">Gets a device twin.</span></span> <span data-ttu-id="d9470-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="d9470-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="d9470-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9470-111">EXAMPLES</span></span>

### <span data-ttu-id="d9470-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9470-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="d9470-113">Restituisce l'oggetto Twin del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9470-113">Returns the device twin object.</span></span>

## <span data-ttu-id="d9470-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9470-114">PARAMETERS</span></span>

### <span data-ttu-id="d9470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9470-115">-DefaultProfile</span></span>
<span data-ttu-id="d9470-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9470-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9470-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d9470-117">-DeviceId</span></span>
<span data-ttu-id="d9470-118">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9470-118">Target Device Id.</span></span>

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

### <span data-ttu-id="d9470-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9470-119">-InputObject</span></span>
<span data-ttu-id="d9470-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d9470-120">IotHub object</span></span>

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

### <span data-ttu-id="d9470-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d9470-121">-IotHubName</span></span>
<span data-ttu-id="d9470-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="d9470-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9470-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9470-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9470-124">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9470-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9470-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9470-125">-ResourceId</span></span>
<span data-ttu-id="d9470-126">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d9470-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9470-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9470-127">CommonParameters</span></span>
<span data-ttu-id="d9470-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9470-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9470-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9470-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9470-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9470-130">INPUTS</span></span>

### <span data-ttu-id="d9470-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9470-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d9470-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d9470-132">System.String</span></span>

## <span data-ttu-id="d9470-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9470-133">OUTPUTS</span></span>

### <span data-ttu-id="d9470-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="d9470-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="d9470-135">Note</span><span class="sxs-lookup"><span data-stu-id="d9470-135">NOTES</span></span>

## <span data-ttu-id="d9470-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9470-136">RELATED LINKS</span></span>
