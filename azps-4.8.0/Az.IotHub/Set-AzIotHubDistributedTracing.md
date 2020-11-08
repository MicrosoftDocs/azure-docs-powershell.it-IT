---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033073"
---
# <span data-ttu-id="a92f9-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="a92f9-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="a92f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a92f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a92f9-103">Aggiornare le opzioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a92f9-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a92f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a92f9-104">SYNTAX</span></span>

### <span data-ttu-id="a92f9-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a92f9-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a92f9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a92f9-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a92f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a92f9-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92f9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a92f9-108">DESCRIPTION</span></span>
<span data-ttu-id="a92f9-109">Aggiornare le opzioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a92f9-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a92f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a92f9-110">EXAMPLES</span></span>

### <span data-ttu-id="a92f9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a92f9-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="a92f9-112">Aggiornare le opzioni di analisi distribuite per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a92f9-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="a92f9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a92f9-113">PARAMETERS</span></span>

### <span data-ttu-id="a92f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92f9-114">-DefaultProfile</span></span>
<span data-ttu-id="a92f9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a92f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a92f9-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a92f9-116">-DeviceId</span></span>
<span data-ttu-id="a92f9-117">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a92f9-117">Target Device Id.</span></span>

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

### <span data-ttu-id="a92f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a92f9-118">-InputObject</span></span>
<span data-ttu-id="a92f9-119">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="a92f9-119">IotHub object</span></span>

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

### <span data-ttu-id="a92f9-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a92f9-120">-IotHubName</span></span>
<span data-ttu-id="a92f9-121">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="a92f9-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a92f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="a92f9-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a92f9-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a92f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a92f9-124">-ResourceId</span></span>
<span data-ttu-id="a92f9-125">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="a92f9-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a92f9-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="a92f9-126">-SamplingMode</span></span>
<span data-ttu-id="a92f9-127">Attiva il campionamento per abilitare e disabilitare la traccia distribuita.</span><span class="sxs-lookup"><span data-stu-id="a92f9-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="a92f9-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="a92f9-128">-SamplingRate</span></span>
<span data-ttu-id="a92f9-129">Controlla la quantità di messaggi campionati per l'aggiunta di un contesto di traccia.</span><span class="sxs-lookup"><span data-stu-id="a92f9-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="a92f9-130">Questo valore è una percentuale.</span><span class="sxs-lookup"><span data-stu-id="a92f9-130">This value is a percentage.</span></span>
<span data-ttu-id="a92f9-131">Sono consentiti solo i valori compresi tra 0 e 100 (inclusi).</span><span class="sxs-lookup"><span data-stu-id="a92f9-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="a92f9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a92f9-132">-Confirm</span></span>
<span data-ttu-id="a92f9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a92f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92f9-134">-WhatIf</span></span>
<span data-ttu-id="a92f9-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a92f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a92f9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a92f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92f9-137">CommonParameters</span></span>
<span data-ttu-id="a92f9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92f9-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92f9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92f9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a92f9-140">INPUTS</span></span>

### <span data-ttu-id="a92f9-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a92f9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a92f9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a92f9-142">System.String</span></span>

## <span data-ttu-id="a92f9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a92f9-143">OUTPUTS</span></span>

### <span data-ttu-id="a92f9-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="a92f9-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="a92f9-145">Note</span><span class="sxs-lookup"><span data-stu-id="a92f9-145">NOTES</span></span>

## <span data-ttu-id="a92f9-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a92f9-146">RELATED LINKS</span></span>
