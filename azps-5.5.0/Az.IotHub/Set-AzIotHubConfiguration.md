---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190343"
---
# <span data-ttu-id="cf0a6-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf0a6-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="cf0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0a6-103">Aggiornare i campi modificabili della registrazione della configurazione.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="cf0a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf0a6-104">SYNTAX</span></span>

### <span data-ttu-id="cf0a6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf0a6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf0a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf0a6-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf0a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cf0a6-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf0a6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf0a6-108">DESCRIPTION</span></span>
<span data-ttu-id="cf0a6-109">Aggiornare le proprietà specificate di una configurazione automatica di gestione dei dispositivi IoT.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="cf0a6-110">Nota: il contenuto della configurazione non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="cf0a6-111">Le proprietà di configurazione che possono essere aggiornate sono "etichette", "metriche", "priorità" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="cf0a6-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="cf0a6-112">Per https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="cf0a6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf0a6-113">EXAMPLES</span></span>

### <span data-ttu-id="cf0a6-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cf0a6-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="cf0a6-115">Modificare la priorità di una configurazione del dispositivo e aggiornare la condizione di destinazione</span><span class="sxs-lookup"><span data-stu-id="cf0a6-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="cf0a6-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cf0a6-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="cf0a6-117">Aggiornare le metriche e le etichette di una configurazione di dispositivo</span><span class="sxs-lookup"><span data-stu-id="cf0a6-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="cf0a6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf0a6-118">PARAMETERS</span></span>

### <span data-ttu-id="cf0a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0a6-119">-DefaultProfile</span></span>
<span data-ttu-id="cf0a6-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf0a6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cf0a6-121">-Force</span></span>
<span data-ttu-id="cf0a6-122">Consente di sostituire l'oggetto di configurazione anche se è stato aggiornato dopo il recupero dell'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="cf0a6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf0a6-123">-InputObject</span></span>
<span data-ttu-id="cf0a6-124">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="cf0a6-124">IotHub object</span></span>

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

### <span data-ttu-id="cf0a6-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cf0a6-125">-IotHubName</span></span>
<span data-ttu-id="cf0a6-126">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="cf0a6-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cf0a6-127">-Label</span><span class="sxs-lookup"><span data-stu-id="cf0a6-127">-Label</span></span>
<span data-ttu-id="cf0a6-128">Mappa delle etichette da applicare alla configurazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="cf0a6-129">-Metrica</span><span class="sxs-lookup"><span data-stu-id="cf0a6-129">-Metric</span></span>
<span data-ttu-id="cf0a6-130">Raccolta di query per la definizione delle metriche di configurazione.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="cf0a6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="cf0a6-131">-Name</span></span>
<span data-ttu-id="cf0a6-132">Identificatore della configurazione.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="cf0a6-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="cf0a6-133">-Priority</span></span>
<span data-ttu-id="cf0a6-134">Peso della configurazione del dispositivo in caso di regole concorrenti (il punteggio più alto).</span><span class="sxs-lookup"><span data-stu-id="cf0a6-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="cf0a6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0a6-135">-ResourceGroupName</span></span>
<span data-ttu-id="cf0a6-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cf0a6-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cf0a6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf0a6-137">-ResourceId</span></span>
<span data-ttu-id="cf0a6-138">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="cf0a6-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cf0a6-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="cf0a6-139">-TargetCondition</span></span>
<span data-ttu-id="cf0a6-140">Condizione di destinazione in cui si applica una configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="cf0a6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf0a6-141">-Confirm</span></span>
<span data-ttu-id="cf0a6-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf0a6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0a6-143">-WhatIf</span></span>
<span data-ttu-id="cf0a6-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0a6-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf0a6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0a6-146">CommonParameters</span></span>
<span data-ttu-id="cf0a6-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf0a6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0a6-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf0a6-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0a6-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf0a6-149">INPUTS</span></span>

### <span data-ttu-id="cf0a6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cf0a6-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cf0a6-151">System.String</span><span class="sxs-lookup"><span data-stu-id="cf0a6-151">System.String</span></span>

## <span data-ttu-id="cf0a6-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf0a6-152">OUTPUTS</span></span>

### <span data-ttu-id="cf0a6-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf0a6-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="cf0a6-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf0a6-154">NOTES</span></span>

## <span data-ttu-id="cf0a6-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf0a6-155">RELATED LINKS</span></span>
