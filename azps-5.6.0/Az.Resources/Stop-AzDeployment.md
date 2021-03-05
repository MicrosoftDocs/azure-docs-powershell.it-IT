---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 794cc94ece2452f1fd5518d64d4071d7fa6ec326
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963757"
---
# <span data-ttu-id="6e7b7-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6e7b7-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="6e7b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7b7-103">Annullare una distribuzione in esecuzione</span><span class="sxs-lookup"><span data-stu-id="6e7b7-103">Cancel a running deployment</span></span>

## <span data-ttu-id="6e7b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e7b7-104">SYNTAX</span></span>

### <span data-ttu-id="6e7b7-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e7b7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7b7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6e7b7-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e7b7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e7b7-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e7b7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="6e7b7-109">Il **cmdlet Stop-AzDeployment** annulla una distribuzione nell'ambito della sottoscrizione avviata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="6e7b7-110">Per arrestare una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio Provisioning, e non uno stato completato, ad esempio Provisioning effettuato o Non riuscito.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="6e7b7-111">Per creare una distribuzione con ambito di sottoscrizione, usare il cmdlet New-AzDeployment distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="6e7b7-112">Questo cmdlet interrompe solo una distribuzione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="6e7b7-113">Usare il *parametro Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="6e7b7-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e7b7-114">EXAMPLES</span></span>

### <span data-ttu-id="6e7b7-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e7b7-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="6e7b7-116">Questo comando annulla una distribuzione in esecuzione "deployment01" nell'ambito della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="6e7b7-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6e7b7-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="6e7b7-118">Questo comando recupera la distribuzione "deployment01" nell'ambito di sottoscrizione corrente e la annulla.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="6e7b7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e7b7-119">PARAMETERS</span></span>

### <span data-ttu-id="6e7b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7b7-120">-DefaultProfile</span></span>
<span data-ttu-id="6e7b7-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e7b7-122">-Id</span><span class="sxs-lookup"><span data-stu-id="6e7b7-122">-Id</span></span>
<span data-ttu-id="6e7b7-123">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6e7b7-124">Esempio: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6e7b7-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="6e7b7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e7b7-125">-InputObject</span></span>
<span data-ttu-id="6e7b7-126">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-126">The deployment object.</span></span>

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

### <span data-ttu-id="6e7b7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6e7b7-127">-Name</span></span>
<span data-ttu-id="6e7b7-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="6e7b7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e7b7-129">-PassThru</span></span>
<span data-ttu-id="6e7b7-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6e7b7-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6e7b7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e7b7-131">-Pre</span></span>
<span data-ttu-id="6e7b7-132">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6e7b7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e7b7-133">-Confirm</span></span>
<span data-ttu-id="6e7b7-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e7b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e7b7-135">-WhatIf</span></span>
<span data-ttu-id="6e7b7-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e7b7-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e7b7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7b7-138">CommonParameters</span></span>
<span data-ttu-id="6e7b7-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7b7-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e7b7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7b7-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e7b7-141">INPUTS</span></span>

### <span data-ttu-id="6e7b7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6e7b7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6e7b7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e7b7-143">OUTPUTS</span></span>

### <span data-ttu-id="6e7b7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e7b7-144">System.Boolean</span></span>

## <span data-ttu-id="6e7b7-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e7b7-145">NOTES</span></span>

## <span data-ttu-id="6e7b7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e7b7-146">RELATED LINKS</span></span>
