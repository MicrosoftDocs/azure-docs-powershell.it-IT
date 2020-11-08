---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192873"
---
# <span data-ttu-id="f2047-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="f2047-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="f2047-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2047-102">SYNOPSIS</span></span>
<span data-ttu-id="f2047-103">Richiamare un metodo del modulo Edge.</span><span class="sxs-lookup"><span data-stu-id="f2047-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="f2047-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2047-104">SYNTAX</span></span>

### <span data-ttu-id="f2047-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2047-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2047-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2047-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2047-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f2047-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2047-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2047-108">DESCRIPTION</span></span>
<span data-ttu-id="f2047-109">Richiamare un metodo del modulo Edge.</span><span class="sxs-lookup"><span data-stu-id="f2047-109">Invoke an Edge module method.</span></span> <span data-ttu-id="f2047-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="f2047-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="f2047-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2047-111">EXAMPLES</span></span>

### <span data-ttu-id="f2047-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2047-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="f2047-113">Richiamare un metodo del modulo Edge.</span><span class="sxs-lookup"><span data-stu-id="f2047-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="f2047-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2047-114">PARAMETERS</span></span>

### <span data-ttu-id="f2047-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="f2047-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="f2047-116">Numero di secondi di attesa finché non viene eseguita correttamente una connessione.</span><span class="sxs-lookup"><span data-stu-id="f2047-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="f2047-117">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="f2047-117">Default is 10.</span></span>

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

### <span data-ttu-id="f2047-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2047-118">-DefaultProfile</span></span>
<span data-ttu-id="f2047-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2047-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2047-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f2047-120">-DeviceId</span></span>
<span data-ttu-id="f2047-121">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f2047-121">Target Device Id.</span></span>

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

### <span data-ttu-id="f2047-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2047-122">-InputObject</span></span>
<span data-ttu-id="f2047-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="f2047-123">IotHub object</span></span>

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

### <span data-ttu-id="f2047-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f2047-124">-IotHubName</span></span>
<span data-ttu-id="f2047-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="f2047-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f2047-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f2047-126">-ModuleId</span></span>
<span data-ttu-id="f2047-127">ID modulo del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f2047-127">Target device's module id.</span></span>

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

### <span data-ttu-id="f2047-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2047-128">-Name</span></span>
<span data-ttu-id="f2047-129">Il nome del metodo da richiamare nel modulo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2047-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="f2047-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="f2047-130">-Payload</span></span>
<span data-ttu-id="f2047-131">Payload per il metodo da richiamare in questo modulo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f2047-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="f2047-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2047-132">-ResourceGroupName</span></span>
<span data-ttu-id="f2047-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f2047-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f2047-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2047-134">-ResourceId</span></span>
<span data-ttu-id="f2047-135">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="f2047-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f2047-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="f2047-136">-ResponseTimeOut</span></span>
<span data-ttu-id="f2047-137">Numero di secondi di attesa finché non viene ricevuto un risultato dal metodo Direct.</span><span class="sxs-lookup"><span data-stu-id="f2047-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="f2047-138">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="f2047-138">Default is 10.</span></span>

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

### <span data-ttu-id="f2047-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2047-139">-Confirm</span></span>
<span data-ttu-id="f2047-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2047-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2047-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2047-141">-WhatIf</span></span>
<span data-ttu-id="f2047-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2047-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2047-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2047-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2047-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2047-144">CommonParameters</span></span>
<span data-ttu-id="f2047-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2047-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2047-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2047-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2047-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2047-147">INPUTS</span></span>

### <span data-ttu-id="f2047-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f2047-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f2047-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f2047-149">System.String</span></span>

## <span data-ttu-id="f2047-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2047-150">OUTPUTS</span></span>

### <span data-ttu-id="f2047-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="f2047-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="f2047-152">Note</span><span class="sxs-lookup"><span data-stu-id="f2047-152">NOTES</span></span>

## <span data-ttu-id="f2047-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2047-153">RELATED LINKS</span></span>
