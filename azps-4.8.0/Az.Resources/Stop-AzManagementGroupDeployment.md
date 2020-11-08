---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 8604aa58efff7b6fe7ef6dc931fdcb54b313d634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188263"
---
# <span data-ttu-id="3d4c0-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3d4c0-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="3d4c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4c0-103">Annullamento di una distribuzione in corso in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="3d4c0-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="3d4c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d4c0-104">SYNTAX</span></span>

### <span data-ttu-id="3d4c0-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3d4c0-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d4c0-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3d4c0-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d4c0-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c0-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d4c0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d4c0-108">DESCRIPTION</span></span>
<span data-ttu-id="3d4c0-109">Il cmdlet **Stop-AzManagementGroupDeployment** Annulla una distribuzione avviata ma non completata in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="3d4c0-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="3d4c0-111">Per creare una distribuzione in un gruppo di gestione, usare il cmdlet New-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="3d4c0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d4c0-112">EXAMPLES</span></span>

### <span data-ttu-id="3d4c0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d4c0-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="3d4c0-114">Questo comando Annulla una distribuzione in corso "deployment01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="3d4c0-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="3d4c0-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3d4c0-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="3d4c0-116">Questo comando ottiene la distribuzione "deployment01" nel gruppo di gestione "myMG" e la Annulla.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="3d4c0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d4c0-117">PARAMETERS</span></span>

### <span data-ttu-id="3d4c0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d4c0-118">-ApiVersion</span></span>
<span data-ttu-id="3d4c0-119">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d4c0-120">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3d4c0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4c0-121">-DefaultProfile</span></span>
<span data-ttu-id="3d4c0-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d4c0-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3d4c0-123">-Id</span></span>
<span data-ttu-id="3d4c0-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3d4c0-125">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3d4c0-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d4c0-126">-InputObject</span></span>
<span data-ttu-id="3d4c0-127">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c0-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3d4c0-128">-ManagementGroupId</span></span>
<span data-ttu-id="3d4c0-129">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c0-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="3d4c0-130">-Name</span></span>
<span data-ttu-id="3d4c0-131">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4c0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d4c0-132">-PassThru</span></span>
<span data-ttu-id="3d4c0-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3d4c0-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3d4c0-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d4c0-134">-Pre</span></span>
<span data-ttu-id="3d4c0-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3d4c0-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3d4c0-136">-Confirm</span></span>
<span data-ttu-id="3d4c0-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d4c0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d4c0-138">-WhatIf</span></span>
<span data-ttu-id="3d4c0-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d4c0-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d4c0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4c0-141">CommonParameters</span></span>
<span data-ttu-id="3d4c0-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d4c0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4c0-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d4c0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4c0-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d4c0-144">INPUTS</span></span>

### <span data-ttu-id="3d4c0-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="3d4c0-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3d4c0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d4c0-146">OUTPUTS</span></span>

### <span data-ttu-id="3d4c0-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d4c0-147">System.Boolean</span></span>

## <span data-ttu-id="3d4c0-148">Note</span><span class="sxs-lookup"><span data-stu-id="3d4c0-148">NOTES</span></span>

## <span data-ttu-id="3d4c0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d4c0-149">RELATED LINKS</span></span>
