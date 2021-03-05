---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 84f1485f84996c1c0e98768914afffd501722ab7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978478"
---
# <span data-ttu-id="8e2b8-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="8e2b8-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="8e2b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2b8-103">Aggiorna i tag e le proprietà desiderate di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="8e2b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e2b8-104">SYNTAX</span></span>

### <span data-ttu-id="8e2b8-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e2b8-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e2b8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e2b8-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e2b8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8e2b8-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e2b8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e2b8-108">DESCRIPTION</span></span>
<span data-ttu-id="8e2b8-109">Aggiorna o sostituisce un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="8e2b8-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="8e2b8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e2b8-111">EXAMPLES</span></span>

### <span data-ttu-id="8e2b8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e2b8-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="8e2b8-113">Restituisce l'oggetto dispositivo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="8e2b8-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8e2b8-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="8e2b8-115">Restituisce l'oggetto dispositivo con le proprietà desiderate aggiornate.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="8e2b8-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8e2b8-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="8e2b8-117">Restituisce l'oggetto dispositivo con la proprietà tag aggiornata.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="8e2b8-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8e2b8-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="8e2b8-119">Restituisce l'oggetto dispositivo sostituito.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="8e2b8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2b8-120">PARAMETERS</span></span>

### <span data-ttu-id="8e2b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2b8-121">-DefaultProfile</span></span>
<span data-ttu-id="8e2b8-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2b8-123">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="8e2b8-123">-Desired</span></span>
<span data-ttu-id="8e2b8-124">Aggiungere o aggiornare la proprietà desiderata in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-124">Add or update the desired property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2b8-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8e2b8-125">-DeviceId</span></span>
<span data-ttu-id="8e2b8-126">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-126">Target Device Id.</span></span>

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

### <span data-ttu-id="8e2b8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e2b8-127">-InputObject</span></span>
<span data-ttu-id="8e2b8-128">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8e2b8-128">IotHub object</span></span>

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

### <span data-ttu-id="8e2b8-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8e2b8-129">-IotHubName</span></span>
<span data-ttu-id="8e2b8-130">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="8e2b8-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8e2b8-131">-Parziale</span><span class="sxs-lookup"><span data-stu-id="8e2b8-131">-Partial</span></span>
<span data-ttu-id="8e2b8-132">Consente di aggiornare solo parzialmente i tag e le proprietà desiderate di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="8e2b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="8e2b8-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8e2b8-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8e2b8-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e2b8-135">-ResourceId</span></span>
<span data-ttu-id="8e2b8-136">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8e2b8-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8e2b8-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e2b8-137">-Tag</span></span>
<span data-ttu-id="8e2b8-138">Aggiungere o aggiornare la proprietà tag in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-138">Add or update the tags property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2b8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e2b8-139">-Confirm</span></span>
<span data-ttu-id="8e2b8-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2b8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2b8-141">-WhatIf</span></span>
<span data-ttu-id="8e2b8-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e2b8-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2b8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2b8-144">CommonParameters</span></span>
<span data-ttu-id="8e2b8-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2b8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2b8-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2b8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2b8-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e2b8-147">INPUTS</span></span>

### <span data-ttu-id="8e2b8-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8e2b8-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8e2b8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2b8-149">System.String</span></span>

## <span data-ttu-id="8e2b8-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e2b8-150">OUTPUTS</span></span>

### <span data-ttu-id="8e2b8-151">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2b8-151">System.String</span></span>

## <span data-ttu-id="8e2b8-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e2b8-152">NOTES</span></span>

## <span data-ttu-id="8e2b8-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e2b8-153">RELATED LINKS</span></span>
