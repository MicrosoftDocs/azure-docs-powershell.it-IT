---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354808"
---
# <span data-ttu-id="6776b-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6776b-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="6776b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6776b-102">SYNOPSIS</span></span>
<span data-ttu-id="6776b-103">Rimuove una distribuzione in ambito tenant e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="6776b-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="6776b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6776b-104">SYNTAX</span></span>

### <span data-ttu-id="6776b-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6776b-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6776b-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6776b-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6776b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="6776b-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6776b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6776b-108">DESCRIPTION</span></span>
<span data-ttu-id="6776b-109">Il cmdlet **Remove-AzTenantDeployment** rimuove una distribuzione di Azure nell'ambito del tenant corrente e in tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="6776b-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="6776b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6776b-110">EXAMPLES</span></span>

### <span data-ttu-id="6776b-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="6776b-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="6776b-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="6776b-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="6776b-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="6776b-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="6776b-114">Questo comando ottiene la distribuzione "RolesDeployment" nell'ambito del tenant corrente e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="6776b-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="6776b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6776b-115">PARAMETERS</span></span>

### <span data-ttu-id="6776b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6776b-116">-AsJob</span></span>
<span data-ttu-id="6776b-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6776b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6776b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6776b-118">-DefaultProfile</span></span>
<span data-ttu-id="6776b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6776b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6776b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="6776b-120">-Id</span></span>
<span data-ttu-id="6776b-121">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6776b-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6776b-122">esempio:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6776b-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="6776b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6776b-123">-InputObject</span></span>
<span data-ttu-id="6776b-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="6776b-124">The deployment object.</span></span>

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

### <span data-ttu-id="6776b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6776b-125">-Name</span></span>
<span data-ttu-id="6776b-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6776b-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="6776b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6776b-127">-PassThru</span></span>
<span data-ttu-id="6776b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6776b-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6776b-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="6776b-129">-Pre</span></span>
<span data-ttu-id="6776b-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6776b-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6776b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6776b-131">-Confirm</span></span>
<span data-ttu-id="6776b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6776b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6776b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6776b-133">-WhatIf</span></span>
<span data-ttu-id="6776b-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6776b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6776b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6776b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6776b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6776b-136">CommonParameters</span></span>
<span data-ttu-id="6776b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6776b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6776b-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6776b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6776b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6776b-139">INPUTS</span></span>

### <span data-ttu-id="6776b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="6776b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6776b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6776b-141">OUTPUTS</span></span>

### <span data-ttu-id="6776b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6776b-142">System.Boolean</span></span>

## <span data-ttu-id="6776b-143">Note</span><span class="sxs-lookup"><span data-stu-id="6776b-143">NOTES</span></span>

## <span data-ttu-id="6776b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6776b-144">RELATED LINKS</span></span>
