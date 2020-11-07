---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 7bd45da18565ae408ec71753f7f4527e53c2e4c1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866969"
---
# <span data-ttu-id="b70c2-101">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b70c2-101">Remove-AzureRmDeployment</span></span>

## <span data-ttu-id="b70c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b70c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b70c2-103">Rimuove una distribuzione e tutte le operazioni associate</span><span class="sxs-lookup"><span data-stu-id="b70c2-103">Removes a deployment and any associated operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b70c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b70c2-104">SYNTAX</span></span>

### <span data-ttu-id="b70c2-105">RemoveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b70c2-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzureRmDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b70c2-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b70c2-106">RemoveByDeploymentId</span></span>
```
Remove-AzureRmDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b70c2-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b70c2-107">RemoveByInputObject</span></span>
```
Remove-AzureRmDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b70c2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b70c2-108">DESCRIPTION</span></span>
<span data-ttu-id="b70c2-109">Il cmdlet **Remove-AzureRmDeployment** rimuove una distribuzione di Azure all'ambito dell'abbonamento e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="b70c2-109">The **Remove-AzureRmDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="b70c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b70c2-110">EXAMPLES</span></span>

### <span data-ttu-id="b70c2-111">Esempio 1: rimuovere una distribuzione con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="b70c2-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzureRmDeployment -Name "RolesDeployment"
```

<span data-ttu-id="b70c2-112">Questo comando rimuove la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b70c2-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="b70c2-113">Esempio 2: ottenere una distribuzione e rimuoverla</span><span class="sxs-lookup"><span data-stu-id="b70c2-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Remove-AzureRmDeployment
```

<span data-ttu-id="b70c2-114">Questo comando ottiene la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione e la rimuove.</span><span class="sxs-lookup"><span data-stu-id="b70c2-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="b70c2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b70c2-115">PARAMETERS</span></span>

### <span data-ttu-id="b70c2-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b70c2-116">-ApiVersion</span></span>
<span data-ttu-id="b70c2-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b70c2-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b70c2-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="b70c2-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b70c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b70c2-119">-AsJob</span></span>
<span data-ttu-id="b70c2-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b70c2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b70c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b70c2-121">-DefaultProfile</span></span>
<span data-ttu-id="b70c2-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b70c2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b70c2-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b70c2-123">-Id</span></span>
<span data-ttu-id="b70c2-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b70c2-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b70c2-125">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b70c2-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70c2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b70c2-126">-InputObject</span></span>
<span data-ttu-id="b70c2-127">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="b70c2-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b70c2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b70c2-128">-Name</span></span>
<span data-ttu-id="b70c2-129">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b70c2-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b70c2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b70c2-130">-PassThru</span></span>
<span data-ttu-id="b70c2-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b70c2-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b70c2-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b70c2-132">-Pre</span></span>
<span data-ttu-id="b70c2-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b70c2-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b70c2-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b70c2-134">-Confirm</span></span>
<span data-ttu-id="b70c2-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b70c2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b70c2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b70c2-136">-WhatIf</span></span>
<span data-ttu-id="b70c2-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b70c2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b70c2-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b70c2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b70c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b70c2-139">CommonParameters</span></span>
<span data-ttu-id="b70c2-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b70c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b70c2-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b70c2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b70c2-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b70c2-142">INPUTS</span></span>

### <span data-ttu-id="b70c2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b70c2-143">System.String</span></span>

## <span data-ttu-id="b70c2-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b70c2-144">OUTPUTS</span></span>

### <span data-ttu-id="b70c2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b70c2-145">System.Boolean</span></span>

## <span data-ttu-id="b70c2-146">Note</span><span class="sxs-lookup"><span data-stu-id="b70c2-146">NOTES</span></span>

## <span data-ttu-id="b70c2-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b70c2-147">RELATED LINKS</span></span>
