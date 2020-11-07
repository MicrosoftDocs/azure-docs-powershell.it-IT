---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: dbc5238819c6dc7a7555dd1f95ec0ba3478f2b2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677309"
---
# <span data-ttu-id="9c010-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9c010-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="9c010-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c010-102">SYNOPSIS</span></span>
<span data-ttu-id="9c010-103">Rimuove una distribuzione e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="9c010-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="9c010-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c010-104">SYNTAX</span></span>

### <span data-ttu-id="9c010-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c010-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c010-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9c010-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c010-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c010-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c010-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c010-108">DESCRIPTION</span></span>
<span data-ttu-id="9c010-109">Il cmdlet **Remove-AzDeployment** rimuove una distribuzione di Azure all'ambito dell'abbonamento e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="9c010-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="9c010-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c010-110">EXAMPLES</span></span>

### <span data-ttu-id="9c010-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="9c010-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="9c010-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9c010-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="9c010-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="9c010-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="9c010-114">Questo comando ottiene la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="9c010-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="9c010-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c010-115">PARAMETERS</span></span>

### <span data-ttu-id="9c010-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c010-116">-ApiVersion</span></span>
<span data-ttu-id="9c010-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9c010-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c010-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="9c010-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9c010-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c010-119">-AsJob</span></span>
<span data-ttu-id="9c010-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9c010-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c010-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c010-121">-DefaultProfile</span></span>
<span data-ttu-id="9c010-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c010-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c010-123">-ID</span><span class="sxs-lookup"><span data-stu-id="9c010-123">-Id</span></span>
<span data-ttu-id="9c010-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9c010-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="9c010-125">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="9c010-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c010-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c010-126">-InputObject</span></span>
<span data-ttu-id="9c010-127">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="9c010-127">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c010-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c010-128">-Name</span></span>
<span data-ttu-id="9c010-129">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9c010-129">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c010-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c010-130">-PassThru</span></span>
<span data-ttu-id="9c010-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9c010-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9c010-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c010-132">-Pre</span></span>
<span data-ttu-id="9c010-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9c010-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9c010-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c010-134">-Confirm</span></span>
<span data-ttu-id="9c010-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c010-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c010-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c010-136">-WhatIf</span></span>
<span data-ttu-id="9c010-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c010-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c010-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c010-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c010-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c010-139">CommonParameters</span></span>
<span data-ttu-id="9c010-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c010-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c010-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c010-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c010-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c010-142">INPUTS</span></span>

### <span data-ttu-id="9c010-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="9c010-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9c010-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c010-144">OUTPUTS</span></span>

### <span data-ttu-id="9c010-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c010-145">System.Boolean</span></span>

## <span data-ttu-id="9c010-146">Note</span><span class="sxs-lookup"><span data-stu-id="9c010-146">NOTES</span></span>

## <span data-ttu-id="9c010-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c010-147">RELATED LINKS</span></span>