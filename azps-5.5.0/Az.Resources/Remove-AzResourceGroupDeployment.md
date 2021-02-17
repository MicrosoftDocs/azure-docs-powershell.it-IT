---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197967"
---
# <span data-ttu-id="66a40-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66a40-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="66a40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a40-102">SYNOPSIS</span></span>
<span data-ttu-id="66a40-103">Rimuove la distribuzione di un gruppo di risorse e le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="66a40-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="66a40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66a40-104">SYNTAX</span></span>

### <span data-ttu-id="66a40-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66a40-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66a40-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="66a40-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66a40-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="66a40-107">DESCRIPTION</span></span>

<span data-ttu-id="66a40-108">Il cmdlet **Remove-AzResourceGroupDeployment** rimuove la distribuzione di un gruppo di risorse di Azure e le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="66a40-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="66a40-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66a40-109">EXAMPLES</span></span>

### <span data-ttu-id="66a40-110">Esempio 1: Rimuove una distribuzione del gruppo di risorse con ResourceId</span><span class="sxs-lookup"><span data-stu-id="66a40-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="66a40-111">Questo comando rimuove una distribuzione del gruppo di risorse con l'ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="66a40-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="66a40-112">La rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="66a40-112">Successful removal returns true.</span></span>

### <span data-ttu-id="66a40-113">Esempio 2: Rimuove una distribuzione di un gruppo di risorse con ResourceGroupName e ResourceName</span><span class="sxs-lookup"><span data-stu-id="66a40-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="66a40-114">Questo comando rimuove una distribuzione del gruppo di risorse con i valori ResourceGroupName e ResourceName forniti.</span><span class="sxs-lookup"><span data-stu-id="66a40-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="66a40-115">La rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="66a40-115">Successful removal returns true.</span></span>

## <span data-ttu-id="66a40-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66a40-116">PARAMETERS</span></span>

### <span data-ttu-id="66a40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a40-117">-DefaultProfile</span></span>
<span data-ttu-id="66a40-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="66a40-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66a40-119">-Id</span><span class="sxs-lookup"><span data-stu-id="66a40-119">-Id</span></span>
<span data-ttu-id="66a40-120">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="66a40-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="66a40-121">-Name</span><span class="sxs-lookup"><span data-stu-id="66a40-121">-Name</span></span>
<span data-ttu-id="66a40-122">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="66a40-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="66a40-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="66a40-123">-Pre</span></span>
<span data-ttu-id="66a40-124">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="66a40-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66a40-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a40-125">-ResourceGroupName</span></span>
<span data-ttu-id="66a40-126">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="66a40-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="66a40-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66a40-127">-Confirm</span></span>
<span data-ttu-id="66a40-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66a40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66a40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a40-129">-WhatIf</span></span>
<span data-ttu-id="66a40-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a40-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66a40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66a40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a40-132">CommonParameters</span></span>
<span data-ttu-id="66a40-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a40-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66a40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a40-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="66a40-135">INPUTS</span></span>

### <span data-ttu-id="66a40-136">System.String</span><span class="sxs-lookup"><span data-stu-id="66a40-136">System.String</span></span>

## <span data-ttu-id="66a40-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66a40-137">OUTPUTS</span></span>

### <span data-ttu-id="66a40-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66a40-138">System.Boolean</span></span>

## <span data-ttu-id="66a40-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="66a40-139">NOTES</span></span>

## <span data-ttu-id="66a40-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66a40-140">RELATED LINKS</span></span>

[<span data-ttu-id="66a40-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66a40-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="66a40-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66a40-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="66a40-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66a40-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="66a40-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66a40-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


