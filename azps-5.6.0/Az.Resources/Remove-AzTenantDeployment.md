---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: f995050e86189c1b84652895ad0434403c4e86d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979405"
---
# <span data-ttu-id="95433-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="95433-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="95433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95433-102">SYNOPSIS</span></span>
<span data-ttu-id="95433-103">Rimuove una distribuzione con ambito tenant ed eventuali operazioni associate</span><span class="sxs-lookup"><span data-stu-id="95433-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="95433-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95433-104">SYNTAX</span></span>

### <span data-ttu-id="95433-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95433-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95433-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="95433-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95433-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="95433-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95433-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="95433-108">DESCRIPTION</span></span>
<span data-ttu-id="95433-109">Il cmdlet **Remove-AzTenantDeployment** rimuove una distribuzione di Azure nell'ambito tenant corrente ed eventuali operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="95433-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="95433-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95433-110">EXAMPLES</span></span>

### <span data-ttu-id="95433-111">Esempio 1: Rimuovere una distribuzione con un nome assegnato</span><span class="sxs-lookup"><span data-stu-id="95433-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="95433-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="95433-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="95433-113">Esempio 2: Ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="95433-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="95433-114">Questo comando recupera la distribuzione "RolesDeployment" nell'ambito tenant corrente e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="95433-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="95433-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95433-115">PARAMETERS</span></span>

### <span data-ttu-id="95433-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95433-116">-AsJob</span></span>
<span data-ttu-id="95433-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="95433-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95433-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95433-118">-DefaultProfile</span></span>
<span data-ttu-id="95433-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95433-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95433-120">-Id</span><span class="sxs-lookup"><span data-stu-id="95433-120">-Id</span></span>
<span data-ttu-id="95433-121">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95433-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="95433-122">Esempio: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="95433-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="95433-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95433-123">-InputObject</span></span>
<span data-ttu-id="95433-124">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95433-124">The deployment object.</span></span>

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

### <span data-ttu-id="95433-125">-Name</span><span class="sxs-lookup"><span data-stu-id="95433-125">-Name</span></span>
<span data-ttu-id="95433-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="95433-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="95433-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95433-127">-PassThru</span></span>
<span data-ttu-id="95433-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="95433-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="95433-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="95433-129">-Pre</span></span>
<span data-ttu-id="95433-130">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="95433-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="95433-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95433-131">-Confirm</span></span>
<span data-ttu-id="95433-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95433-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95433-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95433-133">-WhatIf</span></span>
<span data-ttu-id="95433-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95433-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95433-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="95433-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95433-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95433-136">CommonParameters</span></span>
<span data-ttu-id="95433-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95433-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95433-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95433-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95433-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="95433-139">INPUTS</span></span>

### <span data-ttu-id="95433-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="95433-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="95433-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95433-141">OUTPUTS</span></span>

### <span data-ttu-id="95433-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="95433-142">System.Boolean</span></span>

## <span data-ttu-id="95433-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="95433-143">NOTES</span></span>

## <span data-ttu-id="95433-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95433-144">RELATED LINKS</span></span>
