---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677290"
---
# <span data-ttu-id="4a73e-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a73e-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4a73e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a73e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a73e-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="4a73e-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4a73e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a73e-104">SYNTAX</span></span>

### <span data-ttu-id="4a73e-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a73e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a73e-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4a73e-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a73e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a73e-107">DESCRIPTION</span></span>
<span data-ttu-id="4a73e-108">Il cmdlet **Remove-AzResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="4a73e-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4a73e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a73e-109">EXAMPLES</span></span>

## <span data-ttu-id="4a73e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a73e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a73e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4a73e-111">-ApiVersion</span></span>
<span data-ttu-id="4a73e-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a73e-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4a73e-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4a73e-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4a73e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a73e-114">-DefaultProfile</span></span>
<span data-ttu-id="4a73e-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a73e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a73e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="4a73e-116">-Id</span></span>
<span data-ttu-id="4a73e-117">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4a73e-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4a73e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a73e-118">-Name</span></span>
<span data-ttu-id="4a73e-119">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4a73e-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4a73e-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="4a73e-120">-Pre</span></span>
<span data-ttu-id="4a73e-121">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4a73e-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4a73e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a73e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a73e-123">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4a73e-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="4a73e-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a73e-124">-Confirm</span></span>
<span data-ttu-id="4a73e-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a73e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a73e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a73e-126">-WhatIf</span></span>
<span data-ttu-id="4a73e-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a73e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a73e-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a73e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a73e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a73e-129">CommonParameters</span></span>
<span data-ttu-id="4a73e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a73e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a73e-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a73e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a73e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a73e-132">INPUTS</span></span>

### <span data-ttu-id="4a73e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a73e-133">System.String</span></span>

## <span data-ttu-id="4a73e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a73e-134">OUTPUTS</span></span>

### <span data-ttu-id="4a73e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a73e-135">System.Boolean</span></span>

## <span data-ttu-id="4a73e-136">Note</span><span class="sxs-lookup"><span data-stu-id="4a73e-136">NOTES</span></span>

## <span data-ttu-id="4a73e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a73e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4a73e-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a73e-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a73e-139">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a73e-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a73e-140">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a73e-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4a73e-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4a73e-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


