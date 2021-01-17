---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347491"
---
# <span data-ttu-id="bec2e-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="bec2e-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="bec2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bec2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bec2e-103">Aggiornare i campi modificabili della registrazione della configurazione.</span><span class="sxs-lookup"><span data-stu-id="bec2e-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="bec2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bec2e-104">SYNTAX</span></span>

### <span data-ttu-id="bec2e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bec2e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec2e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bec2e-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec2e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bec2e-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec2e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bec2e-108">DESCRIPTION</span></span>
<span data-ttu-id="bec2e-109">Aggiornare le proprietà specificate di una configurazione di gestione dei dispositivi automatica.</span><span class="sxs-lookup"><span data-stu-id="bec2e-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="bec2e-110">Nota: il contenuto della configurazione non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="bec2e-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="bec2e-111">Le proprietà di configurazione che possono essere aggiornate sono "etichette", "metriche", "priorità" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="bec2e-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="bec2e-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="bec2e-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="bec2e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bec2e-113">EXAMPLES</span></span>

### <span data-ttu-id="bec2e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bec2e-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="bec2e-115">Modificare la priorità di una configurazione del dispositivo e aggiornarne la condizione di destinazione</span><span class="sxs-lookup"><span data-stu-id="bec2e-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="bec2e-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bec2e-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="bec2e-117">Aggiornare le metriche e le etichette di una configurazione di dispositivo</span><span class="sxs-lookup"><span data-stu-id="bec2e-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="bec2e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bec2e-118">PARAMETERS</span></span>

### <span data-ttu-id="bec2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec2e-119">-DefaultProfile</span></span>
<span data-ttu-id="bec2e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bec2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec2e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bec2e-121">-Force</span></span>
<span data-ttu-id="bec2e-122">Consente di sostituire l'oggetto di configurazione anche se è stato aggiornato da quando è stato recuperato l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="bec2e-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="bec2e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bec2e-123">-InputObject</span></span>
<span data-ttu-id="bec2e-124">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="bec2e-124">IotHub object</span></span>

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

### <span data-ttu-id="bec2e-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bec2e-125">-IotHubName</span></span>
<span data-ttu-id="bec2e-126">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="bec2e-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bec2e-127">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="bec2e-127">-Label</span></span>
<span data-ttu-id="bec2e-128">Mappa delle etichette da applicare alla configurazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bec2e-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="bec2e-129">-Metrica</span><span class="sxs-lookup"><span data-stu-id="bec2e-129">-Metric</span></span>
<span data-ttu-id="bec2e-130">Raccolta query per la definizione delle metriche di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bec2e-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="bec2e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="bec2e-131">-Name</span></span>
<span data-ttu-id="bec2e-132">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="bec2e-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="bec2e-133">-Priorità</span><span class="sxs-lookup"><span data-stu-id="bec2e-133">-Priority</span></span>
<span data-ttu-id="bec2e-134">Peso della configurazione del dispositivo in caso di regole concorrenti (vittorie più alte).</span><span class="sxs-lookup"><span data-stu-id="bec2e-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="bec2e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec2e-135">-ResourceGroupName</span></span>
<span data-ttu-id="bec2e-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bec2e-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bec2e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bec2e-137">-ResourceId</span></span>
<span data-ttu-id="bec2e-138">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="bec2e-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bec2e-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="bec2e-139">-TargetCondition</span></span>
<span data-ttu-id="bec2e-140">Condizione di destinazione in cui si applica una configurazione di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bec2e-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="bec2e-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bec2e-141">-Confirm</span></span>
<span data-ttu-id="bec2e-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec2e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec2e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec2e-143">-WhatIf</span></span>
<span data-ttu-id="bec2e-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bec2e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec2e-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bec2e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec2e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec2e-146">CommonParameters</span></span>
<span data-ttu-id="bec2e-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec2e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec2e-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec2e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec2e-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bec2e-149">INPUTS</span></span>

### <span data-ttu-id="bec2e-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bec2e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bec2e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bec2e-151">System.String</span></span>

## <span data-ttu-id="bec2e-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bec2e-152">OUTPUTS</span></span>

### <span data-ttu-id="bec2e-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="bec2e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="bec2e-154">Note</span><span class="sxs-lookup"><span data-stu-id="bec2e-154">NOTES</span></span>

## <span data-ttu-id="bec2e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bec2e-155">RELATED LINKS</span></span>
