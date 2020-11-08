---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189860"
---
# <span data-ttu-id="d392d-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="d392d-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="d392d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d392d-102">SYNOPSIS</span></span>
<span data-ttu-id="d392d-103">Inviare un messaggio da dispositivo a cloud.</span><span class="sxs-lookup"><span data-stu-id="d392d-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="d392d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d392d-104">SYNTAX</span></span>

### <span data-ttu-id="d392d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d392d-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d392d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d392d-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d392d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d392d-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d392d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d392d-108">DESCRIPTION</span></span>
<span data-ttu-id="d392d-109">Il comando supporta l'invio di messaggi con le proprietà dell'applicazione e del sistema.</span><span class="sxs-lookup"><span data-stu-id="d392d-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="d392d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d392d-110">EXAMPLES</span></span>

### <span data-ttu-id="d392d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d392d-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="d392d-112">Invio del messaggio del dispositivo al cloud tramite il tipo di trasporto predefinito.</span><span class="sxs-lookup"><span data-stu-id="d392d-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="d392d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d392d-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="d392d-114">Invio di un dispositivo MQTT al messaggio cloud.</span><span class="sxs-lookup"><span data-stu-id="d392d-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="d392d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d392d-115">PARAMETERS</span></span>

### <span data-ttu-id="d392d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d392d-116">-DefaultProfile</span></span>
<span data-ttu-id="d392d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d392d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d392d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d392d-118">-DeviceId</span></span>
<span data-ttu-id="d392d-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d392d-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d392d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d392d-120">-InputObject</span></span>
<span data-ttu-id="d392d-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d392d-121">IotHub object</span></span>

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

### <span data-ttu-id="d392d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d392d-122">-IotHubName</span></span>
<span data-ttu-id="d392d-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="d392d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d392d-124">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="d392d-124">-Message</span></span>
<span data-ttu-id="d392d-125">Corpo del messaggio da inviare all'hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="d392d-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="d392d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d392d-126">-PassThru</span></span>
<span data-ttu-id="d392d-127">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="d392d-127">Allows to return the boolean object.</span></span> <span data-ttu-id="d392d-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d392d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d392d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d392d-129">-ResourceGroupName</span></span>
<span data-ttu-id="d392d-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d392d-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d392d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d392d-131">-ResourceId</span></span>
<span data-ttu-id="d392d-132">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d392d-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d392d-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="d392d-133">-TransportType</span></span>
<span data-ttu-id="d392d-134">Tipo di trasporto da usare.</span><span class="sxs-lookup"><span data-stu-id="d392d-134">Transport type to use.</span></span>
<span data-ttu-id="d392d-135">Il valore predefinito è AMQP.</span><span class="sxs-lookup"><span data-stu-id="d392d-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d392d-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d392d-136">-Confirm</span></span>
<span data-ttu-id="d392d-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d392d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d392d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d392d-138">-WhatIf</span></span>
<span data-ttu-id="d392d-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d392d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d392d-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d392d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d392d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d392d-141">CommonParameters</span></span>
<span data-ttu-id="d392d-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d392d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d392d-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d392d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d392d-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d392d-144">INPUTS</span></span>

### <span data-ttu-id="d392d-145">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d392d-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d392d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d392d-146">System.String</span></span>

## <span data-ttu-id="d392d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d392d-147">OUTPUTS</span></span>

### <span data-ttu-id="d392d-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d392d-148">System.Boolean</span></span>

## <span data-ttu-id="d392d-149">Note</span><span class="sxs-lookup"><span data-stu-id="d392d-149">NOTES</span></span>

## <span data-ttu-id="d392d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d392d-150">RELATED LINKS</span></span>
