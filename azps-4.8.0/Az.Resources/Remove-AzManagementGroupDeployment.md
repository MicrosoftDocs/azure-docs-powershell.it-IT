---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031112"
---
# <span data-ttu-id="31e97-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31e97-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="31e97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31e97-102">SYNOPSIS</span></span>
<span data-ttu-id="31e97-103">Rimuove una distribuzione in un gruppo di gestione e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="31e97-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="31e97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31e97-104">SYNTAX</span></span>

### <span data-ttu-id="31e97-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31e97-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31e97-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="31e97-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31e97-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="31e97-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31e97-108">DESCRIPTION</span></span>
<span data-ttu-id="31e97-109">Il cmdlet **Remove-AzManagementGroupDeployment** rimuove una distribuzione di Azure in un gruppo di gestione e in tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="31e97-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="31e97-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31e97-110">EXAMPLES</span></span>

### <span data-ttu-id="31e97-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="31e97-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="31e97-112">Questo comando rimuove la distribuzione "RolesDeployment" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="31e97-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="31e97-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="31e97-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="31e97-114">Questo comando ottiene la distribuzione "RolesDeployment" nel gruppo di gestione "myMG" e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="31e97-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="31e97-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31e97-115">PARAMETERS</span></span>

### <span data-ttu-id="31e97-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="31e97-116">-ApiVersion</span></span>
<span data-ttu-id="31e97-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="31e97-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="31e97-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="31e97-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31e97-119">-AsJob</span></span>
<span data-ttu-id="31e97-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="31e97-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e97-121">-DefaultProfile</span></span>
<span data-ttu-id="31e97-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31e97-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-123">-ID</span><span class="sxs-lookup"><span data-stu-id="31e97-123">-Id</span></span>
<span data-ttu-id="31e97-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="31e97-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="31e97-125">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="31e97-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31e97-126">-InputObject</span></span>
<span data-ttu-id="31e97-127">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="31e97-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="31e97-128">-ManagementGroupId</span></span>
<span data-ttu-id="31e97-129">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="31e97-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="31e97-130">-Name</span></span>
<span data-ttu-id="31e97-131">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="31e97-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31e97-132">-PassThru</span></span>
<span data-ttu-id="31e97-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="31e97-133">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="31e97-134">-Pre</span></span>
<span data-ttu-id="31e97-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="31e97-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31e97-136">-Confirm</span></span>
<span data-ttu-id="31e97-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e97-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e97-138">-WhatIf</span></span>
<span data-ttu-id="31e97-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e97-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e97-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31e97-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31e97-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e97-141">CommonParameters</span></span>
<span data-ttu-id="31e97-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e97-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e97-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31e97-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e97-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31e97-144">INPUTS</span></span>

### <span data-ttu-id="31e97-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="31e97-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="31e97-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31e97-146">OUTPUTS</span></span>

### <span data-ttu-id="31e97-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31e97-147">System.Boolean</span></span>

## <span data-ttu-id="31e97-148">Note</span><span class="sxs-lookup"><span data-stu-id="31e97-148">NOTES</span></span>

## <span data-ttu-id="31e97-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31e97-149">RELATED LINKS</span></span>
