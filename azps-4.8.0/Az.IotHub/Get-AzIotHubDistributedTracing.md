---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192473"
---
# <span data-ttu-id="5f94d-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="5f94d-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="5f94d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f94d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f94d-103">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f94d-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="5f94d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f94d-104">SYNTAX</span></span>

### <span data-ttu-id="5f94d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f94d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f94d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f94d-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f94d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5f94d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f94d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f94d-108">DESCRIPTION</span></span>
<span data-ttu-id="5f94d-109">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f94d-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="5f94d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f94d-110">EXAMPLES</span></span>

### <span data-ttu-id="5f94d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5f94d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="5f94d-112">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f94d-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="5f94d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f94d-113">PARAMETERS</span></span>

### <span data-ttu-id="5f94d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f94d-114">-DefaultProfile</span></span>
<span data-ttu-id="5f94d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f94d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f94d-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5f94d-116">-DeviceId</span></span>
<span data-ttu-id="5f94d-117">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f94d-117">Target Device Id.</span></span>

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

### <span data-ttu-id="5f94d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f94d-118">-InputObject</span></span>
<span data-ttu-id="5f94d-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="5f94d-119">IotHub object</span></span>

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

### <span data-ttu-id="5f94d-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5f94d-120">-IotHubName</span></span>
<span data-ttu-id="5f94d-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="5f94d-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5f94d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f94d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f94d-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5f94d-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5f94d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f94d-124">-ResourceId</span></span>
<span data-ttu-id="5f94d-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="5f94d-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5f94d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f94d-126">CommonParameters</span></span>
<span data-ttu-id="5f94d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f94d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f94d-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f94d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f94d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f94d-129">INPUTS</span></span>

### <span data-ttu-id="5f94d-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5f94d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5f94d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5f94d-131">System.String</span></span>

## <span data-ttu-id="5f94d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f94d-132">OUTPUTS</span></span>

### <span data-ttu-id="5f94d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="5f94d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="5f94d-134">Note</span><span class="sxs-lookup"><span data-stu-id="5f94d-134">NOTES</span></span>

## <span data-ttu-id="5f94d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f94d-135">RELATED LINKS</span></span>
