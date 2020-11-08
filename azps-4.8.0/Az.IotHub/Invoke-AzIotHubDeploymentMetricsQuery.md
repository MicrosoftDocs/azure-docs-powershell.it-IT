---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192877"
---
# <span data-ttu-id="8cc5a-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="8cc5a-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="8cc5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cc5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc5a-103">Richiamare una query metrica di distribuzione di Edge.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="8cc5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cc5a-104">SYNTAX</span></span>

### <span data-ttu-id="8cc5a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cc5a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cc5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8cc5a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cc5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8cc5a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cc5a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cc5a-108">DESCRIPTION</span></span>
<span data-ttu-id="8cc5a-109">Valutare una metrica personalizzata o di sistema di destinazione definita in una distribuzione di Edge molto.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="8cc5a-110">Esistono metriche di sistema predefinite che vengono calcolate tramite hub molto e non possono essere personalizzate.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="8cc5a-111">"Mirati" Mostra i dispositivi Edge molto corrispondenti alla condizione di destinazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="8cc5a-112">"Applicato" Mostra i dispositivi Edge con targeting per gli altri che non sono destinati a un'altra distribuzione con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="8cc5a-113">"Reporting Success" Mostra i dispositivi Edge molto che hanno riferito che i moduli sono stati distribuiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="8cc5a-114">"Segnalazione errore" Mostra i dispositivi Edge molto che hanno segnalato che uno o più moduli non sono stati distribuiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="8cc5a-115">Per analizzare ulteriormente l'errore, connettersi in remoto a tali dispositivi e visualizzare i file di log.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="8cc5a-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cc5a-116">EXAMPLES</span></span>

### <span data-ttu-id="8cc5a-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cc5a-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="8cc5a-118">Valuta la metrica "warningLimit" definita personalizzata.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="8cc5a-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8cc5a-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="8cc5a-120">Valutare la metrica del sistema "Reporting Success".</span><span class="sxs-lookup"><span data-stu-id="8cc5a-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="8cc5a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cc5a-121">PARAMETERS</span></span>

### <span data-ttu-id="8cc5a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc5a-122">-DefaultProfile</span></span>
<span data-ttu-id="8cc5a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc5a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cc5a-124">-InputObject</span></span>
<span data-ttu-id="8cc5a-125">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc5a-125">IotHub object</span></span>

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

### <span data-ttu-id="8cc5a-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8cc5a-126">-IotHubName</span></span>
<span data-ttu-id="8cc5a-127">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="8cc5a-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8cc5a-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="8cc5a-128">-MetricName</span></span>
<span data-ttu-id="8cc5a-129">Metrica di destinazione per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="8cc5a-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="8cc5a-130">-MetricType</span></span>
<span data-ttu-id="8cc5a-131">Indica la raccolta metrica da usare per la ricerca di una metrica.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="8cc5a-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cc5a-132">-Name</span></span>
<span data-ttu-id="8cc5a-133">Identificatore per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="8cc5a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cc5a-134">-ResourceGroupName</span></span>
<span data-ttu-id="8cc5a-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8cc5a-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8cc5a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cc5a-136">-ResourceId</span></span>
<span data-ttu-id="8cc5a-137">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc5a-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8cc5a-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cc5a-138">-Confirm</span></span>
<span data-ttu-id="8cc5a-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc5a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cc5a-140">-WhatIf</span></span>
<span data-ttu-id="8cc5a-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc5a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc5a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc5a-143">CommonParameters</span></span>
<span data-ttu-id="8cc5a-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc5a-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cc5a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc5a-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cc5a-146">INPUTS</span></span>

### <span data-ttu-id="8cc5a-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8cc5a-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8cc5a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8cc5a-148">System.String</span></span>

## <span data-ttu-id="8cc5a-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cc5a-149">OUTPUTS</span></span>

### <span data-ttu-id="8cc5a-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="8cc5a-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="8cc5a-151">Note</span><span class="sxs-lookup"><span data-stu-id="8cc5a-151">NOTES</span></span>

## <span data-ttu-id="8cc5a-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cc5a-152">RELATED LINKS</span></span>