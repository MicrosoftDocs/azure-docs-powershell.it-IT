---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: e6948bf1868865bb53bd3e1bfabc68aded44cd4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967598"
---
# <span data-ttu-id="b3155-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b3155-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="b3155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3155-102">SYNOPSIS</span></span>
<span data-ttu-id="b3155-103">Annullare una distribuzione in esecuzione nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="b3155-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="b3155-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3155-104">SYNTAX</span></span>

### <span data-ttu-id="b3155-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3155-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3155-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b3155-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3155-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3155-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3155-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3155-108">DESCRIPTION</span></span>
<span data-ttu-id="b3155-109">Il cmdlet **Stop-AzTenantDeployment** annulla una distribuzione avviata ma non completata in base all'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="b3155-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="b3155-110">Per arrestare una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio Provisioning, e non uno stato completato, ad esempio Provisioning effettuato o Non riuscito.</span><span class="sxs-lookup"><span data-stu-id="b3155-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b3155-111">Per creare una distribuzione nell'ambito tenant, usare il cmdlet New-AzTenantDeployment tenant.</span><span class="sxs-lookup"><span data-stu-id="b3155-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="b3155-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3155-112">EXAMPLES</span></span>

### <span data-ttu-id="b3155-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3155-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="b3155-114">Questo comando annulla una distribuzione in esecuzione "deployment01" nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="b3155-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="b3155-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b3155-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="b3155-116">Questo comando recupera la distribuzione "deployment01" nell'ambito tenant corrente e la annulla.</span><span class="sxs-lookup"><span data-stu-id="b3155-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="b3155-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3155-117">PARAMETERS</span></span>

### <span data-ttu-id="b3155-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3155-118">-DefaultProfile</span></span>
<span data-ttu-id="b3155-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3155-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3155-120">-Id</span><span class="sxs-lookup"><span data-stu-id="b3155-120">-Id</span></span>
<span data-ttu-id="b3155-121">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b3155-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b3155-122">Esempio: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b3155-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b3155-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3155-123">-InputObject</span></span>
<span data-ttu-id="b3155-124">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b3155-124">The deployment object.</span></span>

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

### <span data-ttu-id="b3155-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b3155-125">-Name</span></span>
<span data-ttu-id="b3155-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b3155-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="b3155-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3155-127">-PassThru</span></span>
<span data-ttu-id="b3155-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b3155-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b3155-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3155-129">-Pre</span></span>
<span data-ttu-id="b3155-130">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b3155-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b3155-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3155-131">-Confirm</span></span>
<span data-ttu-id="b3155-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3155-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3155-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3155-133">-WhatIf</span></span>
<span data-ttu-id="b3155-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3155-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3155-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3155-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3155-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3155-136">CommonParameters</span></span>
<span data-ttu-id="b3155-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3155-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3155-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3155-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3155-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3155-139">INPUTS</span></span>

### <span data-ttu-id="b3155-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b3155-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b3155-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3155-141">OUTPUTS</span></span>

### <span data-ttu-id="b3155-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3155-142">System.Boolean</span></span>

## <span data-ttu-id="b3155-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3155-143">NOTES</span></span>

## <span data-ttu-id="b3155-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3155-144">RELATED LINKS</span></span>
