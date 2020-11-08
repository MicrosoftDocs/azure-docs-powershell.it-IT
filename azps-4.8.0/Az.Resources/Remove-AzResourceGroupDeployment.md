---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188902"
---
# <span data-ttu-id="b7ae6-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7ae6-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b7ae6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ae6-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="b7ae6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7ae6-104">SYNTAX</span></span>

### <span data-ttu-id="b7ae6-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7ae6-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ae6-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b7ae6-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ae6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7ae6-107">DESCRIPTION</span></span>

<span data-ttu-id="b7ae6-108">Il cmdlet **Remove-AzResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="b7ae6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7ae6-109">EXAMPLES</span></span>

### <span data-ttu-id="b7ae6-110">Esempio 1: rimuove una distribuzione di un gruppo di risorse con ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ae6-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="b7ae6-111">Questo comando rimuove una distribuzione di un gruppo di risorse con l'ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b7ae6-112">La rimozione riuscita restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-112">Successful removal returns true.</span></span>

### <span data-ttu-id="b7ae6-113">Esempio 2: rimuove una distribuzione di un gruppo di risorse con ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="b7ae6-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="b7ae6-114">Questo comando rimuove una distribuzione di un gruppo di risorse con il ResourceGroupName e il ResourceName forniti.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="b7ae6-115">La rimozione riuscita restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-115">Successful removal returns true.</span></span>

## <span data-ttu-id="b7ae6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7ae6-116">PARAMETERS</span></span>

### <span data-ttu-id="b7ae6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b7ae6-117">-ApiVersion</span></span>
<span data-ttu-id="b7ae6-118">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b7ae6-119">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ae6-120">-DefaultProfile</span></span>
<span data-ttu-id="b7ae6-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7ae6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7ae6-122">-ID</span><span class="sxs-lookup"><span data-stu-id="b7ae6-122">-Id</span></span>
<span data-ttu-id="b7ae6-123">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-123">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7ae6-124">-Name</span></span>
<span data-ttu-id="b7ae6-125">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-125">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="b7ae6-126">-Pre</span></span>
<span data-ttu-id="b7ae6-127">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b7ae6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ae6-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7ae6-129">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-129">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7ae6-130">-Confirm</span></span>
<span data-ttu-id="b7ae6-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ae6-132">-WhatIf</span></span>
<span data-ttu-id="b7ae6-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ae6-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ae6-135">CommonParameters</span></span>
<span data-ttu-id="b7ae6-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ae6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ae6-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7ae6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ae6-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7ae6-138">INPUTS</span></span>

### <span data-ttu-id="b7ae6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ae6-139">System.String</span></span>

## <span data-ttu-id="b7ae6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7ae6-140">OUTPUTS</span></span>

### <span data-ttu-id="b7ae6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7ae6-141">System.Boolean</span></span>

## <span data-ttu-id="b7ae6-142">Note</span><span class="sxs-lookup"><span data-stu-id="b7ae6-142">NOTES</span></span>

## <span data-ttu-id="b7ae6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7ae6-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7ae6-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7ae6-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="b7ae6-145">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7ae6-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="b7ae6-146">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7ae6-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="b7ae6-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7ae6-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


