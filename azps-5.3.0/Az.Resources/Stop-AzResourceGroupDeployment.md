---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382560"
---
# <span data-ttu-id="e599c-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e599c-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e599c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e599c-102">SYNOPSIS</span></span>
<span data-ttu-id="e599c-103">Annulla la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e599c-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="e599c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e599c-104">SYNTAX</span></span>

### <span data-ttu-id="e599c-105">StopByResourceGroupDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e599c-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e599c-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e599c-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e599c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e599c-107">DESCRIPTION</span></span>
<span data-ttu-id="e599c-108">Il cmdlet **Stop-AzResourceGroupDeployment** Annulla una distribuzione di un gruppo di risorse Azure iniziata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="e599c-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="e599c-109">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="e599c-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="e599c-110">Una risorsa Azure è un'entità gestita dall'utente, ad esempio un sito Web, un database o un server di database.</span><span class="sxs-lookup"><span data-stu-id="e599c-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="e599c-111">Un gruppo di risorse è una raccolta di risorse distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="e599c-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="e599c-112">Per distribuire un gruppo di risorse, usare il cmdlet New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e599c-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="e599c-113">Il cmdlet New-AzResource crea una nuova risorsa, ma non attiva un'operazione di distribuzione di un gruppo di risorse che questo cmdlet può arrestare.</span><span class="sxs-lookup"><span data-stu-id="e599c-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="e599c-114">Questo cmdlet arresta una sola distribuzione in uso.</span><span class="sxs-lookup"><span data-stu-id="e599c-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="e599c-115">Usa il parametro *Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="e599c-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="e599c-116">Se si omette il parametro *Name* , **Stop-AzResourceGroupDeployment** cerca una distribuzione in corso e la arresta.</span><span class="sxs-lookup"><span data-stu-id="e599c-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="e599c-117">Se il cmdlet trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="e599c-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="e599c-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e599c-118">EXAMPLES</span></span>

### <span data-ttu-id="e599c-119">Esempio 1: avviare e arrestare una distribuzione di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e599c-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="e599c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e599c-120">PARAMETERS</span></span>

### <span data-ttu-id="e599c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e599c-121">-DefaultProfile</span></span>
<span data-ttu-id="e599c-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e599c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e599c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="e599c-123">-Id</span></span>
<span data-ttu-id="e599c-124">Specifica l'ID della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="e599c-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e599c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e599c-125">-Name</span></span>
<span data-ttu-id="e599c-126">Specifica il nome della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="e599c-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="e599c-127">Se non specifichi questo parametro, questo cmdlet cerca una distribuzione in uso nel gruppo di risorse e la arresta.</span><span class="sxs-lookup"><span data-stu-id="e599c-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="e599c-128">Se trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="e599c-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="e599c-129">Per ottenere il nome della distribuzione, usa il cmdlet Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="e599c-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e599c-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="e599c-130">-Pre</span></span>
<span data-ttu-id="e599c-131">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e599c-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e599c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e599c-132">-ResourceGroupName</span></span>
<span data-ttu-id="e599c-133">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e599c-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e599c-134">Questo cmdlet interrompe la distribuzione del gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="e599c-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e599c-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e599c-135">-Confirm</span></span>
<span data-ttu-id="e599c-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e599c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e599c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e599c-137">-WhatIf</span></span>
<span data-ttu-id="e599c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e599c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e599c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e599c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e599c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e599c-140">CommonParameters</span></span>
<span data-ttu-id="e599c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e599c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e599c-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e599c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e599c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e599c-143">INPUTS</span></span>

### <span data-ttu-id="e599c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e599c-144">System.String</span></span>

## <span data-ttu-id="e599c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e599c-145">OUTPUTS</span></span>

### <span data-ttu-id="e599c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e599c-146">System.Boolean</span></span>

## <span data-ttu-id="e599c-147">Note</span><span class="sxs-lookup"><span data-stu-id="e599c-147">NOTES</span></span>

## <span data-ttu-id="e599c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e599c-148">RELATED LINKS</span></span>

[<span data-ttu-id="e599c-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e599c-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e599c-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e599c-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e599c-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e599c-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e599c-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e599c-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e599c-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e599c-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="e599c-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e599c-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


