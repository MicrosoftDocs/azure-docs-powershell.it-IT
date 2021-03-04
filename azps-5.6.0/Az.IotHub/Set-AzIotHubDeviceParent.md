---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955837"
---
# <span data-ttu-id="5a814-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="5a814-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="5a814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a814-102">SYNOPSIS</span></span>
<span data-ttu-id="5a814-103">Impostare il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="5a814-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="5a814-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a814-104">SYNTAX</span></span>

### <span data-ttu-id="5a814-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a814-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a814-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a814-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a814-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a814-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a814-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a814-108">DESCRIPTION</span></span>
<span data-ttu-id="5a814-109">Impostare il dispositivo padre del dispositivo non perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="5a814-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="5a814-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a814-110">EXAMPLES</span></span>

### <span data-ttu-id="5a814-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a814-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
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
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="5a814-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a814-112">PARAMETERS</span></span>

### <span data-ttu-id="5a814-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a814-113">-DefaultProfile</span></span>
<span data-ttu-id="5a814-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a814-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a814-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5a814-115">-DeviceId</span></span>
<span data-ttu-id="5a814-116">ID del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5a814-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="5a814-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a814-117">-Force</span></span>
<span data-ttu-id="5a814-118">Sovrascrive il dispositivo padre del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5a814-118">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a814-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a814-119">-InputObject</span></span>
<span data-ttu-id="5a814-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="5a814-120">IotHub object</span></span>

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

### <span data-ttu-id="5a814-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5a814-121">-IotHubName</span></span>
<span data-ttu-id="5a814-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="5a814-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5a814-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="5a814-123">-ParentDeviceId</span></span>
<span data-ttu-id="5a814-124">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="5a814-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a814-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a814-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a814-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5a814-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5a814-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a814-127">-ResourceId</span></span>
<span data-ttu-id="5a814-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="5a814-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5a814-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a814-129">-Confirm</span></span>
<span data-ttu-id="5a814-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a814-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a814-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a814-131">-WhatIf</span></span>
<span data-ttu-id="5a814-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a814-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a814-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a814-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a814-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a814-134">CommonParameters</span></span>
<span data-ttu-id="5a814-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a814-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a814-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a814-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a814-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a814-137">INPUTS</span></span>

### <span data-ttu-id="5a814-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5a814-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5a814-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5a814-139">System.String</span></span>

## <span data-ttu-id="5a814-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a814-140">OUTPUTS</span></span>

### <span data-ttu-id="5a814-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevaso</span><span class="sxs-lookup"><span data-stu-id="5a814-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="5a814-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a814-142">NOTES</span></span>

## <span data-ttu-id="5a814-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a814-143">RELATED LINKS</span></span>
