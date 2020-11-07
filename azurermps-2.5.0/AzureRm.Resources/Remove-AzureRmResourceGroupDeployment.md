---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866953"
---
# <span data-ttu-id="88835-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88835-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="88835-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88835-102">SYNOPSIS</span></span>
<span data-ttu-id="88835-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="88835-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88835-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88835-104">SYNTAX</span></span>

### <span data-ttu-id="88835-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88835-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88835-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="88835-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88835-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88835-107">DESCRIPTION</span></span>
<span data-ttu-id="88835-108">Il cmdlet **Remove-AzureRmResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="88835-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="88835-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88835-109">EXAMPLES</span></span>

## <span data-ttu-id="88835-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88835-110">PARAMETERS</span></span>

### <span data-ttu-id="88835-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88835-111">-ApiVersion</span></span>
<span data-ttu-id="88835-112">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="88835-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="88835-113">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="88835-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="88835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88835-114">-DefaultProfile</span></span>
<span data-ttu-id="88835-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88835-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88835-116">-ID</span><span class="sxs-lookup"><span data-stu-id="88835-116">-Id</span></span>
<span data-ttu-id="88835-117">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88835-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="88835-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="88835-118">-Name</span></span>
<span data-ttu-id="88835-119">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88835-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88835-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="88835-120">-Pre</span></span>
<span data-ttu-id="88835-121">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="88835-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88835-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88835-122">-ResourceGroupName</span></span>
<span data-ttu-id="88835-123">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88835-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88835-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88835-124">-Confirm</span></span>
<span data-ttu-id="88835-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88835-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88835-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88835-126">-WhatIf</span></span>
<span data-ttu-id="88835-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88835-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88835-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88835-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88835-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88835-129">CommonParameters</span></span>
<span data-ttu-id="88835-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88835-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88835-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88835-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88835-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88835-132">INPUTS</span></span>

### <span data-ttu-id="88835-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="88835-133">None</span></span>

## <span data-ttu-id="88835-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88835-134">OUTPUTS</span></span>

## <span data-ttu-id="88835-135">Note</span><span class="sxs-lookup"><span data-stu-id="88835-135">NOTES</span></span>

## <span data-ttu-id="88835-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88835-136">RELATED LINKS</span></span>

[<span data-ttu-id="88835-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88835-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="88835-138">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88835-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="88835-139">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88835-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="88835-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88835-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


