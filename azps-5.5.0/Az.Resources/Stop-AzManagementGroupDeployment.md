---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208386"
---
# <span data-ttu-id="e33f7-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e33f7-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="e33f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e33f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e33f7-103">Annullare una distribuzione in esecuzione in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="e33f7-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="e33f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e33f7-104">SYNTAX</span></span>

### <span data-ttu-id="e33f7-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e33f7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e33f7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e33f7-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e33f7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="e33f7-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e33f7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e33f7-108">DESCRIPTION</span></span>
<span data-ttu-id="e33f7-109">Il cmdlet **Stop-AzManagementGroupDeployment** annulla una distribuzione avviata ma non completata in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="e33f7-110">Per arrestare una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio Provisioning, e non uno stato completato, ad esempio Provisioning effettuato o Non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e33f7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="e33f7-111">Per creare una distribuzione in un gruppo di gestione, usare il cmdlet New-AzManagementGroupDeployment distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="e33f7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e33f7-112">EXAMPLES</span></span>

### <span data-ttu-id="e33f7-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e33f7-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="e33f7-114">Questo comando annulla una distribuzione in esecuzione "deployment01" presso il gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="e33f7-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="e33f7-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e33f7-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="e33f7-116">Questo comando recupera la distribuzione "deployment01" presso il gruppo di gestione "myMG" e la annulla.</span><span class="sxs-lookup"><span data-stu-id="e33f7-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="e33f7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e33f7-117">PARAMETERS</span></span>

### <span data-ttu-id="e33f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e33f7-118">-DefaultProfile</span></span>
<span data-ttu-id="e33f7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e33f7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e33f7-120">-Id</span><span class="sxs-lookup"><span data-stu-id="e33f7-120">-Id</span></span>
<span data-ttu-id="e33f7-121">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e33f7-122">Esempio: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="e33f7-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e33f7-123">-InputObject</span></span>
<span data-ttu-id="e33f7-124">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f7-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e33f7-125">-ManagementGroupId</span></span>
<span data-ttu-id="e33f7-126">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e33f7-127">-Name</span></span>
<span data-ttu-id="e33f7-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e33f7-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e33f7-129">-PassThru</span></span>
<span data-ttu-id="e33f7-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="e33f7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e33f7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="e33f7-131">-Pre</span></span>
<span data-ttu-id="e33f7-132">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e33f7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e33f7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e33f7-133">-Confirm</span></span>
<span data-ttu-id="e33f7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e33f7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e33f7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e33f7-135">-WhatIf</span></span>
<span data-ttu-id="e33f7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e33f7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e33f7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e33f7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e33f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33f7-138">CommonParameters</span></span>
<span data-ttu-id="e33f7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e33f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33f7-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e33f7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33f7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="e33f7-141">INPUTS</span></span>

### <span data-ttu-id="e33f7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e33f7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e33f7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e33f7-143">OUTPUTS</span></span>

### <span data-ttu-id="e33f7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e33f7-144">System.Boolean</span></span>

## <span data-ttu-id="e33f7-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e33f7-145">NOTES</span></span>

## <span data-ttu-id="e33f7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e33f7-146">RELATED LINKS</span></span>
