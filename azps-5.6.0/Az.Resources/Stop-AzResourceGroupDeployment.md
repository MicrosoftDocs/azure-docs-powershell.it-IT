---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 9258c15578aaeae5102a5d60b2f18a8a4f179d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967629"
---
# <span data-ttu-id="da02e-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da02e-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="da02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da02e-102">SYNOPSIS</span></span>
<span data-ttu-id="da02e-103">Annulla la distribuzione di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da02e-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="da02e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da02e-104">SYNTAX</span></span>

### <span data-ttu-id="da02e-105">StopByResourceGroupDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da02e-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da02e-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="da02e-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da02e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da02e-107">DESCRIPTION</span></span>
<span data-ttu-id="da02e-108">Il cmdlet **Stop-AzResourceGroupDeployment** annulla una distribuzione del gruppo di risorse Azure avviata ma non completata.</span><span class="sxs-lookup"><span data-stu-id="da02e-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="da02e-109">Per arrestare una distribuzione, la distribuzione deve avere uno stato di provisioning incompleto, ad esempio Provisioning, e non uno stato completato, ad esempio Provisioning effettuato o Non riuscito.</span><span class="sxs-lookup"><span data-stu-id="da02e-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="da02e-110">Una risorsa di Azure è un'entità gestita dall'utente, ad esempio un sito Web, un database o un server di database.</span><span class="sxs-lookup"><span data-stu-id="da02e-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="da02e-111">Un gruppo di risorse è una raccolta di risorse distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="da02e-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="da02e-112">Per distribuire un gruppo di risorse, usare il cmdlet New-AzResourceGroupDeployment risorse.</span><span class="sxs-lookup"><span data-stu-id="da02e-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="da02e-113">Il New-AzResource cmdlet crea una nuova risorsa, ma non attiva un'operazione di distribuzione del gruppo di risorse che questo cmdlet può interrompere.</span><span class="sxs-lookup"><span data-stu-id="da02e-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="da02e-114">Questo cmdlet interrompe solo una distribuzione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="da02e-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="da02e-115">Usare il *parametro Name* per interrompere una distribuzione specifica.</span><span class="sxs-lookup"><span data-stu-id="da02e-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="da02e-116">Se si omette il *parametro Name,* **Stop-AzResourceGroupDeployment** cerca una distribuzione in esecuzione e la interrompe.</span><span class="sxs-lookup"><span data-stu-id="da02e-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="da02e-117">Se il cmdlet trova più distribuzioni in esecuzione, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="da02e-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="da02e-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da02e-118">EXAMPLES</span></span>

### <span data-ttu-id="da02e-119">Esempio 1: Avvio e interruzione della distribuzione di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="da02e-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="da02e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da02e-120">PARAMETERS</span></span>

### <span data-ttu-id="da02e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da02e-121">-DefaultProfile</span></span>
<span data-ttu-id="da02e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="da02e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da02e-123">-Id</span><span class="sxs-lookup"><span data-stu-id="da02e-123">-Id</span></span>
<span data-ttu-id="da02e-124">Specifica l'ID della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="da02e-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="da02e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="da02e-125">-Name</span></span>
<span data-ttu-id="da02e-126">Specifica il nome della distribuzione del gruppo di risorse da interrompere.</span><span class="sxs-lookup"><span data-stu-id="da02e-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="da02e-127">Se non si specifica questo parametro, questo cmdlet cerca una distribuzione in esecuzione nel gruppo di risorse e lo interrompe.</span><span class="sxs-lookup"><span data-stu-id="da02e-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="da02e-128">Se vengono trovate più distribuzioni in esecuzione, il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="da02e-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="da02e-129">Per ottenere il nome della distribuzione, usare il cmdlet Get-AzResourceGroupDeployment distribuzione.</span><span class="sxs-lookup"><span data-stu-id="da02e-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="da02e-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="da02e-130">-Pre</span></span>
<span data-ttu-id="da02e-131">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="da02e-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="da02e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da02e-132">-ResourceGroupName</span></span>
<span data-ttu-id="da02e-133">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da02e-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="da02e-134">Questo cmdlet interrompe la distribuzione del gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="da02e-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da02e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da02e-135">-Confirm</span></span>
<span data-ttu-id="da02e-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da02e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da02e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da02e-137">-WhatIf</span></span>
<span data-ttu-id="da02e-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da02e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da02e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da02e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da02e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da02e-140">CommonParameters</span></span>
<span data-ttu-id="da02e-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da02e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da02e-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da02e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da02e-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="da02e-143">INPUTS</span></span>

### <span data-ttu-id="da02e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="da02e-144">System.String</span></span>

## <span data-ttu-id="da02e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da02e-145">OUTPUTS</span></span>

### <span data-ttu-id="da02e-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da02e-146">System.Boolean</span></span>

## <span data-ttu-id="da02e-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="da02e-147">NOTES</span></span>

## <span data-ttu-id="da02e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da02e-148">RELATED LINKS</span></span>

[<span data-ttu-id="da02e-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da02e-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="da02e-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="da02e-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="da02e-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da02e-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="da02e-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da02e-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="da02e-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da02e-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="da02e-154">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="da02e-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


