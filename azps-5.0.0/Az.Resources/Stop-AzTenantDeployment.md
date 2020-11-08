---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200488"
---
# <span data-ttu-id="91090-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="91090-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="91090-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91090-102">SYNOPSIS</span></span>
<span data-ttu-id="91090-103">Annullare una distribuzione in uso in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="91090-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="91090-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91090-104">SYNTAX</span></span>

### <span data-ttu-id="91090-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="91090-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91090-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="91090-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91090-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="91090-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91090-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91090-108">DESCRIPTION</span></span>
<span data-ttu-id="91090-109">Il cmdlet **Stop-AzTenantDeployment** Annulla una distribuzione avviata ma non completata nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="91090-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="91090-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="91090-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="91090-111">Per creare una distribuzione in ambito tenant, usare il cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="91090-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="91090-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91090-112">EXAMPLES</span></span>

### <span data-ttu-id="91090-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91090-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="91090-114">Questo comando Annulla una distribuzione in corso "deployment01" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="91090-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="91090-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91090-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="91090-116">Questo comando ottiene la distribuzione "deployment01" nell'ambito del tenant corrente e la Annulla.</span><span class="sxs-lookup"><span data-stu-id="91090-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="91090-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91090-117">PARAMETERS</span></span>

### <span data-ttu-id="91090-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91090-118">-DefaultProfile</span></span>
<span data-ttu-id="91090-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91090-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91090-120">-ID</span><span class="sxs-lookup"><span data-stu-id="91090-120">-Id</span></span>
<span data-ttu-id="91090-121">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91090-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="91090-122">esempio:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="91090-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="91090-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91090-123">-InputObject</span></span>
<span data-ttu-id="91090-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="91090-124">The deployment object.</span></span>

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

### <span data-ttu-id="91090-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="91090-125">-Name</span></span>
<span data-ttu-id="91090-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91090-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91090-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91090-127">-PassThru</span></span>
<span data-ttu-id="91090-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="91090-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="91090-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="91090-129">-Pre</span></span>
<span data-ttu-id="91090-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="91090-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="91090-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91090-131">-Confirm</span></span>
<span data-ttu-id="91090-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91090-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91090-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91090-133">-WhatIf</span></span>
<span data-ttu-id="91090-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91090-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91090-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91090-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91090-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91090-136">CommonParameters</span></span>
<span data-ttu-id="91090-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91090-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91090-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91090-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91090-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91090-139">INPUTS</span></span>

### <span data-ttu-id="91090-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="91090-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="91090-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91090-141">OUTPUTS</span></span>

### <span data-ttu-id="91090-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91090-142">System.Boolean</span></span>

## <span data-ttu-id="91090-143">Note</span><span class="sxs-lookup"><span data-stu-id="91090-143">NOTES</span></span>

## <span data-ttu-id="91090-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91090-144">RELATED LINKS</span></span>
