---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
ms.openlocfilehash: d8f54706ed37412f6b1081311d90d032b57d2a16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687756"
---
# <span data-ttu-id="ec301-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ec301-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="ec301-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec301-102">SYNOPSIS</span></span>
<span data-ttu-id="ec301-103">Cancal una distribuzione in corso</span><span class="sxs-lookup"><span data-stu-id="ec301-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec301-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec301-104">SYNTAX</span></span>

### <span data-ttu-id="ec301-105">StopByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec301-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec301-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ec301-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec301-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec301-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec301-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec301-108">DESCRIPTION</span></span>
<span data-ttu-id="ec301-109">Il cmdlet **Stop-AzureRmDeployment** Annulla una distribuzione all'ambito dell'abbonamento che è stata avviata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="ec301-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="ec301-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="ec301-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="ec301-111">Per creare una distribuzione in ambito abbonamento, usare il cmdlet New-AzureRmDeployment.</span><span class="sxs-lookup"><span data-stu-id="ec301-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="ec301-112">Questo cmdlet arresta una sola distribuzione in uso.</span><span class="sxs-lookup"><span data-stu-id="ec301-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="ec301-113">Usa il parametro *Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="ec301-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="ec301-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec301-114">EXAMPLES</span></span>

### <span data-ttu-id="ec301-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec301-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="ec301-116">Questo comando Annulla una distribuzione in corso "deployment01" nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ec301-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="ec301-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ec301-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="ec301-118">Questo comando ottiene la distribuzione "deployment01" nell'ambito corrente della sottoscrizione e la Annulla.</span><span class="sxs-lookup"><span data-stu-id="ec301-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="ec301-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec301-119">PARAMETERS</span></span>

### <span data-ttu-id="ec301-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec301-120">-ApiVersion</span></span>
<span data-ttu-id="ec301-121">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ec301-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec301-122">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="ec301-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ec301-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec301-123">-DefaultProfile</span></span>
<span data-ttu-id="ec301-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec301-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec301-125">-ID</span><span class="sxs-lookup"><span data-stu-id="ec301-125">-Id</span></span>
<span data-ttu-id="ec301-126">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ec301-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ec301-127">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ec301-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ec301-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec301-128">-InputObject</span></span>
<span data-ttu-id="ec301-129">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="ec301-129">The deployment object.</span></span>

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

### <span data-ttu-id="ec301-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec301-130">-Name</span></span>
<span data-ttu-id="ec301-131">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ec301-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="ec301-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec301-132">-PassThru</span></span>
<span data-ttu-id="ec301-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ec301-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ec301-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec301-134">-Pre</span></span>
<span data-ttu-id="ec301-135">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ec301-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec301-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec301-136">-Confirm</span></span>
<span data-ttu-id="ec301-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec301-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec301-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec301-138">-WhatIf</span></span>
<span data-ttu-id="ec301-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec301-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec301-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec301-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec301-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec301-141">CommonParameters</span></span>
<span data-ttu-id="ec301-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec301-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec301-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec301-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec301-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec301-144">INPUTS</span></span>

### <span data-ttu-id="ec301-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ec301-145">System.String</span></span>

## <span data-ttu-id="ec301-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec301-146">OUTPUTS</span></span>

### <span data-ttu-id="ec301-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec301-147">System.Boolean</span></span>

## <span data-ttu-id="ec301-148">Note</span><span class="sxs-lookup"><span data-stu-id="ec301-148">NOTES</span></span>

## <span data-ttu-id="ec301-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec301-149">RELATED LINKS</span></span>