---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300541"
---
# <span data-ttu-id="dee12-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dee12-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="dee12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dee12-102">SYNOPSIS</span></span>
<span data-ttu-id="dee12-103">Rimuove una distribuzione in un gruppo di gestione e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="dee12-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="dee12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dee12-104">SYNTAX</span></span>

### <span data-ttu-id="dee12-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dee12-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dee12-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="dee12-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dee12-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="dee12-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dee12-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dee12-108">DESCRIPTION</span></span>
<span data-ttu-id="dee12-109">Il cmdlet **Remove-AzManagementGroupDeployment** rimuove una distribuzione di Azure in un gruppo di gestione e in tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="dee12-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="dee12-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dee12-110">EXAMPLES</span></span>

### <span data-ttu-id="dee12-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="dee12-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="dee12-112">Questo comando rimuove la distribuzione "RolesDeployment" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="dee12-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="dee12-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="dee12-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="dee12-114">Questo comando ottiene la distribuzione "RolesDeployment" nel gruppo di gestione "myMG" e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="dee12-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="dee12-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dee12-115">PARAMETERS</span></span>

### <span data-ttu-id="dee12-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dee12-116">-AsJob</span></span>
<span data-ttu-id="dee12-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dee12-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dee12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee12-118">-DefaultProfile</span></span>
<span data-ttu-id="dee12-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dee12-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee12-120">-ID</span><span class="sxs-lookup"><span data-stu-id="dee12-120">-Id</span></span>
<span data-ttu-id="dee12-121">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dee12-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="dee12-122">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="dee12-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="dee12-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dee12-123">-InputObject</span></span>
<span data-ttu-id="dee12-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="dee12-124">The deployment object.</span></span>

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

### <span data-ttu-id="dee12-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="dee12-125">-ManagementGroupId</span></span>
<span data-ttu-id="dee12-126">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="dee12-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee12-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dee12-127">-Name</span></span>
<span data-ttu-id="dee12-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dee12-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee12-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dee12-129">-PassThru</span></span>
<span data-ttu-id="dee12-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dee12-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dee12-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="dee12-131">-Pre</span></span>
<span data-ttu-id="dee12-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="dee12-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dee12-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dee12-133">-Confirm</span></span>
<span data-ttu-id="dee12-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dee12-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee12-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee12-135">-WhatIf</span></span>
<span data-ttu-id="dee12-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee12-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee12-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dee12-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee12-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee12-138">CommonParameters</span></span>
<span data-ttu-id="dee12-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee12-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee12-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dee12-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee12-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dee12-141">INPUTS</span></span>

### <span data-ttu-id="dee12-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="dee12-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dee12-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dee12-143">OUTPUTS</span></span>

### <span data-ttu-id="dee12-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dee12-144">System.Boolean</span></span>

## <span data-ttu-id="dee12-145">Note</span><span class="sxs-lookup"><span data-stu-id="dee12-145">NOTES</span></span>

## <span data-ttu-id="dee12-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dee12-146">RELATED LINKS</span></span>
