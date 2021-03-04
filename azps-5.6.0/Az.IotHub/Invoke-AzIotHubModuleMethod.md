---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: ea2362fc779ada8faf62c863ccffb9e58e078b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987865"
---
# <span data-ttu-id="70067-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="70067-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="70067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70067-102">SYNOPSIS</span></span>
<span data-ttu-id="70067-103">Richiamare un metodo del modulo di Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70067-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="70067-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70067-104">SYNTAX</span></span>

### <span data-ttu-id="70067-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="70067-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70067-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70067-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70067-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="70067-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70067-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70067-108">DESCRIPTION</span></span>
<span data-ttu-id="70067-109">Richiamare un metodo del modulo di Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70067-109">Invoke an Edge module method.</span></span> <span data-ttu-id="70067-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="70067-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="70067-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70067-111">EXAMPLES</span></span>

### <span data-ttu-id="70067-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="70067-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="70067-113">Richiamare un metodo del modulo di Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70067-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="70067-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70067-114">PARAMETERS</span></span>

### <span data-ttu-id="70067-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="70067-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="70067-116">Numero di secondi di attesa prima che la connessione sia stata stabilita correttamente.</span><span class="sxs-lookup"><span data-stu-id="70067-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="70067-117">L'impostazione predefinita è 10.</span><span class="sxs-lookup"><span data-stu-id="70067-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70067-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70067-118">-DefaultProfile</span></span>
<span data-ttu-id="70067-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70067-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70067-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="70067-120">-DeviceId</span></span>
<span data-ttu-id="70067-121">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70067-121">Target Device Id.</span></span>

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

### <span data-ttu-id="70067-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70067-122">-InputObject</span></span>
<span data-ttu-id="70067-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="70067-123">IotHub object</span></span>

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

### <span data-ttu-id="70067-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="70067-124">-IotHubName</span></span>
<span data-ttu-id="70067-125">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="70067-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="70067-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="70067-126">-ModuleId</span></span>
<span data-ttu-id="70067-127">ID modulo del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="70067-127">Target device's module id.</span></span>

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

### <span data-ttu-id="70067-128">-Name</span><span class="sxs-lookup"><span data-stu-id="70067-128">-Name</span></span>
<span data-ttu-id="70067-129">Nome del metodo da richiamare in questo modulo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70067-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="70067-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="70067-130">-Payload</span></span>
<span data-ttu-id="70067-131">Payload per il metodo da richiamare in questo modulo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70067-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="70067-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70067-132">-ResourceGroupName</span></span>
<span data-ttu-id="70067-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="70067-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70067-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70067-134">-ResourceId</span></span>
<span data-ttu-id="70067-135">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="70067-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="70067-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="70067-136">-ResponseTimeOut</span></span>
<span data-ttu-id="70067-137">Numero di secondi di attesa finché non si riceve un risultato dal metodo diretto.</span><span class="sxs-lookup"><span data-stu-id="70067-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="70067-138">L'impostazione predefinita è 10.</span><span class="sxs-lookup"><span data-stu-id="70067-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70067-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70067-139">-Confirm</span></span>
<span data-ttu-id="70067-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70067-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70067-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70067-141">-WhatIf</span></span>
<span data-ttu-id="70067-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70067-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70067-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70067-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70067-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70067-144">CommonParameters</span></span>
<span data-ttu-id="70067-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70067-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70067-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70067-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70067-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="70067-147">INPUTS</span></span>

### <span data-ttu-id="70067-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="70067-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="70067-149">System.String</span><span class="sxs-lookup"><span data-stu-id="70067-149">System.String</span></span>

## <span data-ttu-id="70067-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70067-150">OUTPUTS</span></span>

### <span data-ttu-id="70067-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="70067-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="70067-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="70067-152">NOTES</span></span>

## <span data-ttu-id="70067-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70067-153">RELATED LINKS</span></span>
