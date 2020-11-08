---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203291"
---
# <span data-ttu-id="6dea4-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dea4-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6dea4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dea4-102">SYNOPSIS</span></span>
<span data-ttu-id="6dea4-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="6dea4-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="6dea4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dea4-104">SYNTAX</span></span>

### <span data-ttu-id="6dea4-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dea4-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dea4-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6dea4-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dea4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dea4-107">DESCRIPTION</span></span>

<span data-ttu-id="6dea4-108">Il cmdlet **Remove-AzResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="6dea4-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="6dea4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dea4-109">EXAMPLES</span></span>

### <span data-ttu-id="6dea4-110">Esempio 1: rimuove una distribuzione di un gruppo di risorse con ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dea4-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="6dea4-111">Questo comando rimuove una distribuzione di un gruppo di risorse con l'ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6dea4-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6dea4-112">La rimozione riuscita restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="6dea4-112">Successful removal returns true.</span></span>

### <span data-ttu-id="6dea4-113">Esempio 2: rimuove una distribuzione di un gruppo di risorse con ResourceGroupName e resourceName</span><span class="sxs-lookup"><span data-stu-id="6dea4-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="6dea4-114">Questo comando rimuove una distribuzione di un gruppo di risorse con il ResourceGroupName e il ResourceName forniti.</span><span class="sxs-lookup"><span data-stu-id="6dea4-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="6dea4-115">La rimozione riuscita restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="6dea4-115">Successful removal returns true.</span></span>

## <span data-ttu-id="6dea4-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dea4-116">PARAMETERS</span></span>

### <span data-ttu-id="6dea4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dea4-117">-DefaultProfile</span></span>
<span data-ttu-id="6dea4-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6dea4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dea4-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6dea4-119">-Id</span></span>
<span data-ttu-id="6dea4-120">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6dea4-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="6dea4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dea4-121">-Name</span></span>
<span data-ttu-id="6dea4-122">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6dea4-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="6dea4-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="6dea4-123">-Pre</span></span>
<span data-ttu-id="6dea4-124">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6dea4-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6dea4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dea4-125">-ResourceGroupName</span></span>
<span data-ttu-id="6dea4-126">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6dea4-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="6dea4-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6dea4-127">-Confirm</span></span>
<span data-ttu-id="6dea4-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dea4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dea4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dea4-129">-WhatIf</span></span>
<span data-ttu-id="6dea4-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dea4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dea4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dea4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dea4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dea4-132">CommonParameters</span></span>
<span data-ttu-id="6dea4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dea4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dea4-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dea4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dea4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dea4-135">INPUTS</span></span>

### <span data-ttu-id="6dea4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6dea4-136">System.String</span></span>

## <span data-ttu-id="6dea4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dea4-137">OUTPUTS</span></span>

### <span data-ttu-id="6dea4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dea4-138">System.Boolean</span></span>

## <span data-ttu-id="6dea4-139">Note</span><span class="sxs-lookup"><span data-stu-id="6dea4-139">NOTES</span></span>

## <span data-ttu-id="6dea4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dea4-140">RELATED LINKS</span></span>

[<span data-ttu-id="6dea4-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dea4-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="6dea4-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dea4-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6dea4-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dea4-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="6dea4-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6dea4-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


