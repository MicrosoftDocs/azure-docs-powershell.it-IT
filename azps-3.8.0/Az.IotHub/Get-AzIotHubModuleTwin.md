---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021793"
---
# <span data-ttu-id="11898-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="11898-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="11898-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11898-102">SYNOPSIS</span></span>
<span data-ttu-id="11898-103">Ottiene un modulo di dispositivo molto Twin.</span><span class="sxs-lookup"><span data-stu-id="11898-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="11898-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11898-104">SYNTAX</span></span>

### <span data-ttu-id="11898-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11898-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11898-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="11898-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11898-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="11898-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11898-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11898-108">DESCRIPTION</span></span>
<span data-ttu-id="11898-109">Ottiene un modulo di dispositivo molto Twin.</span><span class="sxs-lookup"><span data-stu-id="11898-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="11898-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="11898-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="11898-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11898-111">EXAMPLES</span></span>

### <span data-ttu-id="11898-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11898-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="11898-113">Restituisce l'oggetto Twin del modulo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11898-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="11898-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11898-114">PARAMETERS</span></span>

### <span data-ttu-id="11898-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11898-115">-DefaultProfile</span></span>
<span data-ttu-id="11898-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11898-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11898-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="11898-117">-DeviceId</span></span>
<span data-ttu-id="11898-118">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11898-118">Target Device Id.</span></span>

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

### <span data-ttu-id="11898-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11898-119">-InputObject</span></span>
<span data-ttu-id="11898-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="11898-120">IotHub object</span></span>

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

### <span data-ttu-id="11898-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="11898-121">-IotHubName</span></span>
<span data-ttu-id="11898-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="11898-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="11898-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="11898-123">-ModuleId</span></span>
<span data-ttu-id="11898-124">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="11898-124">Target Module Id.</span></span>

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

### <span data-ttu-id="11898-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11898-125">-ResourceGroupName</span></span>
<span data-ttu-id="11898-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="11898-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="11898-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11898-127">-ResourceId</span></span>
<span data-ttu-id="11898-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="11898-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="11898-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11898-129">CommonParameters</span></span>
<span data-ttu-id="11898-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11898-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11898-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11898-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11898-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11898-132">INPUTS</span></span>

### <span data-ttu-id="11898-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="11898-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="11898-134">System. String</span><span class="sxs-lookup"><span data-stu-id="11898-134">System.String</span></span>

## <span data-ttu-id="11898-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11898-135">OUTPUTS</span></span>

### <span data-ttu-id="11898-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="11898-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="11898-137">Note</span><span class="sxs-lookup"><span data-stu-id="11898-137">NOTES</span></span>

## <span data-ttu-id="11898-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11898-138">RELATED LINKS</span></span>
