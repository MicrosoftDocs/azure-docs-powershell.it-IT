---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033455"
---
# <span data-ttu-id="7075f-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="7075f-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="7075f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7075f-102">SYNOPSIS</span></span>
<span data-ttu-id="7075f-103">Richiamare un metodo diretto in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7075f-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="7075f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7075f-104">SYNTAX</span></span>

### <span data-ttu-id="7075f-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7075f-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7075f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7075f-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7075f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7075f-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7075f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7075f-108">DESCRIPTION</span></span>
<span data-ttu-id="7075f-109">Richiamare un metodo diretto in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7075f-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="7075f-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="7075f-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="7075f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7075f-111">EXAMPLES</span></span>

### <span data-ttu-id="7075f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7075f-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="7075f-113">Richiama un metodo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7075f-113">Invoke a device method.</span></span>

## <span data-ttu-id="7075f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7075f-114">PARAMETERS</span></span>

### <span data-ttu-id="7075f-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="7075f-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="7075f-116">Numero di secondi di attesa finché non viene eseguita correttamente una connessione.</span><span class="sxs-lookup"><span data-stu-id="7075f-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="7075f-117">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7075f-117">Default is 10.</span></span>

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

### <span data-ttu-id="7075f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7075f-118">-DefaultProfile</span></span>
<span data-ttu-id="7075f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7075f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7075f-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7075f-120">-DeviceId</span></span>
<span data-ttu-id="7075f-121">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7075f-121">Target Device Id.</span></span>

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

### <span data-ttu-id="7075f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7075f-122">-InputObject</span></span>
<span data-ttu-id="7075f-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="7075f-123">IotHub object</span></span>

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

### <span data-ttu-id="7075f-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7075f-124">-IotHubName</span></span>
<span data-ttu-id="7075f-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="7075f-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7075f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7075f-126">-Name</span></span>
<span data-ttu-id="7075f-127">Nome del metodo da richiamare su questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7075f-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7075f-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="7075f-128">-Payload</span></span>
<span data-ttu-id="7075f-129">Payload per il metodo da richiamare su questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7075f-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="7075f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7075f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7075f-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7075f-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7075f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7075f-132">-ResourceId</span></span>
<span data-ttu-id="7075f-133">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="7075f-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7075f-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="7075f-134">-ResponseTimeOut</span></span>
<span data-ttu-id="7075f-135">Numero di secondi di attesa finché non viene ricevuto un risultato dal metodo Direct.</span><span class="sxs-lookup"><span data-stu-id="7075f-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="7075f-136">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="7075f-136">Default is 10.</span></span>

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

### <span data-ttu-id="7075f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7075f-137">-Confirm</span></span>
<span data-ttu-id="7075f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7075f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7075f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7075f-139">-WhatIf</span></span>
<span data-ttu-id="7075f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7075f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7075f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7075f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7075f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7075f-142">CommonParameters</span></span>
<span data-ttu-id="7075f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7075f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7075f-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7075f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7075f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7075f-145">INPUTS</span></span>

### <span data-ttu-id="7075f-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7075f-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7075f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7075f-147">System.String</span></span>

## <span data-ttu-id="7075f-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7075f-148">OUTPUTS</span></span>

### <span data-ttu-id="7075f-149">Microsoft. Azure. Commands. Management. IotHub. Models. PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="7075f-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="7075f-150">Note</span><span class="sxs-lookup"><span data-stu-id="7075f-150">NOTES</span></span>

## <span data-ttu-id="7075f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7075f-151">RELATED LINKS</span></span>
