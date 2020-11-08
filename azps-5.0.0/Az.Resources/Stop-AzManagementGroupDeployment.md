---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200490"
---
# <span data-ttu-id="ce78f-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce78f-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ce78f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce78f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce78f-103">Annullamento di una distribuzione in corso in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="ce78f-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="ce78f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce78f-104">SYNTAX</span></span>

### <span data-ttu-id="ce78f-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce78f-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce78f-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ce78f-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce78f-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce78f-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce78f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce78f-108">DESCRIPTION</span></span>
<span data-ttu-id="ce78f-109">Il cmdlet **Stop-AzManagementGroupDeployment** Annulla una distribuzione avviata ma non completata in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ce78f-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="ce78f-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="ce78f-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="ce78f-111">Per creare una distribuzione in un gruppo di gestione, usare il cmdlet New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ce78f-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="ce78f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce78f-112">EXAMPLES</span></span>

### <span data-ttu-id="ce78f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce78f-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="ce78f-114">Questo comando Annulla una distribuzione in corso "deployment01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="ce78f-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="ce78f-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce78f-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="ce78f-116">Questo comando ottiene la distribuzione "deployment01" nel gruppo di gestione "myMG" e la Annulla.</span><span class="sxs-lookup"><span data-stu-id="ce78f-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="ce78f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce78f-117">PARAMETERS</span></span>

### <span data-ttu-id="ce78f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce78f-118">-DefaultProfile</span></span>
<span data-ttu-id="ce78f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce78f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce78f-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ce78f-120">-Id</span></span>
<span data-ttu-id="ce78f-121">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ce78f-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ce78f-122">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ce78f-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ce78f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce78f-123">-InputObject</span></span>
<span data-ttu-id="ce78f-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="ce78f-124">The deployment object.</span></span>

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

### <span data-ttu-id="ce78f-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ce78f-125">-ManagementGroupId</span></span>
<span data-ttu-id="ce78f-126">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ce78f-126">The management group id.</span></span>

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

### <span data-ttu-id="ce78f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce78f-127">-Name</span></span>
<span data-ttu-id="ce78f-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ce78f-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="ce78f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce78f-129">-PassThru</span></span>
<span data-ttu-id="ce78f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ce78f-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ce78f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ce78f-131">-Pre</span></span>
<span data-ttu-id="ce78f-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ce78f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ce78f-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce78f-133">-Confirm</span></span>
<span data-ttu-id="ce78f-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce78f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce78f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce78f-135">-WhatIf</span></span>
<span data-ttu-id="ce78f-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce78f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce78f-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce78f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce78f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce78f-138">CommonParameters</span></span>
<span data-ttu-id="ce78f-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce78f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce78f-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce78f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce78f-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce78f-141">INPUTS</span></span>

### <span data-ttu-id="ce78f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="ce78f-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ce78f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce78f-143">OUTPUTS</span></span>

### <span data-ttu-id="ce78f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce78f-144">System.Boolean</span></span>

## <span data-ttu-id="ce78f-145">Note</span><span class="sxs-lookup"><span data-stu-id="ce78f-145">NOTES</span></span>

## <span data-ttu-id="ce78f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce78f-146">RELATED LINKS</span></span>
