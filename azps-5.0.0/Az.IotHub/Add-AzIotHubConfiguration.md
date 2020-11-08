---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201254"
---
# <span data-ttu-id="a1619-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1619-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="a1619-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1619-102">SYNOPSIS</span></span>
<span data-ttu-id="a1619-103">Aggiungere una configurazione di gestione automatica dei dispositivi in un hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1619-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="a1619-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1619-104">SYNTAX</span></span>

### <span data-ttu-id="a1619-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1619-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1619-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1619-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1619-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1619-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1619-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1619-108">DESCRIPTION</span></span>
<span data-ttu-id="a1619-109">Il contenuto della configurazione è JSON e slightly varia in base al dispositivo o allo scopo di un modulo.</span><span class="sxs-lookup"><span data-stu-id="a1619-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="a1619-110">Le configurazioni dei dispositivi sono sotto forma di {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="a1619-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="a1619-111">Le configurazioni dei moduli sono sotto forma di {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="a1619-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="a1619-112">Le configurazioni possono essere definite con le metriche fornite dall'utente per la valutazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="a1619-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="a1619-113">Le metriche degli utenti sono JSON e sotto forma di {"Queries": {...}}</span><span class="sxs-lookup"><span data-stu-id="a1619-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="a1619-114">oppure {"Metrics": {"Queries": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="a1619-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="a1619-115">Nota: la condizione di destinazione per i moduli deve iniziare con "from Devices. Modules where".</span><span class="sxs-lookup"><span data-stu-id="a1619-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="a1619-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="a1619-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="a1619-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1619-117">EXAMPLES</span></span>

### <span data-ttu-id="a1619-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1619-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="a1619-119">Creare una configurazione di dispositivo con metadati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a1619-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="a1619-120">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a1619-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="a1619-121">Creare una configurazione di dispositivo con una priorità di 3 che si applica alla condizione quando un dispositivo è taggato nell'edificio 9 e l'ambiente è "test".</span><span class="sxs-lookup"><span data-stu-id="a1619-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="a1619-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a1619-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="a1619-123">Creare una configurazione di dispositivo con le metriche degli utenti.</span><span class="sxs-lookup"><span data-stu-id="a1619-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="a1619-124">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a1619-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="a1619-125">Creare una configurazione di dispositivo con etichette.</span><span class="sxs-lookup"><span data-stu-id="a1619-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="a1619-126">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a1619-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="a1619-127">Creare una configurazione del dispositivo con contenuto.</span><span class="sxs-lookup"><span data-stu-id="a1619-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="a1619-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1619-128">PARAMETERS</span></span>

### <span data-ttu-id="a1619-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1619-129">-DefaultProfile</span></span>
<span data-ttu-id="a1619-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1619-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1619-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="a1619-131">-DeviceContent</span></span>
<span data-ttu-id="a1619-132">Configurazione per i dispositivi IotHub.</span><span class="sxs-lookup"><span data-stu-id="a1619-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="a1619-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1619-133">-InputObject</span></span>
<span data-ttu-id="a1619-134">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="a1619-134">IotHub object</span></span>

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

### <span data-ttu-id="a1619-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a1619-135">-IotHubName</span></span>
<span data-ttu-id="a1619-136">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="a1619-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1619-137">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="a1619-137">-Label</span></span>
<span data-ttu-id="a1619-138">Mappa delle etichette da applicare alla configurazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1619-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="a1619-139">-Metrica</span><span class="sxs-lookup"><span data-stu-id="a1619-139">-Metric</span></span>
<span data-ttu-id="a1619-140">Raccolta query per la definizione delle metriche di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a1619-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="a1619-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1619-141">-Name</span></span>
<span data-ttu-id="a1619-142">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="a1619-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="a1619-143">-Priorità</span><span class="sxs-lookup"><span data-stu-id="a1619-143">-Priority</span></span>
<span data-ttu-id="a1619-144">Peso della configurazione del dispositivo in caso di regole concorrenti (vittorie più alte).</span><span class="sxs-lookup"><span data-stu-id="a1619-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="a1619-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1619-145">-ResourceGroupName</span></span>
<span data-ttu-id="a1619-146">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a1619-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1619-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1619-147">-ResourceId</span></span>
<span data-ttu-id="a1619-148">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="a1619-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a1619-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="a1619-149">-TargetCondition</span></span>
<span data-ttu-id="a1619-150">Condizione di destinazione in cui si applica una configurazione di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1619-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="a1619-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1619-151">-Confirm</span></span>
<span data-ttu-id="a1619-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1619-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1619-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1619-153">-WhatIf</span></span>
<span data-ttu-id="a1619-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1619-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1619-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1619-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1619-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1619-156">CommonParameters</span></span>
<span data-ttu-id="a1619-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1619-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1619-158">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1619-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1619-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1619-159">INPUTS</span></span>

### <span data-ttu-id="a1619-160">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a1619-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a1619-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a1619-161">System.String</span></span>

## <span data-ttu-id="a1619-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1619-162">OUTPUTS</span></span>

### <span data-ttu-id="a1619-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1619-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="a1619-164">Note</span><span class="sxs-lookup"><span data-stu-id="a1619-164">NOTES</span></span>

## <span data-ttu-id="a1619-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1619-165">RELATED LINKS</span></span>
