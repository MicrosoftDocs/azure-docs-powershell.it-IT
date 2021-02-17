---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180518"
---
# <span data-ttu-id="b5a28-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="b5a28-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="b5a28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5a28-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a28-103">Impostare il dispositivo padre del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="b5a28-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="b5a28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5a28-104">SYNTAX</span></span>

### <span data-ttu-id="b5a28-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5a28-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5a28-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b5a28-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5a28-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b5a28-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5a28-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5a28-108">DESCRIPTION</span></span>
<span data-ttu-id="b5a28-109">Impostare il dispositivo padre del dispositivo non perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="b5a28-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="b5a28-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5a28-110">EXAMPLES</span></span>

### <span data-ttu-id="b5a28-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b5a28-111">Example 1</span></span>
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

## <span data-ttu-id="b5a28-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5a28-112">PARAMETERS</span></span>

### <span data-ttu-id="b5a28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a28-113">-DefaultProfile</span></span>
<span data-ttu-id="b5a28-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5a28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5a28-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b5a28-115">-DeviceId</span></span>
<span data-ttu-id="b5a28-116">ID del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="b5a28-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="b5a28-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b5a28-117">-Force</span></span>
<span data-ttu-id="b5a28-118">Sovrascrive il dispositivo padre del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="b5a28-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="b5a28-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5a28-119">-InputObject</span></span>
<span data-ttu-id="b5a28-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b5a28-120">IotHub object</span></span>

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

### <span data-ttu-id="b5a28-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b5a28-121">-IotHubName</span></span>
<span data-ttu-id="b5a28-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="b5a28-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b5a28-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="b5a28-123">-ParentDeviceId</span></span>
<span data-ttu-id="b5a28-124">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="b5a28-124">Id of edge device.</span></span>

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

### <span data-ttu-id="b5a28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5a28-125">-ResourceGroupName</span></span>
<span data-ttu-id="b5a28-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b5a28-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b5a28-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5a28-127">-ResourceId</span></span>
<span data-ttu-id="b5a28-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b5a28-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b5a28-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5a28-129">-Confirm</span></span>
<span data-ttu-id="b5a28-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5a28-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a28-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a28-131">-WhatIf</span></span>
<span data-ttu-id="b5a28-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5a28-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5a28-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5a28-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a28-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a28-134">CommonParameters</span></span>
<span data-ttu-id="b5a28-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5a28-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a28-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a28-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a28-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5a28-137">INPUTS</span></span>

### <span data-ttu-id="b5a28-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b5a28-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b5a28-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b5a28-139">System.String</span></span>

## <span data-ttu-id="b5a28-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5a28-140">OUTPUTS</span></span>

### <span data-ttu-id="b5a28-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="b5a28-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="b5a28-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5a28-142">NOTES</span></span>

## <span data-ttu-id="b5a28-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5a28-143">RELATED LINKS</span></span>
