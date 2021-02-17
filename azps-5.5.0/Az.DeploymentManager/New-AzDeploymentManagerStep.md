---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208619"
---
# <span data-ttu-id="3b5c6-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="3b5c6-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="3b5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5c6-103">Crea un passaggio.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-103">Creates a step.</span></span>

## <span data-ttu-id="3b5c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b5c6-104">SYNTAX</span></span>

### <span data-ttu-id="3b5c6-105">Attendi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b5c6-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5c6-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="3b5c6-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5c6-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="3b5c6-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b5c6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3b5c6-108">DESCRIPTION</span></span>
<span data-ttu-id="3b5c6-109">Il cmdlet **New-AzDeploymentManagerStep** crea un passaggio di distribuzione a cui è possibile fare riferimento nelle implementazioni.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="3b5c6-110">Specificare le *proprietà Name,* *ResourceGroupName* e required.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="3b5c6-111">È possibile modificare l'oggetto restituito in locale e quindi applicare le modifiche al passaggio usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="3b5c6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b5c6-112">EXAMPLES</span></span>

### <span data-ttu-id="3b5c6-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b5c6-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="3b5c6-114">Crea un passaggio in ContosoResourceGroup con il nome ContosoService1WaitStep con Stati Uniti centrali come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="3b5c6-115">La proprietà Durata fornisce la durata dell'implementazione prima di eseguire il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="3b5c6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b5c6-116">PARAMETERS</span></span>

### <span data-ttu-id="3b5c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5c6-117">-DefaultProfile</span></span>
<span data-ttu-id="3b5c6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b5c6-119">-Durata</span><span class="sxs-lookup"><span data-stu-id="3b5c6-119">-Duration</span></span>
<span data-ttu-id="3b5c6-120">La durata di attesa nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="3b5c6-121">Ad esempio: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="3b5c6-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5c6-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="3b5c6-122">-HealthCheckProperties</span></span>
<span data-ttu-id="3b5c6-123">Proprietà della verifica dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5c6-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="3b5c6-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="3b5c6-125">Percorso del file in cui sono definite le proprietà della verifica dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b5c6-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3b5c6-126">-Location</span></span>
<span data-ttu-id="3b5c6-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-127">The location of the resource.</span></span>

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

### <span data-ttu-id="3b5c6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3b5c6-128">-Name</span></span>
<span data-ttu-id="3b5c6-129">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-129">The name of the step.</span></span>

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

### <span data-ttu-id="3b5c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b5c6-131">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-131">The resource group.</span></span>

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

### <span data-ttu-id="3b5c6-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b5c6-132">-Tag</span></span>
<span data-ttu-id="3b5c6-133">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3b5c6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b5c6-134">-Confirm</span></span>
<span data-ttu-id="3b5c6-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5c6-136">-WhatIf</span></span>
<span data-ttu-id="3b5c6-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b5c6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5c6-139">CommonParameters</span></span>
<span data-ttu-id="3b5c6-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5c6-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3b5c6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5c6-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3b5c6-142">INPUTS</span></span>

### <span data-ttu-id="3b5c6-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b5c6-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b5c6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b5c6-144">OUTPUTS</span></span>

### <span data-ttu-id="3b5c6-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="3b5c6-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="3b5c6-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="3b5c6-146">NOTES</span></span>

## <span data-ttu-id="3b5c6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b5c6-147">RELATED LINKS</span></span>
