---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022361"
---
# <span data-ttu-id="637ad-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="637ad-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="637ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="637ad-102">SYNOPSIS</span></span>
<span data-ttu-id="637ad-103">Crea un passaggio.</span><span class="sxs-lookup"><span data-stu-id="637ad-103">Creates a step.</span></span>

## <span data-ttu-id="637ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="637ad-104">SYNTAX</span></span>

### <span data-ttu-id="637ad-105">Wait (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="637ad-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="637ad-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="637ad-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="637ad-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="637ad-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="637ad-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="637ad-108">DESCRIPTION</span></span>
<span data-ttu-id="637ad-109">Il cmdlet **New-AzDeploymentManagerStep** crea un passaggio di distribuzione a cui è possibile fare riferimento in rollout.</span><span class="sxs-lookup"><span data-stu-id="637ad-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="637ad-110">Specificare il *nome* , *ResourceGroupName* e le proprietà obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="637ad-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="637ad-111">Puoi modificare l'oggetto restituito localmente e quindi applicare le modifiche apportate al passaggio usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="637ad-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="637ad-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="637ad-112">EXAMPLES</span></span>

### <span data-ttu-id="637ad-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="637ad-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="637ad-114">Crea un passaggio in ContosoResourceGroup con il nome ContosoService1WaitStep con il centro degli Stati Uniti come posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="637ad-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="637ad-115">La proprietà Duration fornisce la durata in cui l'implementazione verrà attesa prima di eseguire il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="637ad-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="637ad-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="637ad-116">PARAMETERS</span></span>

### <span data-ttu-id="637ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637ad-117">-DefaultProfile</span></span>
<span data-ttu-id="637ad-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="637ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="637ad-119">-Durata</span><span class="sxs-lookup"><span data-stu-id="637ad-119">-Duration</span></span>
<span data-ttu-id="637ad-120">Durata da attendere in formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="637ad-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="637ad-121">Ad esempio: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="637ad-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="637ad-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="637ad-122">-HealthCheckProperties</span></span>
<span data-ttu-id="637ad-123">Proprietà controllo integrità.</span><span class="sxs-lookup"><span data-stu-id="637ad-123">The health check properties.</span></span>

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

### <span data-ttu-id="637ad-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="637ad-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="637ad-125">Percorso del file in cui sono definite le proprietà di controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="637ad-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="637ad-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="637ad-126">-Location</span></span>
<span data-ttu-id="637ad-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="637ad-127">The location of the resource.</span></span>

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

### <span data-ttu-id="637ad-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="637ad-128">-Name</span></span>
<span data-ttu-id="637ad-129">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="637ad-129">The name of the step.</span></span>

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

### <span data-ttu-id="637ad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637ad-130">-ResourceGroupName</span></span>
<span data-ttu-id="637ad-131">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="637ad-131">The resource group.</span></span>

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

### <span data-ttu-id="637ad-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="637ad-132">-Tag</span></span>
<span data-ttu-id="637ad-133">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="637ad-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="637ad-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="637ad-134">-Confirm</span></span>
<span data-ttu-id="637ad-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="637ad-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="637ad-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="637ad-136">-WhatIf</span></span>
<span data-ttu-id="637ad-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="637ad-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="637ad-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="637ad-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="637ad-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637ad-139">CommonParameters</span></span>
<span data-ttu-id="637ad-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="637ad-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637ad-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="637ad-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637ad-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="637ad-142">INPUTS</span></span>

### <span data-ttu-id="637ad-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="637ad-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="637ad-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="637ad-144">OUTPUTS</span></span>

### <span data-ttu-id="637ad-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="637ad-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="637ad-146">Note</span><span class="sxs-lookup"><span data-stu-id="637ad-146">NOTES</span></span>

## <span data-ttu-id="637ad-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="637ad-147">RELATED LINKS</span></span>
