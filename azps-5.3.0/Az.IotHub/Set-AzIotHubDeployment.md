---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386567"
---
# <span data-ttu-id="62279-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="62279-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="62279-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62279-102">SYNOPSIS</span></span>
<span data-ttu-id="62279-103">Aggiornare i campi modificabili della distribuzione di Edge molto.</span><span class="sxs-lookup"><span data-stu-id="62279-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="62279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62279-104">SYNTAX</span></span>

### <span data-ttu-id="62279-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62279-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62279-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62279-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62279-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62279-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62279-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62279-108">DESCRIPTION</span></span>
<span data-ttu-id="62279-109">Aggiornare le proprietà specificate di una distribuzione di Edge molto.</span><span class="sxs-lookup"><span data-stu-id="62279-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="62279-110">Nota: il contenuto della configurazione non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="62279-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="62279-111">Le proprietà di configurazione che possono essere aggiornate sono "etichette", "metriche", "priorità" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="62279-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="62279-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="62279-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="62279-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62279-113">EXAMPLES</span></span>

### <span data-ttu-id="62279-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62279-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="62279-115">Modificare la priorità della distribuzione del bordo di un sacco e aggiornarne la condizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62279-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="62279-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="62279-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="62279-117">Aggiornare le metriche e le etichette della distribuzione di Edge di un sacco.</span><span class="sxs-lookup"><span data-stu-id="62279-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="62279-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62279-118">PARAMETERS</span></span>

### <span data-ttu-id="62279-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62279-119">-DefaultProfile</span></span>
<span data-ttu-id="62279-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62279-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62279-121">-Force</span><span class="sxs-lookup"><span data-stu-id="62279-121">-Force</span></span>
<span data-ttu-id="62279-122">Consente di sostituire l'oggetto di distribuzione anche se è stato aggiornato da quando è stato recuperato l'ultima volta.</span><span class="sxs-lookup"><span data-stu-id="62279-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="62279-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62279-123">-InputObject</span></span>
<span data-ttu-id="62279-124">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="62279-124">IotHub object</span></span>

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

### <span data-ttu-id="62279-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62279-125">-IotHubName</span></span>
<span data-ttu-id="62279-126">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="62279-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62279-127">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="62279-127">-Label</span></span>
<span data-ttu-id="62279-128">Mappa delle etichette da applicare alla distribuzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62279-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="62279-129">-Metrica</span><span class="sxs-lookup"><span data-stu-id="62279-129">-Metric</span></span>
<span data-ttu-id="62279-130">Raccolta query per la definizione di metriche per la distribuzione di Edge.</span><span class="sxs-lookup"><span data-stu-id="62279-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="62279-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="62279-131">-Name</span></span>
<span data-ttu-id="62279-132">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="62279-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="62279-133">-Priorità</span><span class="sxs-lookup"><span data-stu-id="62279-133">-Priority</span></span>
<span data-ttu-id="62279-134">Peso della distribuzione in caso di regole concorrenti (vittorie più alte).</span><span class="sxs-lookup"><span data-stu-id="62279-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="62279-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62279-135">-ResourceGroupName</span></span>
<span data-ttu-id="62279-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="62279-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62279-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62279-137">-ResourceId</span></span>
<span data-ttu-id="62279-138">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="62279-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62279-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="62279-139">-TargetCondition</span></span>
<span data-ttu-id="62279-140">Condizione di destinazione in cui si applica una distribuzione di Edge.</span><span class="sxs-lookup"><span data-stu-id="62279-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="62279-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62279-141">-Confirm</span></span>
<span data-ttu-id="62279-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62279-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62279-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62279-143">-WhatIf</span></span>
<span data-ttu-id="62279-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62279-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62279-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62279-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62279-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62279-146">CommonParameters</span></span>
<span data-ttu-id="62279-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62279-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62279-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62279-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62279-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62279-149">INPUTS</span></span>

### <span data-ttu-id="62279-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62279-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62279-151">System. String</span><span class="sxs-lookup"><span data-stu-id="62279-151">System.String</span></span>

## <span data-ttu-id="62279-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62279-152">OUTPUTS</span></span>

### <span data-ttu-id="62279-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="62279-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="62279-154">Note</span><span class="sxs-lookup"><span data-stu-id="62279-154">NOTES</span></span>

## <span data-ttu-id="62279-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62279-155">RELATED LINKS</span></span>
