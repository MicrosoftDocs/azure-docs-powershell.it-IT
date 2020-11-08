---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189932"
---
# <span data-ttu-id="adeb4-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="adeb4-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="adeb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="adeb4-103">Aggiungere una distribuzione di Edge molto in un hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="adeb4-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="adeb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adeb4-104">SYNTAX</span></span>

### <span data-ttu-id="adeb4-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adeb4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adeb4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="adeb4-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adeb4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="adeb4-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adeb4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adeb4-108">DESCRIPTION</span></span>
<span data-ttu-id="adeb4-109">Le distribuzioni Edge possono essere create con le metriche definite dall'utente per la valutazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="adeb4-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="adeb4-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="adeb4-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="adeb4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adeb4-111">EXAMPLES</span></span>

### <span data-ttu-id="adeb4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="adeb4-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="adeb4-113">Creare una distribuzione di Edge con metadati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="adeb4-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="adeb4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="adeb4-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="adeb4-115">Creare una distribuzione di Edge con una priorità di 3 che si applica alla condizione in cui un dispositivo è taggato nell'edificio 9 e l'ambiente è "test".</span><span class="sxs-lookup"><span data-stu-id="adeb4-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="adeb4-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="adeb4-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="adeb4-117">Creare una distribuzione di Edge con le metriche degli utenti.</span><span class="sxs-lookup"><span data-stu-id="adeb4-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="adeb4-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="adeb4-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="adeb4-119">Creare una distribuzione di Edge con etichette.</span><span class="sxs-lookup"><span data-stu-id="adeb4-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="adeb4-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="adeb4-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="adeb4-121">Creare una distribuzione di Edge con contenuto.</span><span class="sxs-lookup"><span data-stu-id="adeb4-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="adeb4-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adeb4-122">PARAMETERS</span></span>

### <span data-ttu-id="adeb4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adeb4-123">-DefaultProfile</span></span>
<span data-ttu-id="adeb4-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adeb4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adeb4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adeb4-125">-InputObject</span></span>
<span data-ttu-id="adeb4-126">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="adeb4-126">IotHub object</span></span>

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

### <span data-ttu-id="adeb4-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="adeb4-127">-IotHubName</span></span>
<span data-ttu-id="adeb4-128">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="adeb4-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="adeb4-129">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="adeb4-129">-Label</span></span>
<span data-ttu-id="adeb4-130">Mappa delle etichette da applicare alla distribuzione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="adeb4-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="adeb4-131">-Metrica</span><span class="sxs-lookup"><span data-stu-id="adeb4-131">-Metric</span></span>
<span data-ttu-id="adeb4-132">Raccolta query per la definizione di metriche per la distribuzione di Edge.</span><span class="sxs-lookup"><span data-stu-id="adeb4-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="adeb4-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="adeb4-133">-ModulesContent</span></span>
<span data-ttu-id="adeb4-134">Contenuto di distribuzione dei moduli per i dispositivi Edge molto.</span><span class="sxs-lookup"><span data-stu-id="adeb4-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="adeb4-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="adeb4-135">-Name</span></span>
<span data-ttu-id="adeb4-136">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="adeb4-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="adeb4-137">-Priorità</span><span class="sxs-lookup"><span data-stu-id="adeb4-137">-Priority</span></span>
<span data-ttu-id="adeb4-138">Peso della distribuzione in caso di regole concorrenti (vittorie più alte).</span><span class="sxs-lookup"><span data-stu-id="adeb4-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="adeb4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adeb4-139">-ResourceGroupName</span></span>
<span data-ttu-id="adeb4-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="adeb4-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="adeb4-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adeb4-141">-ResourceId</span></span>
<span data-ttu-id="adeb4-142">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="adeb4-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="adeb4-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="adeb4-143">-TargetCondition</span></span>
<span data-ttu-id="adeb4-144">Condizione di destinazione in cui si applica una distribuzione di Edge.</span><span class="sxs-lookup"><span data-stu-id="adeb4-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="adeb4-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adeb4-145">-Confirm</span></span>
<span data-ttu-id="adeb4-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adeb4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adeb4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adeb4-147">-WhatIf</span></span>
<span data-ttu-id="adeb4-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adeb4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adeb4-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adeb4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adeb4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adeb4-150">CommonParameters</span></span>
<span data-ttu-id="adeb4-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adeb4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adeb4-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adeb4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adeb4-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adeb4-153">INPUTS</span></span>

### <span data-ttu-id="adeb4-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="adeb4-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="adeb4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="adeb4-155">System.String</span></span>

## <span data-ttu-id="adeb4-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adeb4-156">OUTPUTS</span></span>

### <span data-ttu-id="adeb4-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="adeb4-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="adeb4-158">Note</span><span class="sxs-lookup"><span data-stu-id="adeb4-158">NOTES</span></span>

## <span data-ttu-id="adeb4-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adeb4-159">RELATED LINKS</span></span>