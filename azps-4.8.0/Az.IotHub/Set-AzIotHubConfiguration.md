---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189704"
---
# <span data-ttu-id="22df5-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="22df5-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="22df5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22df5-102">SYNOPSIS</span></span>
<span data-ttu-id="22df5-103">Aggiornare i campi modificabili della registrazione della configurazione.</span><span class="sxs-lookup"><span data-stu-id="22df5-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="22df5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22df5-104">SYNTAX</span></span>

### <span data-ttu-id="22df5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22df5-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22df5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22df5-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22df5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="22df5-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22df5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22df5-108">DESCRIPTION</span></span>
<span data-ttu-id="22df5-109">Aggiornare le proprietà specificate di una configurazione di gestione dei dispositivi automatica.</span><span class="sxs-lookup"><span data-stu-id="22df5-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="22df5-110">Nota: il contenuto della configurazione non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="22df5-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="22df5-111">Le proprietà di configurazione che possono essere aggiornate sono "etichette", "metriche", "priorità" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="22df5-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="22df5-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="22df5-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="22df5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22df5-113">EXAMPLES</span></span>

### <span data-ttu-id="22df5-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22df5-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="22df5-115">Modificare la priorità di una configurazione del dispositivo e aggiornarne la condizione di destinazione</span><span class="sxs-lookup"><span data-stu-id="22df5-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="22df5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22df5-116">PARAMETERS</span></span>

### <span data-ttu-id="22df5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22df5-117">-DefaultProfile</span></span>
<span data-ttu-id="22df5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22df5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22df5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="22df5-119">-Force</span></span>
<span data-ttu-id="22df5-120">Consente di sostituire l'oggetto di configurazione anche se è stato aggiornato da quando è stato recuperato l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="22df5-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="22df5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22df5-121">-InputObject</span></span>
<span data-ttu-id="22df5-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="22df5-122">IotHub object</span></span>

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

### <span data-ttu-id="22df5-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="22df5-123">-IotHubName</span></span>
<span data-ttu-id="22df5-124">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="22df5-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="22df5-125">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="22df5-125">-Label</span></span>
<span data-ttu-id="22df5-126">Mappa delle etichette da applicare alla configurazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="22df5-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="22df5-127">-Metrica</span><span class="sxs-lookup"><span data-stu-id="22df5-127">-Metric</span></span>
<span data-ttu-id="22df5-128">Raccolta query per la definizione delle metriche di configurazione.</span><span class="sxs-lookup"><span data-stu-id="22df5-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="22df5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="22df5-129">-Name</span></span>
<span data-ttu-id="22df5-130">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="22df5-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="22df5-131">-Priorità</span><span class="sxs-lookup"><span data-stu-id="22df5-131">-Priority</span></span>
<span data-ttu-id="22df5-132">Peso della configurazione del dispositivo in caso di regole concorrenti (vittorie più alte).</span><span class="sxs-lookup"><span data-stu-id="22df5-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="22df5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22df5-133">-ResourceGroupName</span></span>
<span data-ttu-id="22df5-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="22df5-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="22df5-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22df5-135">-ResourceId</span></span>
<span data-ttu-id="22df5-136">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="22df5-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="22df5-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="22df5-137">-TargetCondition</span></span>
<span data-ttu-id="22df5-138">Condizione di destinazione in cui si applica una configurazione di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22df5-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="22df5-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22df5-139">-Confirm</span></span>
<span data-ttu-id="22df5-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22df5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22df5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22df5-141">-WhatIf</span></span>
<span data-ttu-id="22df5-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22df5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22df5-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22df5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22df5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22df5-144">CommonParameters</span></span>
<span data-ttu-id="22df5-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22df5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22df5-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22df5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22df5-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22df5-147">INPUTS</span></span>

### <span data-ttu-id="22df5-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="22df5-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="22df5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="22df5-149">System.String</span></span>

## <span data-ttu-id="22df5-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22df5-150">OUTPUTS</span></span>

### <span data-ttu-id="22df5-151">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="22df5-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="22df5-152">Note</span><span class="sxs-lookup"><span data-stu-id="22df5-152">NOTES</span></span>

## <span data-ttu-id="22df5-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22df5-153">RELATED LINKS</span></span>