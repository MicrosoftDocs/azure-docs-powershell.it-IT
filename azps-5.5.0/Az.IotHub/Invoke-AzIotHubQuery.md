---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187638"
---
# <span data-ttu-id="ef457-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="ef457-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="ef457-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef457-102">SYNOPSIS</span></span>
<span data-ttu-id="ef457-103">Eseguire query in un Hub IoT usando un SQL molto potente.</span><span class="sxs-lookup"><span data-stu-id="ef457-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="ef457-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef457-104">SYNTAX</span></span>

### <span data-ttu-id="ef457-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef457-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef457-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef457-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef457-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef457-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef457-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef457-108">DESCRIPTION</span></span>
<span data-ttu-id="ef457-109">È possibile eseguire query in un Hub IoT usando un potente linguaggio simile SQL per recuperare informazioni su dispositivi e moduli, processi e routing dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="ef457-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="ef457-110">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="ef457-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="ef457-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef457-111">EXAMPLES</span></span>

### <span data-ttu-id="ef457-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef457-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="ef457-113">Eseguire query su tutti i dati di dispositivo in un Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="ef457-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="ef457-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ef457-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="ef457-115">Eseguire query sui 2 principali dati del modulo in un dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef457-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="ef457-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef457-116">PARAMETERS</span></span>

### <span data-ttu-id="ef457-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef457-117">-DefaultProfile</span></span>
<span data-ttu-id="ef457-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef457-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef457-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef457-119">-InputObject</span></span>
<span data-ttu-id="ef457-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="ef457-120">IotHub object</span></span>

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

### <span data-ttu-id="ef457-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ef457-121">-IotHubName</span></span>
<span data-ttu-id="ef457-122">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="ef457-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ef457-123">-Query</span><span class="sxs-lookup"><span data-stu-id="ef457-123">-Query</span></span>
<span data-ttu-id="ef457-124">Query utente da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ef457-124">User query to be executed.</span></span>

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

### <span data-ttu-id="ef457-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef457-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef457-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ef457-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ef457-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef457-127">-ResourceId</span></span>
<span data-ttu-id="ef457-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="ef457-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ef457-129">-In alto</span><span class="sxs-lookup"><span data-stu-id="ef457-129">-Top</span></span>
<span data-ttu-id="ef457-130">Numero massimo di elementi da restituire.</span><span class="sxs-lookup"><span data-stu-id="ef457-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="ef457-131">Per impostazione predefinita, la query non ha alcun limite.</span><span class="sxs-lookup"><span data-stu-id="ef457-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="ef457-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef457-132">-Confirm</span></span>
<span data-ttu-id="ef457-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef457-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef457-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef457-134">-WhatIf</span></span>
<span data-ttu-id="ef457-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef457-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef457-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef457-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef457-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef457-137">CommonParameters</span></span>
<span data-ttu-id="ef457-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef457-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef457-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef457-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef457-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef457-140">INPUTS</span></span>

### <span data-ttu-id="ef457-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ef457-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ef457-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ef457-142">System.String</span></span>

## <span data-ttu-id="ef457-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef457-143">OUTPUTS</span></span>

### <span data-ttu-id="ef457-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef457-144">System.String</span></span>

## <span data-ttu-id="ef457-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef457-145">NOTES</span></span>

## <span data-ttu-id="ef457-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef457-146">RELATED LINKS</span></span>
