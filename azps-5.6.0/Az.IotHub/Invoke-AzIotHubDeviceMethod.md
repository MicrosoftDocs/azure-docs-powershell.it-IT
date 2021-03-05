---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 4c3782496041be7328ede29fad5ab3818791a0be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962942"
---
# <span data-ttu-id="d0f0e-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="d0f0e-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="d0f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f0e-103">Richiamare un metodo diretto in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="d0f0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0f0e-104">SYNTAX</span></span>

### <span data-ttu-id="d0f0e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0f0e-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f0e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0f0e-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f0e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0f0e-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f0e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="d0f0e-109">Richiamare un metodo diretto in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="d0f0e-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="d0f0e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0f0e-111">EXAMPLES</span></span>

### <span data-ttu-id="d0f0e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0f0e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="d0f0e-113">Richiamare un metodo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-113">Invoke a device method.</span></span>

## <span data-ttu-id="d0f0e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f0e-114">PARAMETERS</span></span>

### <span data-ttu-id="d0f0e-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="d0f0e-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="d0f0e-116">Numero di secondi di attesa prima che la connessione sia stata stabilita correttamente.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="d0f0e-117">L'impostazione predefinita è 10.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-117">Default is 10.</span></span>

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

### <span data-ttu-id="d0f0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f0e-118">-DefaultProfile</span></span>
<span data-ttu-id="d0f0e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f0e-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d0f0e-120">-DeviceId</span></span>
<span data-ttu-id="d0f0e-121">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-121">Target Device Id.</span></span>

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

### <span data-ttu-id="d0f0e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0f0e-122">-InputObject</span></span>
<span data-ttu-id="d0f0e-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d0f0e-123">IotHub object</span></span>

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

### <span data-ttu-id="d0f0e-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d0f0e-124">-IotHubName</span></span>
<span data-ttu-id="d0f0e-125">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="d0f0e-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d0f0e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d0f0e-126">-Name</span></span>
<span data-ttu-id="d0f0e-127">Nome del metodo da richiamare nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="d0f0e-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="d0f0e-128">-Payload</span></span>
<span data-ttu-id="d0f0e-129">Payload per il metodo da richiamare in questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="d0f0e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f0e-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0f0e-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d0f0e-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0f0e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0f0e-132">-ResourceId</span></span>
<span data-ttu-id="d0f0e-133">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d0f0e-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d0f0e-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="d0f0e-134">-ResponseTimeOut</span></span>
<span data-ttu-id="d0f0e-135">Numero di secondi di attesa finché non si riceve un risultato dal metodo diretto.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="d0f0e-136">L'impostazione predefinita è 10.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-136">Default is 10.</span></span>

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

### <span data-ttu-id="d0f0e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0f0e-137">-Confirm</span></span>
<span data-ttu-id="d0f0e-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f0e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f0e-139">-WhatIf</span></span>
<span data-ttu-id="d0f0e-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f0e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f0e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f0e-142">CommonParameters</span></span>
<span data-ttu-id="d0f0e-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f0e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f0e-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f0e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f0e-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0f0e-145">INPUTS</span></span>

### <span data-ttu-id="d0f0e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d0f0e-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d0f0e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="d0f0e-147">System.String</span></span>

## <span data-ttu-id="d0f0e-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0f0e-148">OUTPUTS</span></span>

### <span data-ttu-id="d0f0e-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="d0f0e-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="d0f0e-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0f0e-150">NOTES</span></span>

## <span data-ttu-id="d0f0e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0f0e-151">RELATED LINKS</span></span>
