---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: 290b2ddcea6812b840b9c19ad2d44c4a0e461e64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988020"
---
# <span data-ttu-id="fce51-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="fce51-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="fce51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce51-102">SYNOPSIS</span></span>
<span data-ttu-id="fce51-103">Ottenere le impostazioni delle traccia distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fce51-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fce51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fce51-104">SYNTAX</span></span>

### <span data-ttu-id="fce51-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fce51-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fce51-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fce51-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fce51-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fce51-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fce51-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fce51-108">DESCRIPTION</span></span>
<span data-ttu-id="fce51-109">Ottenere le impostazioni delle traccia distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fce51-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fce51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fce51-110">EXAMPLES</span></span>

### <span data-ttu-id="fce51-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fce51-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="fce51-112">Ottenere le impostazioni delle traccia distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fce51-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="fce51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fce51-113">PARAMETERS</span></span>

### <span data-ttu-id="fce51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce51-114">-DefaultProfile</span></span>
<span data-ttu-id="fce51-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fce51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fce51-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fce51-116">-DeviceId</span></span>
<span data-ttu-id="fce51-117">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fce51-117">Target Device Id.</span></span>

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

### <span data-ttu-id="fce51-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fce51-118">-InputObject</span></span>
<span data-ttu-id="fce51-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fce51-119">IotHub object</span></span>

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

### <span data-ttu-id="fce51-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fce51-120">-IotHubName</span></span>
<span data-ttu-id="fce51-121">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="fce51-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fce51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce51-122">-ResourceGroupName</span></span>
<span data-ttu-id="fce51-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fce51-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fce51-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fce51-124">-ResourceId</span></span>
<span data-ttu-id="fce51-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fce51-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fce51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce51-126">CommonParameters</span></span>
<span data-ttu-id="fce51-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce51-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce51-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce51-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="fce51-129">INPUTS</span></span>

### <span data-ttu-id="fce51-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fce51-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fce51-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fce51-131">System.String</span></span>

## <span data-ttu-id="fce51-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fce51-132">OUTPUTS</span></span>

### <span data-ttu-id="fce51-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceT più elettronica</span><span class="sxs-lookup"><span data-stu-id="fce51-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="fce51-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="fce51-134">NOTES</span></span>

## <span data-ttu-id="fce51-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fce51-135">RELATED LINKS</span></span>
