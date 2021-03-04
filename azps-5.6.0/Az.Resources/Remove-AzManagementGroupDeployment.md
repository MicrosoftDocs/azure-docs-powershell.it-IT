---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: 06f3dec483c2c8b5e1730cb1046f927d6d38a7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967693"
---
# <span data-ttu-id="c323f-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c323f-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c323f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c323f-102">SYNOPSIS</span></span>
<span data-ttu-id="c323f-103">Rimuove una distribuzione da un gruppo di gestione ed eventuali operazioni associate</span><span class="sxs-lookup"><span data-stu-id="c323f-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="c323f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c323f-104">SYNTAX</span></span>

### <span data-ttu-id="c323f-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c323f-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c323f-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c323f-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c323f-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c323f-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c323f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c323f-108">DESCRIPTION</span></span>
<span data-ttu-id="c323f-109">Il cmdlet **Remove-AzManagementGroupDeployment** rimuove una distribuzione di Azure in un gruppo di gestione ed eventuali operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="c323f-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="c323f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c323f-110">EXAMPLES</span></span>

### <span data-ttu-id="c323f-111">Esempio 1: Rimuovere una distribuzione con un nome assegnato</span><span class="sxs-lookup"><span data-stu-id="c323f-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="c323f-112">Questo comando rimuove la distribuzione "RolesDeployment" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="c323f-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="c323f-113">Esempio 2: Ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="c323f-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="c323f-114">Questo comando recupera la distribuzione "RolesDeployment" dal gruppo di gestione "myMG" e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="c323f-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="c323f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c323f-115">PARAMETERS</span></span>

### <span data-ttu-id="c323f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c323f-116">-AsJob</span></span>
<span data-ttu-id="c323f-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c323f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c323f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c323f-118">-DefaultProfile</span></span>
<span data-ttu-id="c323f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c323f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c323f-120">-Id</span><span class="sxs-lookup"><span data-stu-id="c323f-120">-Id</span></span>
<span data-ttu-id="c323f-121">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c323f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c323f-122">Esempio: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c323f-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c323f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c323f-123">-InputObject</span></span>
<span data-ttu-id="c323f-124">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c323f-124">The deployment object.</span></span>

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

### <span data-ttu-id="c323f-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c323f-125">-ManagementGroupId</span></span>
<span data-ttu-id="c323f-126">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c323f-126">The management group id.</span></span>

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

### <span data-ttu-id="c323f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c323f-127">-Name</span></span>
<span data-ttu-id="c323f-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c323f-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="c323f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c323f-129">-PassThru</span></span>
<span data-ttu-id="c323f-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="c323f-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c323f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c323f-131">-Pre</span></span>
<span data-ttu-id="c323f-132">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c323f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c323f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c323f-133">-Confirm</span></span>
<span data-ttu-id="c323f-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c323f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c323f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c323f-135">-WhatIf</span></span>
<span data-ttu-id="c323f-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c323f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c323f-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c323f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c323f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c323f-138">CommonParameters</span></span>
<span data-ttu-id="c323f-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c323f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c323f-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c323f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c323f-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="c323f-141">INPUTS</span></span>

### <span data-ttu-id="c323f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c323f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c323f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c323f-143">OUTPUTS</span></span>

### <span data-ttu-id="c323f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c323f-144">System.Boolean</span></span>

## <span data-ttu-id="c323f-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="c323f-145">NOTES</span></span>

## <span data-ttu-id="c323f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c323f-146">RELATED LINKS</span></span>
