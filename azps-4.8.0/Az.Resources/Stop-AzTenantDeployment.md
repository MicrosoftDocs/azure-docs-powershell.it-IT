---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188881"
---
# <span data-ttu-id="956d4-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="956d4-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="956d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="956d4-102">SYNOPSIS</span></span>
<span data-ttu-id="956d4-103">Annullare una distribuzione in uso in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="956d4-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="956d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="956d4-104">SYNTAX</span></span>

### <span data-ttu-id="956d4-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="956d4-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="956d4-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="956d4-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="956d4-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="956d4-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956d4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="956d4-108">DESCRIPTION</span></span>
<span data-ttu-id="956d4-109">Il cmdlet **Stop-AzTenantDeployment** Annulla una distribuzione avviata ma non completata nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="956d4-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="956d4-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="956d4-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="956d4-111">Per creare una distribuzione in ambito tenant, usare il cmdlet New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="956d4-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="956d4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="956d4-112">EXAMPLES</span></span>

### <span data-ttu-id="956d4-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="956d4-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="956d4-114">Questo comando Annulla una distribuzione in corso "deployment01" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="956d4-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="956d4-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="956d4-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="956d4-116">Questo comando ottiene la distribuzione "deployment01" nell'ambito del tenant corrente e la Annulla.</span><span class="sxs-lookup"><span data-stu-id="956d4-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="956d4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="956d4-117">PARAMETERS</span></span>

### <span data-ttu-id="956d4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="956d4-118">-ApiVersion</span></span>
<span data-ttu-id="956d4-119">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="956d4-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="956d4-120">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="956d4-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="956d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956d4-121">-DefaultProfile</span></span>
<span data-ttu-id="956d4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="956d4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="956d4-123">-ID</span><span class="sxs-lookup"><span data-stu-id="956d4-123">-Id</span></span>
<span data-ttu-id="956d4-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="956d4-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="956d4-125">esempio:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="956d4-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="956d4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="956d4-126">-InputObject</span></span>
<span data-ttu-id="956d4-127">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="956d4-127">The deployment object.</span></span>

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

### <span data-ttu-id="956d4-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="956d4-128">-Name</span></span>
<span data-ttu-id="956d4-129">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="956d4-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956d4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="956d4-130">-PassThru</span></span>
<span data-ttu-id="956d4-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="956d4-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="956d4-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="956d4-132">-Pre</span></span>
<span data-ttu-id="956d4-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="956d4-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="956d4-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="956d4-134">-Confirm</span></span>
<span data-ttu-id="956d4-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="956d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956d4-136">-WhatIf</span></span>
<span data-ttu-id="956d4-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="956d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956d4-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="956d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956d4-139">CommonParameters</span></span>
<span data-ttu-id="956d4-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="956d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956d4-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="956d4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956d4-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="956d4-142">INPUTS</span></span>

### <span data-ttu-id="956d4-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="956d4-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="956d4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="956d4-144">OUTPUTS</span></span>

### <span data-ttu-id="956d4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="956d4-145">System.Boolean</span></span>

## <span data-ttu-id="956d4-146">Note</span><span class="sxs-lookup"><span data-stu-id="956d4-146">NOTES</span></span>

## <span data-ttu-id="956d4-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="956d4-147">RELATED LINKS</span></span>
