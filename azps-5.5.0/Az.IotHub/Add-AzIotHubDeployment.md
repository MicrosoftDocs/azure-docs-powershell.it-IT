---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188278"
---
# <span data-ttu-id="bfb86-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="bfb86-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="bfb86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb86-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb86-103">Aggiungere una distribuzione Edge IoT in un Hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfb86-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="bfb86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfb86-104">SYNTAX</span></span>

### <span data-ttu-id="bfb86-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfb86-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb86-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bfb86-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfb86-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bfb86-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb86-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfb86-108">DESCRIPTION</span></span>
<span data-ttu-id="bfb86-109">Le distribuzioni Edge possono essere create con metriche definite dall'utente per la valutazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="bfb86-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="bfb86-110">Per https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="bfb86-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="bfb86-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfb86-111">EXAMPLES</span></span>

### <span data-ttu-id="bfb86-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bfb86-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="bfb86-113">Creare una distribuzione Edge con metadati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bfb86-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="bfb86-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bfb86-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="bfb86-115">Creare una distribuzione Edge con priorità 3 che si applica a una condizione quando un dispositivo è contrassegnato nell'edificio 9 e l'ambiente è "test".</span><span class="sxs-lookup"><span data-stu-id="bfb86-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="bfb86-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bfb86-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="bfb86-117">Crea una distribuzione Edge con metriche utente.</span><span class="sxs-lookup"><span data-stu-id="bfb86-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="bfb86-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="bfb86-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="bfb86-119">Creare una distribuzione Edge con etichette.</span><span class="sxs-lookup"><span data-stu-id="bfb86-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="bfb86-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="bfb86-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="bfb86-121">Creare una distribuzione Edge con contenuto.</span><span class="sxs-lookup"><span data-stu-id="bfb86-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="bfb86-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb86-122">PARAMETERS</span></span>

### <span data-ttu-id="bfb86-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb86-123">-DefaultProfile</span></span>
<span data-ttu-id="bfb86-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb86-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb86-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfb86-125">-InputObject</span></span>
<span data-ttu-id="bfb86-126">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="bfb86-126">IotHub object</span></span>

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

### <span data-ttu-id="bfb86-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bfb86-127">-IotHubName</span></span>
<span data-ttu-id="bfb86-128">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="bfb86-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bfb86-129">-Label</span><span class="sxs-lookup"><span data-stu-id="bfb86-129">-Label</span></span>
<span data-ttu-id="bfb86-130">Mappa di etichette da applicare alla distribuzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfb86-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="bfb86-131">-Metrica</span><span class="sxs-lookup"><span data-stu-id="bfb86-131">-Metric</span></span>
<span data-ttu-id="bfb86-132">Raccolta di query per la definizione delle metriche di distribuzione di IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb86-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="bfb86-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="bfb86-133">-ModulesContent</span></span>
<span data-ttu-id="bfb86-134">Contenuto della distribuzione dei moduli per dispositivi Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="bfb86-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="bfb86-135">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb86-135">-Name</span></span>
<span data-ttu-id="bfb86-136">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bfb86-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="bfb86-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="bfb86-137">-Priority</span></span>
<span data-ttu-id="bfb86-138">Peso della distribuzione in caso di regole concorrenti (il punteggio più alto).</span><span class="sxs-lookup"><span data-stu-id="bfb86-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="bfb86-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb86-139">-ResourceGroupName</span></span>
<span data-ttu-id="bfb86-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="bfb86-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bfb86-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfb86-141">-ResourceId</span></span>
<span data-ttu-id="bfb86-142">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="bfb86-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bfb86-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="bfb86-143">-TargetCondition</span></span>
<span data-ttu-id="bfb86-144">Condizione di destinazione in cui si applica una distribuzione Edge.</span><span class="sxs-lookup"><span data-stu-id="bfb86-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="bfb86-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb86-145">-Confirm</span></span>
<span data-ttu-id="bfb86-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb86-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb86-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb86-147">-WhatIf</span></span>
<span data-ttu-id="bfb86-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb86-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb86-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb86-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb86-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb86-150">CommonParameters</span></span>
<span data-ttu-id="bfb86-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb86-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb86-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb86-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb86-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfb86-153">INPUTS</span></span>

### <span data-ttu-id="bfb86-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bfb86-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bfb86-155">System.String</span><span class="sxs-lookup"><span data-stu-id="bfb86-155">System.String</span></span>

## <span data-ttu-id="bfb86-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfb86-156">OUTPUTS</span></span>

### <span data-ttu-id="bfb86-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="bfb86-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="bfb86-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfb86-158">NOTES</span></span>

## <span data-ttu-id="bfb86-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfb86-159">RELATED LINKS</span></span>
