---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180526"
---
# <span data-ttu-id="2416d-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="2416d-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="2416d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2416d-102">SYNOPSIS</span></span>
<span data-ttu-id="2416d-103">Eliminare un dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2416d-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="2416d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2416d-104">SYNTAX</span></span>

### <span data-ttu-id="2416d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2416d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2416d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2416d-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2416d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2416d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2416d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2416d-108">DESCRIPTION</span></span>
<span data-ttu-id="2416d-109">Eliminare tutti i dispositivi o un dispositivo specifico da un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="2416d-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="2416d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2416d-110">EXAMPLES</span></span>

### <span data-ttu-id="2416d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2416d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="2416d-112">Eliminare tutti i dispositivi hub Iot.</span><span class="sxs-lookup"><span data-stu-id="2416d-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="2416d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2416d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="2416d-114">Eliminare un dispositivo Iot Hub.</span><span class="sxs-lookup"><span data-stu-id="2416d-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="2416d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2416d-115">PARAMETERS</span></span>

### <span data-ttu-id="2416d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2416d-116">-DefaultProfile</span></span>
<span data-ttu-id="2416d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2416d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2416d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2416d-118">-DeviceId</span></span>
<span data-ttu-id="2416d-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2416d-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2416d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2416d-120">-InputObject</span></span>
<span data-ttu-id="2416d-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="2416d-121">IotHub object</span></span>

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

### <span data-ttu-id="2416d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2416d-122">-IotHubName</span></span>
<span data-ttu-id="2416d-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="2416d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2416d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2416d-124">-PassThru</span></span>
<span data-ttu-id="2416d-125">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="2416d-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="2416d-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2416d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2416d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2416d-127">-ResourceGroupName</span></span>
<span data-ttu-id="2416d-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2416d-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2416d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2416d-129">-ResourceId</span></span>
<span data-ttu-id="2416d-130">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="2416d-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2416d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2416d-131">-Confirm</span></span>
<span data-ttu-id="2416d-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2416d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2416d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2416d-133">-WhatIf</span></span>
<span data-ttu-id="2416d-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2416d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2416d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2416d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2416d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2416d-136">CommonParameters</span></span>
<span data-ttu-id="2416d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2416d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2416d-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2416d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2416d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="2416d-139">INPUTS</span></span>

### <span data-ttu-id="2416d-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2416d-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2416d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2416d-141">System.String</span></span>

## <span data-ttu-id="2416d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2416d-142">OUTPUTS</span></span>

### <span data-ttu-id="2416d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2416d-143">System.Boolean</span></span>

## <span data-ttu-id="2416d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="2416d-144">NOTES</span></span>

## <span data-ttu-id="2416d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2416d-145">RELATED LINKS</span></span>
