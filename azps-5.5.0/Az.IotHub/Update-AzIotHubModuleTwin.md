---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200047"
---
# <span data-ttu-id="b6f80-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="b6f80-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="b6f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f80-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f80-103">Aggiorna i tag e le proprietà desiderate di un modulo di dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="b6f80-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="b6f80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6f80-104">SYNTAX</span></span>

### <span data-ttu-id="b6f80-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6f80-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f80-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6f80-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6f80-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6f80-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f80-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6f80-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f80-109">Aggiorna o sostituisce un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6f80-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="b6f80-110">Per https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="b6f80-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="b6f80-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6f80-111">EXAMPLES</span></span>

### <span data-ttu-id="b6f80-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6f80-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="b6f80-113">Restituisce l'oggetto modulo dispositivo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b6f80-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="b6f80-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6f80-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="b6f80-115">Restituisce l'oggetto modulo dispositivo con le proprietà desiderate aggiornate.</span><span class="sxs-lookup"><span data-stu-id="b6f80-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="b6f80-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b6f80-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="b6f80-117">Restituisce l'oggetto modulo dispositivo con la proprietà tag aggiornata.</span><span class="sxs-lookup"><span data-stu-id="b6f80-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="b6f80-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b6f80-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="b6f80-119">Restituisce l'oggetto modulo dispositivo sostituito.</span><span class="sxs-lookup"><span data-stu-id="b6f80-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="b6f80-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6f80-120">PARAMETERS</span></span>

### <span data-ttu-id="b6f80-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f80-121">-DefaultProfile</span></span>
<span data-ttu-id="b6f80-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f80-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f80-123">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="b6f80-123">-Desired</span></span>
<span data-ttu-id="b6f80-124">Aggiungere o aggiornare la proprietà desiderata in un modulo.</span><span class="sxs-lookup"><span data-stu-id="b6f80-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="b6f80-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b6f80-125">-DeviceId</span></span>
<span data-ttu-id="b6f80-126">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6f80-126">Target Device Id.</span></span>

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

### <span data-ttu-id="b6f80-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f80-127">-InputObject</span></span>
<span data-ttu-id="b6f80-128">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f80-128">IotHub object</span></span>

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

### <span data-ttu-id="b6f80-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b6f80-129">-IotHubName</span></span>
<span data-ttu-id="b6f80-130">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="b6f80-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b6f80-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="b6f80-131">-ModuleId</span></span>
<span data-ttu-id="b6f80-132">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b6f80-132">Target Module Id.</span></span>

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

### <span data-ttu-id="b6f80-133">-Parziale</span><span class="sxs-lookup"><span data-stu-id="b6f80-133">-Partial</span></span>
<span data-ttu-id="b6f80-134">Consente di aggiornare solo parzialmente i tag e le proprietà desiderate di un modulo.</span><span class="sxs-lookup"><span data-stu-id="b6f80-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="b6f80-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f80-135">-ResourceGroupName</span></span>
<span data-ttu-id="b6f80-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b6f80-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b6f80-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f80-137">-ResourceId</span></span>
<span data-ttu-id="b6f80-138">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b6f80-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b6f80-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6f80-139">-Tag</span></span>
<span data-ttu-id="b6f80-140">Aggiungere o aggiornare la proprietà tag in un modulo.</span><span class="sxs-lookup"><span data-stu-id="b6f80-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="b6f80-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f80-141">-Confirm</span></span>
<span data-ttu-id="b6f80-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f80-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f80-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f80-143">-WhatIf</span></span>
<span data-ttu-id="b6f80-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6f80-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f80-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6f80-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f80-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f80-146">CommonParameters</span></span>
<span data-ttu-id="b6f80-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f80-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f80-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f80-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f80-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6f80-149">INPUTS</span></span>

### <span data-ttu-id="b6f80-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b6f80-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b6f80-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b6f80-151">System.String</span></span>

## <span data-ttu-id="b6f80-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6f80-152">OUTPUTS</span></span>

### <span data-ttu-id="b6f80-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="b6f80-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="b6f80-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6f80-154">NOTES</span></span>

## <span data-ttu-id="b6f80-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6f80-155">RELATED LINKS</span></span>
