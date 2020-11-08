---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193838"
---
# <span data-ttu-id="f6f51-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f6f51-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="f6f51-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6f51-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f51-103">Rimuove una distribuzione e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="f6f51-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="f6f51-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6f51-104">SYNTAX</span></span>

### <span data-ttu-id="f6f51-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6f51-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f51-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f6f51-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6f51-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6f51-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6f51-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6f51-108">DESCRIPTION</span></span>
<span data-ttu-id="f6f51-109">Il cmdlet **Remove-AzDeployment** rimuove una distribuzione di Azure all'ambito dell'abbonamento e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="f6f51-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="f6f51-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6f51-110">EXAMPLES</span></span>

### <span data-ttu-id="f6f51-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="f6f51-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="f6f51-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f6f51-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="f6f51-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="f6f51-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="f6f51-114">Questo comando ottiene la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="f6f51-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="f6f51-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6f51-115">PARAMETERS</span></span>

### <span data-ttu-id="f6f51-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6f51-116">-AsJob</span></span>
<span data-ttu-id="f6f51-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f6f51-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6f51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f51-118">-DefaultProfile</span></span>
<span data-ttu-id="f6f51-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6f51-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6f51-120">-ID</span><span class="sxs-lookup"><span data-stu-id="f6f51-120">-Id</span></span>
<span data-ttu-id="f6f51-121">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f6f51-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f6f51-122">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f6f51-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="f6f51-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6f51-123">-InputObject</span></span>
<span data-ttu-id="f6f51-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="f6f51-124">The deployment object.</span></span>

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

### <span data-ttu-id="f6f51-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6f51-125">-Name</span></span>
<span data-ttu-id="f6f51-126">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f6f51-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="f6f51-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6f51-127">-PassThru</span></span>
<span data-ttu-id="f6f51-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f6f51-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f6f51-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6f51-129">-Pre</span></span>
<span data-ttu-id="f6f51-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f6f51-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f6f51-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6f51-131">-Confirm</span></span>
<span data-ttu-id="f6f51-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6f51-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6f51-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6f51-133">-WhatIf</span></span>
<span data-ttu-id="f6f51-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6f51-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6f51-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6f51-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6f51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f51-136">CommonParameters</span></span>
<span data-ttu-id="f6f51-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6f51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f51-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6f51-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f51-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6f51-139">INPUTS</span></span>

### <span data-ttu-id="f6f51-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="f6f51-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f6f51-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6f51-141">OUTPUTS</span></span>

### <span data-ttu-id="f6f51-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6f51-142">System.Boolean</span></span>

## <span data-ttu-id="f6f51-143">Note</span><span class="sxs-lookup"><span data-stu-id="f6f51-143">NOTES</span></span>

## <span data-ttu-id="f6f51-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6f51-144">RELATED LINKS</span></span>
