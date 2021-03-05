---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 06eb84ea854e9c0262f6f3e00e3e13e90f630baa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988061"
---
# <span data-ttu-id="e5787-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="e5787-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="e5787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5787-102">SYNOPSIS</span></span>
<span data-ttu-id="e5787-103">Ottenere il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="e5787-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="e5787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5787-104">SYNTAX</span></span>

### <span data-ttu-id="e5787-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5787-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5787-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e5787-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5787-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e5787-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5787-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5787-108">DESCRIPTION</span></span>
<span data-ttu-id="e5787-109">Ottenere il dispositivo padre del dispositivo non perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="e5787-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="e5787-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5787-110">EXAMPLES</span></span>

### <span data-ttu-id="e5787-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5787-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="e5787-112">Ottenere il dispositivo padre del dispositivo non perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="e5787-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="e5787-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5787-113">PARAMETERS</span></span>

### <span data-ttu-id="e5787-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5787-114">-DefaultProfile</span></span>
<span data-ttu-id="e5787-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5787-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5787-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e5787-116">-DeviceId</span></span>
<span data-ttu-id="e5787-117">ID del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="e5787-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="e5787-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5787-118">-InputObject</span></span>
<span data-ttu-id="e5787-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="e5787-119">IotHub object</span></span>

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

### <span data-ttu-id="e5787-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e5787-120">-IotHubName</span></span>
<span data-ttu-id="e5787-121">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="e5787-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e5787-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5787-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5787-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e5787-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e5787-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5787-124">-ResourceId</span></span>
<span data-ttu-id="e5787-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="e5787-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e5787-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5787-126">CommonParameters</span></span>
<span data-ttu-id="e5787-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5787-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5787-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5787-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5787-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5787-129">INPUTS</span></span>

### <span data-ttu-id="e5787-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e5787-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e5787-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e5787-131">System.String</span></span>

## <span data-ttu-id="e5787-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5787-132">OUTPUTS</span></span>

### <span data-ttu-id="e5787-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevaso</span><span class="sxs-lookup"><span data-stu-id="e5787-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="e5787-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5787-134">NOTES</span></span>

## <span data-ttu-id="e5787-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5787-135">RELATED LINKS</span></span>
