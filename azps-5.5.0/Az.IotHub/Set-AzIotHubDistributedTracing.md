---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180510"
---
# <span data-ttu-id="8f927-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="8f927-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="8f927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f927-102">SYNOPSIS</span></span>
<span data-ttu-id="8f927-103">Aggiornare le opzioni di traccia distribuita per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f927-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8f927-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f927-104">SYNTAX</span></span>

### <span data-ttu-id="8f927-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f927-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f927-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f927-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f927-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8f927-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f927-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8f927-108">DESCRIPTION</span></span>
<span data-ttu-id="8f927-109">Aggiornare le opzioni di traccia distribuita per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f927-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8f927-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f927-110">EXAMPLES</span></span>

### <span data-ttu-id="8f927-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f927-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="8f927-112">Aggiornare le opzioni di traccia distribuita per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f927-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="8f927-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f927-113">PARAMETERS</span></span>

### <span data-ttu-id="8f927-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f927-114">-DefaultProfile</span></span>
<span data-ttu-id="8f927-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f927-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f927-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8f927-116">-DeviceId</span></span>
<span data-ttu-id="8f927-117">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8f927-117">Target Device Id.</span></span>

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

### <span data-ttu-id="8f927-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f927-118">-InputObject</span></span>
<span data-ttu-id="8f927-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8f927-119">IotHub object</span></span>

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

### <span data-ttu-id="8f927-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8f927-120">-IotHubName</span></span>
<span data-ttu-id="8f927-121">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="8f927-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8f927-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f927-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f927-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8f927-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8f927-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f927-124">-ResourceId</span></span>
<span data-ttu-id="8f927-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8f927-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8f927-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="8f927-126">-SamplingMode</span></span>
<span data-ttu-id="8f927-127">Attiva e disattiva il campionamento per le traccia distribuite.</span><span class="sxs-lookup"><span data-stu-id="8f927-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f927-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="8f927-128">-SamplingRate</span></span>
<span data-ttu-id="8f927-129">Controlla la quantità di messaggi di esempio per l'aggiunta di contesto di traccia.</span><span class="sxs-lookup"><span data-stu-id="8f927-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="8f927-130">Questo valore è una percentuale.</span><span class="sxs-lookup"><span data-stu-id="8f927-130">This value is a percentage.</span></span>
<span data-ttu-id="8f927-131">Sono consentiti solo valori compresi tra 0 e 100 (inclusi).</span><span class="sxs-lookup"><span data-stu-id="8f927-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f927-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f927-132">-Confirm</span></span>
<span data-ttu-id="8f927-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f927-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f927-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f927-134">-WhatIf</span></span>
<span data-ttu-id="8f927-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f927-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f927-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f927-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f927-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f927-137">CommonParameters</span></span>
<span data-ttu-id="8f927-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f927-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f927-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f927-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f927-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="8f927-140">INPUTS</span></span>

### <span data-ttu-id="8f927-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8f927-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8f927-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8f927-142">System.String</span></span>

## <span data-ttu-id="8f927-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f927-143">OUTPUTS</span></span>

### <span data-ttu-id="8f927-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceT più elettronica</span><span class="sxs-lookup"><span data-stu-id="8f927-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="8f927-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="8f927-145">NOTES</span></span>

## <span data-ttu-id="8f927-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f927-146">RELATED LINKS</span></span>
