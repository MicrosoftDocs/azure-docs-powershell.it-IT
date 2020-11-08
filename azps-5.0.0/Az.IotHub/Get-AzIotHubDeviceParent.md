---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201212"
---
# <span data-ttu-id="9c225-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="9c225-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="9c225-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c225-102">SYNOPSIS</span></span>
<span data-ttu-id="9c225-103">Ottenere il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="9c225-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="9c225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c225-104">SYNTAX</span></span>

### <span data-ttu-id="9c225-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c225-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c225-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9c225-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c225-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9c225-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c225-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c225-108">DESCRIPTION</span></span>
<span data-ttu-id="9c225-109">Ottenere il dispositivo padre del dispositivo non Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="9c225-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="9c225-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c225-110">EXAMPLES</span></span>

### <span data-ttu-id="9c225-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c225-111">Example 1</span></span>
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

<span data-ttu-id="9c225-112">Ottenere il dispositivo padre del dispositivo non Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="9c225-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="9c225-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c225-113">PARAMETERS</span></span>

### <span data-ttu-id="9c225-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c225-114">-DefaultProfile</span></span>
<span data-ttu-id="9c225-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c225-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c225-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9c225-116">-DeviceId</span></span>
<span data-ttu-id="9c225-117">ID del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="9c225-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="9c225-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c225-118">-InputObject</span></span>
<span data-ttu-id="9c225-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="9c225-119">IotHub object</span></span>

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

### <span data-ttu-id="9c225-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9c225-120">-IotHubName</span></span>
<span data-ttu-id="9c225-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="9c225-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9c225-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c225-122">-ResourceGroupName</span></span>
<span data-ttu-id="9c225-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9c225-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9c225-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c225-124">-ResourceId</span></span>
<span data-ttu-id="9c225-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="9c225-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9c225-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c225-126">CommonParameters</span></span>
<span data-ttu-id="9c225-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c225-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c225-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c225-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c225-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c225-129">INPUTS</span></span>

### <span data-ttu-id="9c225-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9c225-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9c225-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9c225-131">System.String</span></span>

## <span data-ttu-id="9c225-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c225-132">OUTPUTS</span></span>

### <span data-ttu-id="9c225-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="9c225-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="9c225-134">Note</span><span class="sxs-lookup"><span data-stu-id="9c225-134">NOTES</span></span>

## <span data-ttu-id="9c225-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c225-135">RELATED LINKS</span></span>
