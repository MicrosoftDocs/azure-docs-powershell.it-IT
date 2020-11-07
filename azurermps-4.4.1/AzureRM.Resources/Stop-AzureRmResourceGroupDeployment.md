---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688239"
---
# <span data-ttu-id="b72c1-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b72c1-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b72c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b72c1-102">SYNOPSIS</span></span>
<span data-ttu-id="b72c1-103">Annulla la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b72c1-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b72c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b72c1-104">SYNTAX</span></span>

### <span data-ttu-id="b72c1-105">Set di parametri per il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b72c1-105">The deployment name parameter set.</span></span> <span data-ttu-id="b72c1-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="b72c1-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b72c1-107">Set di parametri ID distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b72c1-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b72c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b72c1-108">DESCRIPTION</span></span>
<span data-ttu-id="b72c1-109">Il cmdlet **Stop-AzureRmResourceGroupDeployment** Annulla una distribuzione di un gruppo di risorse Azure iniziata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="b72c1-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="b72c1-110">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="b72c1-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b72c1-111">Una risorsa Azure è un'entità gestita dall'utente, ad esempio un sito Web, un database o un server di database.</span><span class="sxs-lookup"><span data-stu-id="b72c1-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="b72c1-112">Un gruppo di risorse è una raccolta di risorse distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="b72c1-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="b72c1-113">Per distribuire un gruppo di risorse, usare il cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b72c1-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="b72c1-114">Il cmdlet New-AzureRmResource crea una nuova risorsa, ma non attiva un'operazione di distribuzione di un gruppo di risorse che questo cmdlet può arrestare.</span><span class="sxs-lookup"><span data-stu-id="b72c1-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="b72c1-115">Questo cmdlet arresta una sola distribuzione in uso.</span><span class="sxs-lookup"><span data-stu-id="b72c1-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="b72c1-116">Usa il parametro *Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="b72c1-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="b72c1-117">Se si omette il parametro *Name* , **Stop-AzureRmResourceGroupDeployment** cerca una distribuzione in corso e la arresta.</span><span class="sxs-lookup"><span data-stu-id="b72c1-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="b72c1-118">Se il cmdlet trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="b72c1-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="b72c1-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b72c1-119">EXAMPLES</span></span>

## <span data-ttu-id="b72c1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b72c1-120">PARAMETERS</span></span>

### <span data-ttu-id="b72c1-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b72c1-121">-ApiVersion</span></span>
<span data-ttu-id="b72c1-122">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b72c1-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b72c1-123">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b72c1-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b72c1-124">-ID</span><span class="sxs-lookup"><span data-stu-id="b72c1-124">-Id</span></span>
<span data-ttu-id="b72c1-125">Specifica l'ID della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="b72c1-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="b72c1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b72c1-126">-Name</span></span>
<span data-ttu-id="b72c1-127">Specifica il nome della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="b72c1-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="b72c1-128">Se non specifichi questo parametro, questo cmdlet cerca una distribuzione in uso nel gruppo di risorse e la arresta.</span><span class="sxs-lookup"><span data-stu-id="b72c1-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="b72c1-129">Se trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="b72c1-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="b72c1-130">Per ottenere il nome della distribuzione, usa il cmdlet Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b72c1-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b72c1-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b72c1-131">-Pre</span></span>
<span data-ttu-id="b72c1-132">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b72c1-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b72c1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b72c1-133">-ResourceGroupName</span></span>
<span data-ttu-id="b72c1-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b72c1-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b72c1-135">Questo cmdlet interrompe la distribuzione del gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b72c1-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b72c1-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b72c1-136">-Confirm</span></span>
<span data-ttu-id="b72c1-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b72c1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b72c1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b72c1-138">-WhatIf</span></span>
<span data-ttu-id="b72c1-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b72c1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b72c1-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b72c1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b72c1-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b72c1-141">-DefaultProfile</span></span>
<span data-ttu-id="b72c1-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b72c1-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b72c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b72c1-143">CommonParameters</span></span>
<span data-ttu-id="b72c1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b72c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b72c1-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b72c1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b72c1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b72c1-146">INPUTS</span></span>

### <span data-ttu-id="b72c1-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b72c1-147">None</span></span>

## <span data-ttu-id="b72c1-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b72c1-148">OUTPUTS</span></span>

### <span data-ttu-id="b72c1-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="b72c1-149">Boolean</span></span>

## <span data-ttu-id="b72c1-150">Note</span><span class="sxs-lookup"><span data-stu-id="b72c1-150">NOTES</span></span>

## <span data-ttu-id="b72c1-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b72c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="b72c1-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b72c1-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b72c1-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b72c1-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b72c1-154">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b72c1-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="b72c1-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b72c1-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b72c1-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b72c1-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b72c1-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b72c1-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


