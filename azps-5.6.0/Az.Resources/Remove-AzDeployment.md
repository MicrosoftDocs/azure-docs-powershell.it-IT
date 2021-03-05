---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 9aeba4d3d7b716910ddab1e63713bd6ef2bce17a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003102"
---
# <span data-ttu-id="b2a69-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b2a69-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="b2a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a69-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a69-103">Rimuove una distribuzione ed eventuali operazioni associate</span><span class="sxs-lookup"><span data-stu-id="b2a69-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="b2a69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2a69-104">SYNTAX</span></span>

### <span data-ttu-id="b2a69-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2a69-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2a69-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b2a69-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2a69-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2a69-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2a69-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b2a69-108">DESCRIPTION</span></span>
<span data-ttu-id="b2a69-109">Il cmdlet **Remove-AzDeployment rimuove** una distribuzione di Azure nell'ambito della sottoscrizione ed eventuali operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="b2a69-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="b2a69-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2a69-110">EXAMPLES</span></span>

### <span data-ttu-id="b2a69-111">Esempio 1: Rimuovere una distribuzione con un nome assegnato</span><span class="sxs-lookup"><span data-stu-id="b2a69-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="b2a69-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b2a69-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="b2a69-113">Esempio 2: Ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="b2a69-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="b2a69-114">Questo comando recupera la distribuzione "RolesDeployment" nell'ambito di sottoscrizione corrente e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="b2a69-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="b2a69-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2a69-115">PARAMETERS</span></span>

### <span data-ttu-id="b2a69-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2a69-116">-AsJob</span></span>
<span data-ttu-id="b2a69-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b2a69-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2a69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a69-118">-DefaultProfile</span></span>
<span data-ttu-id="b2a69-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2a69-120">-Id</span><span class="sxs-lookup"><span data-stu-id="b2a69-120">-Id</span></span>
<span data-ttu-id="b2a69-121">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b2a69-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b2a69-122">Esempio: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b2a69-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b2a69-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2a69-123">-InputObject</span></span>
<span data-ttu-id="b2a69-124">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b2a69-124">The deployment object.</span></span>

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

### <span data-ttu-id="b2a69-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b2a69-125">-Name</span></span>
<span data-ttu-id="b2a69-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b2a69-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="b2a69-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2a69-127">-PassThru</span></span>
<span data-ttu-id="b2a69-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b2a69-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b2a69-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="b2a69-129">-Pre</span></span>
<span data-ttu-id="b2a69-130">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b2a69-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b2a69-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2a69-131">-Confirm</span></span>
<span data-ttu-id="b2a69-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2a69-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2a69-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2a69-133">-WhatIf</span></span>
<span data-ttu-id="b2a69-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2a69-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2a69-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2a69-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2a69-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a69-136">CommonParameters</span></span>
<span data-ttu-id="b2a69-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a69-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a69-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2a69-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a69-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b2a69-139">INPUTS</span></span>

### <span data-ttu-id="b2a69-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b2a69-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b2a69-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2a69-141">OUTPUTS</span></span>

### <span data-ttu-id="b2a69-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b2a69-142">System.Boolean</span></span>

## <span data-ttu-id="b2a69-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b2a69-143">NOTES</span></span>

## <span data-ttu-id="b2a69-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2a69-144">RELATED LINKS</span></span>
