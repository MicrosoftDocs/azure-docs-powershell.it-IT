---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519518"
---
# <span data-ttu-id="f7208-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7208-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f7208-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7208-102">SYNOPSIS</span></span>
<span data-ttu-id="f7208-103">Rimuove una distribuzione di un gruppo di risorse e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="f7208-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7208-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7208-104">SYNTAX</span></span>

### <span data-ttu-id="f7208-105">Set di parametri per il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f7208-105">The deployment name parameter set.</span></span> <span data-ttu-id="f7208-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="f7208-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7208-107">Set di parametri ID distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f7208-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7208-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7208-108">DESCRIPTION</span></span>
<span data-ttu-id="f7208-109">Il cmdlet **Remove-AzureRmResourceGroupDeployment** rimuove una distribuzione di un gruppo di risorse Azure e tutte le operazioni associate.</span><span class="sxs-lookup"><span data-stu-id="f7208-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="f7208-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7208-110">EXAMPLES</span></span>

## <span data-ttu-id="f7208-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7208-111">PARAMETERS</span></span>

### <span data-ttu-id="f7208-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f7208-112">-ApiVersion</span></span>
<span data-ttu-id="f7208-113">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7208-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f7208-114">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f7208-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f7208-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f7208-115">-Id</span></span>
<span data-ttu-id="f7208-116">Specifica l'ID della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7208-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7208-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7208-117">-Name</span></span>
<span data-ttu-id="f7208-118">Specifica il nome della distribuzione del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7208-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7208-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="f7208-119">-Pre</span></span>
<span data-ttu-id="f7208-120">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f7208-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f7208-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7208-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7208-122">Specifica il nome del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7208-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7208-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7208-123">-Confirm</span></span>
<span data-ttu-id="f7208-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7208-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7208-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7208-125">-WhatIf</span></span>
<span data-ttu-id="f7208-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7208-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7208-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7208-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7208-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7208-128">-DefaultProfile</span></span>
<span data-ttu-id="f7208-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7208-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7208-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7208-130">CommonParameters</span></span>
<span data-ttu-id="f7208-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7208-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7208-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7208-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7208-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7208-133">INPUTS</span></span>

## <span data-ttu-id="f7208-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7208-134">OUTPUTS</span></span>

### <span data-ttu-id="f7208-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7208-135">System.Boolean</span></span>

## <span data-ttu-id="f7208-136">Note</span><span class="sxs-lookup"><span data-stu-id="f7208-136">NOTES</span></span>

## <span data-ttu-id="f7208-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7208-137">RELATED LINKS</span></span>

[<span data-ttu-id="f7208-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7208-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f7208-139">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7208-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f7208-140">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7208-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f7208-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7208-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


