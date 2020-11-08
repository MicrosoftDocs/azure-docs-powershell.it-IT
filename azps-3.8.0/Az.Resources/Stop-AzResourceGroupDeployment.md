---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 01f2aa36a063caec233aa8c1600d4a01727a549b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019669"
---
# <span data-ttu-id="53dfa-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53dfa-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="53dfa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="53dfa-103">Annulla la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53dfa-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="53dfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53dfa-104">SYNTAX</span></span>

### <span data-ttu-id="53dfa-105">StopByResourceGroupDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53dfa-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53dfa-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="53dfa-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53dfa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="53dfa-108">Il cmdlet **Stop-AzResourceGroupDeployment** Annulla una distribuzione di un gruppo di risorse Azure iniziata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="53dfa-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="53dfa-109">Per interrompere una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio il provisioning e non uno stato completato, ad esempio provisioning o failed.</span><span class="sxs-lookup"><span data-stu-id="53dfa-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="53dfa-110">Una risorsa Azure è un'entità gestita dall'utente, ad esempio un sito Web, un database o un server di database.</span><span class="sxs-lookup"><span data-stu-id="53dfa-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="53dfa-111">Un gruppo di risorse è una raccolta di risorse distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="53dfa-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="53dfa-112">Per distribuire un gruppo di risorse, usare il cmdlet New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="53dfa-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="53dfa-113">Il cmdlet New-AzResource crea una nuova risorsa, ma non attiva un'operazione di distribuzione di un gruppo di risorse che questo cmdlet può arrestare.</span><span class="sxs-lookup"><span data-stu-id="53dfa-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="53dfa-114">Questo cmdlet arresta una sola distribuzione in uso.</span><span class="sxs-lookup"><span data-stu-id="53dfa-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="53dfa-115">Usa il parametro *Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="53dfa-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="53dfa-116">Se si omette il parametro *Name* , **Stop-AzResourceGroupDeployment** cerca una distribuzione in corso e la arresta.</span><span class="sxs-lookup"><span data-stu-id="53dfa-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="53dfa-117">Se il cmdlet trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="53dfa-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="53dfa-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53dfa-118">EXAMPLES</span></span>

### <span data-ttu-id="53dfa-119">Esempio 1: avviare e arrestare una distribuzione di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="53dfa-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="53dfa-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53dfa-120">PARAMETERS</span></span>

### <span data-ttu-id="53dfa-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53dfa-121">-ApiVersion</span></span>
<span data-ttu-id="53dfa-122">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="53dfa-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="53dfa-123">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="53dfa-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="53dfa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53dfa-124">-DefaultProfile</span></span>
<span data-ttu-id="53dfa-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="53dfa-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53dfa-126">-ID</span><span class="sxs-lookup"><span data-stu-id="53dfa-126">-Id</span></span>
<span data-ttu-id="53dfa-127">Specifica l'ID della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="53dfa-127">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="53dfa-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="53dfa-128">-Name</span></span>
<span data-ttu-id="53dfa-129">Specifica il nome della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="53dfa-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="53dfa-130">Se non specifichi questo parametro, questo cmdlet cerca una distribuzione in uso nel gruppo di risorse e la arresta.</span><span class="sxs-lookup"><span data-stu-id="53dfa-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="53dfa-131">Se trova più di una distribuzione in uso, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="53dfa-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="53dfa-132">Per ottenere il nome della distribuzione, usa il cmdlet Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="53dfa-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="53dfa-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="53dfa-133">-Pre</span></span>
<span data-ttu-id="53dfa-134">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="53dfa-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53dfa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53dfa-135">-ResourceGroupName</span></span>
<span data-ttu-id="53dfa-136">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53dfa-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="53dfa-137">Questo cmdlet interrompe la distribuzione del gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="53dfa-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53dfa-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53dfa-138">-Confirm</span></span>
<span data-ttu-id="53dfa-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53dfa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53dfa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53dfa-140">-WhatIf</span></span>
<span data-ttu-id="53dfa-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53dfa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53dfa-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53dfa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53dfa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53dfa-143">CommonParameters</span></span>
<span data-ttu-id="53dfa-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53dfa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53dfa-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53dfa-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53dfa-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53dfa-146">INPUTS</span></span>

### <span data-ttu-id="53dfa-147">System. String</span><span class="sxs-lookup"><span data-stu-id="53dfa-147">System.String</span></span>

## <span data-ttu-id="53dfa-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53dfa-148">OUTPUTS</span></span>

### <span data-ttu-id="53dfa-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53dfa-149">System.Boolean</span></span>

## <span data-ttu-id="53dfa-150">Note</span><span class="sxs-lookup"><span data-stu-id="53dfa-150">NOTES</span></span>

## <span data-ttu-id="53dfa-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53dfa-151">RELATED LINKS</span></span>

[<span data-ttu-id="53dfa-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53dfa-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="53dfa-153">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="53dfa-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="53dfa-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53dfa-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="53dfa-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53dfa-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="53dfa-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53dfa-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="53dfa-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53dfa-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


