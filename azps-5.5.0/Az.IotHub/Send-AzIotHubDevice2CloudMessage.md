---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192414"
---
# <span data-ttu-id="eee05-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="eee05-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="eee05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eee05-102">SYNOPSIS</span></span>
<span data-ttu-id="eee05-103">Inviare un messaggio da dispositivo a cloud.</span><span class="sxs-lookup"><span data-stu-id="eee05-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="eee05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eee05-104">SYNTAX</span></span>

### <span data-ttu-id="eee05-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eee05-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eee05-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="eee05-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eee05-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="eee05-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eee05-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eee05-108">DESCRIPTION</span></span>
<span data-ttu-id="eee05-109">Il comando supporta l'invio di messaggi con le proprietà di applicazioni e di sistema.</span><span class="sxs-lookup"><span data-stu-id="eee05-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="eee05-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eee05-110">EXAMPLES</span></span>

### <span data-ttu-id="eee05-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eee05-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="eee05-112">Invio di un dispositivo a un messaggio nel cloud con il tipo di trasporto predefinito.</span><span class="sxs-lookup"><span data-stu-id="eee05-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="eee05-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="eee05-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="eee05-114">Invio di un dispositivo mqtt a un messaggio nel cloud.</span><span class="sxs-lookup"><span data-stu-id="eee05-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="eee05-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eee05-115">PARAMETERS</span></span>

### <span data-ttu-id="eee05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee05-116">-DefaultProfile</span></span>
<span data-ttu-id="eee05-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eee05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eee05-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="eee05-118">-DeviceId</span></span>
<span data-ttu-id="eee05-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eee05-119">Target Device Id.</span></span>

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

### <span data-ttu-id="eee05-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eee05-120">-InputObject</span></span>
<span data-ttu-id="eee05-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="eee05-121">IotHub object</span></span>

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

### <span data-ttu-id="eee05-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="eee05-122">-IotHubName</span></span>
<span data-ttu-id="eee05-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="eee05-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="eee05-124">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="eee05-124">-Message</span></span>
<span data-ttu-id="eee05-125">Corpo del messaggio da inviare all'hub IoT.</span><span class="sxs-lookup"><span data-stu-id="eee05-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="eee05-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eee05-126">-PassThru</span></span>
<span data-ttu-id="eee05-127">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="eee05-127">Allows to return the boolean object.</span></span> <span data-ttu-id="eee05-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="eee05-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eee05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee05-129">-ResourceGroupName</span></span>
<span data-ttu-id="eee05-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="eee05-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="eee05-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eee05-131">-ResourceId</span></span>
<span data-ttu-id="eee05-132">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="eee05-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="eee05-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="eee05-133">-TransportType</span></span>
<span data-ttu-id="eee05-134">Tipo di trasporto da usare.</span><span class="sxs-lookup"><span data-stu-id="eee05-134">Transport type to use.</span></span>
<span data-ttu-id="eee05-135">L'impostazione predefinita è Amqp.</span><span class="sxs-lookup"><span data-stu-id="eee05-135">Default is Amqp.</span></span>

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

### <span data-ttu-id="eee05-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee05-136">-Confirm</span></span>
<span data-ttu-id="eee05-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eee05-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee05-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee05-138">-WhatIf</span></span>
<span data-ttu-id="eee05-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee05-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee05-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eee05-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee05-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee05-141">CommonParameters</span></span>
<span data-ttu-id="eee05-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee05-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee05-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee05-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee05-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="eee05-144">INPUTS</span></span>

### <span data-ttu-id="eee05-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="eee05-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="eee05-146">System.String</span><span class="sxs-lookup"><span data-stu-id="eee05-146">System.String</span></span>

## <span data-ttu-id="eee05-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eee05-147">OUTPUTS</span></span>

### <span data-ttu-id="eee05-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eee05-148">System.Boolean</span></span>

## <span data-ttu-id="eee05-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="eee05-149">NOTES</span></span>

## <span data-ttu-id="eee05-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eee05-150">RELATED LINKS</span></span>
