---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020951"
---
# <span data-ttu-id="c7060-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="c7060-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="c7060-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7060-102">SYNOPSIS</span></span>
<span data-ttu-id="c7060-103">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7060-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c7060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7060-104">SYNTAX</span></span>

### <span data-ttu-id="c7060-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7060-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7060-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7060-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7060-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c7060-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7060-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7060-108">DESCRIPTION</span></span>
<span data-ttu-id="c7060-109">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7060-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c7060-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7060-110">EXAMPLES</span></span>

### <span data-ttu-id="c7060-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7060-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="c7060-112">Ottenere le impostazioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7060-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="c7060-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7060-113">PARAMETERS</span></span>

### <span data-ttu-id="c7060-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7060-114">-DefaultProfile</span></span>
<span data-ttu-id="c7060-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7060-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7060-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c7060-116">-DeviceId</span></span>
<span data-ttu-id="c7060-117">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c7060-117">Target Device Id.</span></span>

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

### <span data-ttu-id="c7060-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7060-118">-InputObject</span></span>
<span data-ttu-id="c7060-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="c7060-119">IotHub object</span></span>

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

### <span data-ttu-id="c7060-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c7060-120">-IotHubName</span></span>
<span data-ttu-id="c7060-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="c7060-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c7060-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7060-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7060-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c7060-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c7060-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7060-124">-ResourceId</span></span>
<span data-ttu-id="c7060-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="c7060-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c7060-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7060-126">CommonParameters</span></span>
<span data-ttu-id="c7060-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7060-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7060-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7060-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7060-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7060-129">INPUTS</span></span>

### <span data-ttu-id="c7060-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c7060-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c7060-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c7060-131">System.String</span></span>

## <span data-ttu-id="c7060-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7060-132">OUTPUTS</span></span>

### <span data-ttu-id="c7060-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="c7060-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="c7060-134">Note</span><span class="sxs-lookup"><span data-stu-id="c7060-134">NOTES</span></span>

## <span data-ttu-id="c7060-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7060-135">RELATED LINKS</span></span>
