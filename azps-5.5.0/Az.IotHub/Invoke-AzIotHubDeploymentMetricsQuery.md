---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200118"
---
# <span data-ttu-id="10414-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="10414-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="10414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10414-102">SYNOPSIS</span></span>
<span data-ttu-id="10414-103">Richiamare una query metrica di distribuzione di IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="10414-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="10414-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10414-104">SYNTAX</span></span>

### <span data-ttu-id="10414-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10414-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10414-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10414-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10414-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10414-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10414-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10414-108">DESCRIPTION</span></span>
<span data-ttu-id="10414-109">Valutare una metrica personalizzata o di sistema di destinazione definita in una distribuzione Edge IoT.</span><span class="sxs-lookup"><span data-stu-id="10414-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="10414-110">Esistono metriche di sistema predefinite che vengono calcolate dall'Hub Iot e non possono essere personalizzate.</span><span class="sxs-lookup"><span data-stu-id="10414-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="10414-111">"Mirato" mostra i dispositivi Edge IoT che corrispondono alla condizione di destinazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="10414-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="10414-112">"Applicato" mostra i dispositivi Edge IoT mirati non mirati da un'altra distribuzione con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="10414-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="10414-113">"Reporting Success" mostra i dispositivi IoT Edge che hanno segnalato che i moduli sono stati distribuiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="10414-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="10414-114">"Segnalazione errore" mostra i dispositivi IoT Edge che hanno segnalato che uno o più moduli non sono stati distribuiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="10414-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="10414-115">Per analizzare ulteriormente l'errore, connettersi in remoto a tali dispositivi e visualizzare i file di log.</span><span class="sxs-lookup"><span data-stu-id="10414-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="10414-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10414-116">EXAMPLES</span></span>

### <span data-ttu-id="10414-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10414-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="10414-118">Valutare la metrica personalizzata definita 'warningLimit'.</span><span class="sxs-lookup"><span data-stu-id="10414-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="10414-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="10414-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="10414-120">Valutare la metrica di sistema "Reporting Success".</span><span class="sxs-lookup"><span data-stu-id="10414-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="10414-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10414-121">PARAMETERS</span></span>

### <span data-ttu-id="10414-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10414-122">-DefaultProfile</span></span>
<span data-ttu-id="10414-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10414-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10414-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10414-124">-InputObject</span></span>
<span data-ttu-id="10414-125">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="10414-125">IotHub object</span></span>

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

### <span data-ttu-id="10414-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="10414-126">-IotHubName</span></span>
<span data-ttu-id="10414-127">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="10414-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="10414-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="10414-128">-MetricName</span></span>
<span data-ttu-id="10414-129">Metrica di destinazione per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="10414-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="10414-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="10414-130">-MetricType</span></span>
<span data-ttu-id="10414-131">Indica quale raccolta di metriche deve essere usata per cercare una metrica.</span><span class="sxs-lookup"><span data-stu-id="10414-131">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10414-132">-Name</span><span class="sxs-lookup"><span data-stu-id="10414-132">-Name</span></span>
<span data-ttu-id="10414-133">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="10414-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="10414-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10414-134">-ResourceGroupName</span></span>
<span data-ttu-id="10414-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="10414-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="10414-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10414-136">-ResourceId</span></span>
<span data-ttu-id="10414-137">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="10414-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="10414-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10414-138">-Confirm</span></span>
<span data-ttu-id="10414-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10414-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10414-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10414-140">-WhatIf</span></span>
<span data-ttu-id="10414-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10414-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10414-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10414-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10414-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10414-143">CommonParameters</span></span>
<span data-ttu-id="10414-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10414-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10414-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10414-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10414-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="10414-146">INPUTS</span></span>

### <span data-ttu-id="10414-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="10414-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="10414-148">System.String</span><span class="sxs-lookup"><span data-stu-id="10414-148">System.String</span></span>

## <span data-ttu-id="10414-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10414-149">OUTPUTS</span></span>

### <span data-ttu-id="10414-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="10414-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="10414-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="10414-151">NOTES</span></span>

## <span data-ttu-id="10414-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10414-152">RELATED LINKS</span></span>
