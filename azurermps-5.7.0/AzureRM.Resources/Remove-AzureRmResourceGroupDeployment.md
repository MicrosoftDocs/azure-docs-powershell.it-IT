---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517995"
---
# <span data-ttu-id="98bca-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="98bca-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="98bca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98bca-102">SYNOPSIS</span></span>
<span data-ttu-id="98bca-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="98bca-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98bca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98bca-104">SYNTAX</span></span>

### <span data-ttu-id="98bca-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98bca-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98bca-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="98bca-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98bca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98bca-107">DESCRIPTION</span></span>
<span data-ttu-id="98bca-108">Il cmdlet **Remove-AzureRmResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="98bca-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="98bca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98bca-109">EXAMPLES</span></span>

## <span data-ttu-id="98bca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98bca-110">PARAMETERS</span></span>

### <span data-ttu-id="98bca-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="98bca-111">-ApiVersion</span></span>
<span data-ttu-id="98bca-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="98bca-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="98bca-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="98bca-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="98bca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bca-114">-DefaultProfile</span></span>
<span data-ttu-id="98bca-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98bca-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98bca-116">-ID</span><span class="sxs-lookup"><span data-stu-id="98bca-116">-Id</span></span>
<span data-ttu-id="98bca-117">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="98bca-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bca-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="98bca-118">-Name</span></span>
<span data-ttu-id="98bca-119">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="98bca-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bca-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="98bca-120">-Pre</span></span>
<span data-ttu-id="98bca-121">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="98bca-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="98bca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98bca-122">-ResourceGroupName</span></span>
<span data-ttu-id="98bca-123">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="98bca-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98bca-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98bca-124">-Confirm</span></span>
<span data-ttu-id="98bca-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98bca-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bca-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98bca-126">-WhatIf</span></span>
<span data-ttu-id="98bca-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98bca-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98bca-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98bca-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bca-129">CommonParameters</span></span>
<span data-ttu-id="98bca-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bca-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98bca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bca-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98bca-132">INPUTS</span></span>

### <span data-ttu-id="98bca-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="98bca-133">None</span></span>
<span data-ttu-id="98bca-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="98bca-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98bca-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98bca-135">OUTPUTS</span></span>

### <span data-ttu-id="98bca-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98bca-136">System.Boolean</span></span>

## <span data-ttu-id="98bca-137">Note</span><span class="sxs-lookup"><span data-stu-id="98bca-137">NOTES</span></span>

## <span data-ttu-id="98bca-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98bca-138">RELATED LINKS</span></span>

[<span data-ttu-id="98bca-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="98bca-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="98bca-140">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="98bca-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="98bca-141">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="98bca-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="98bca-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="98bca-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


