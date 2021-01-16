---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338671"
---
# <span data-ttu-id="ed48a-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="ed48a-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="ed48a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed48a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed48a-103">Richiamare una query metrica di configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed48a-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="ed48a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed48a-104">SYNTAX</span></span>

### <span data-ttu-id="ed48a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed48a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed48a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed48a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed48a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed48a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed48a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed48a-108">DESCRIPTION</span></span>
<span data-ttu-id="ed48a-109">Valutare una metrica personalizzata o di sistema di destinazione definita in una configurazione di dispositivo molto.</span><span class="sxs-lookup"><span data-stu-id="ed48a-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="ed48a-110">Esistono metriche di sistema predefinite che vengono calcolate tramite hub molto e non possono essere personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ed48a-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="ed48a-111">"Mirato" specifica il numero di gemelli di dispositivo corrispondenti alla condizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ed48a-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="ed48a-112">"Applicato" specifica il numero di gemelli di dispositivo modificati dalla configurazione.</span><span class="sxs-lookup"><span data-stu-id="ed48a-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="ed48a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed48a-113">EXAMPLES</span></span>

### <span data-ttu-id="ed48a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed48a-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="ed48a-115">Valuta la metrica "warningLimit" definita personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ed48a-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="ed48a-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ed48a-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="ed48a-117">Valutare la metrica del sistema "applicato".</span><span class="sxs-lookup"><span data-stu-id="ed48a-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="ed48a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed48a-118">PARAMETERS</span></span>

### <span data-ttu-id="ed48a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed48a-119">-DefaultProfile</span></span>
<span data-ttu-id="ed48a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed48a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed48a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed48a-121">-InputObject</span></span>
<span data-ttu-id="ed48a-122">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="ed48a-122">IotHub object</span></span>

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

### <span data-ttu-id="ed48a-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ed48a-123">-IotHubName</span></span>
<span data-ttu-id="ed48a-124">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="ed48a-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed48a-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="ed48a-125">-MetricName</span></span>
<span data-ttu-id="ed48a-126">Metrica di destinazione per la valutazione.</span><span class="sxs-lookup"><span data-stu-id="ed48a-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="ed48a-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="ed48a-127">-MetricType</span></span>
<span data-ttu-id="ed48a-128">Indica la raccolta metrica da usare per la ricerca di una metrica.</span><span class="sxs-lookup"><span data-stu-id="ed48a-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="ed48a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed48a-129">-Name</span></span>
<span data-ttu-id="ed48a-130">Identificatore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="ed48a-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="ed48a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed48a-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed48a-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ed48a-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed48a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed48a-133">-ResourceId</span></span>
<span data-ttu-id="ed48a-134">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="ed48a-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ed48a-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed48a-135">-Confirm</span></span>
<span data-ttu-id="ed48a-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed48a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed48a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed48a-137">-WhatIf</span></span>
<span data-ttu-id="ed48a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed48a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed48a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed48a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed48a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed48a-140">CommonParameters</span></span>
<span data-ttu-id="ed48a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed48a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed48a-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed48a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed48a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed48a-143">INPUTS</span></span>

### <span data-ttu-id="ed48a-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed48a-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed48a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ed48a-145">System.String</span></span>

## <span data-ttu-id="ed48a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed48a-146">OUTPUTS</span></span>

### <span data-ttu-id="ed48a-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="ed48a-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="ed48a-148">Note</span><span class="sxs-lookup"><span data-stu-id="ed48a-148">NOTES</span></span>

## <span data-ttu-id="ed48a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed48a-149">RELATED LINKS</span></span>
