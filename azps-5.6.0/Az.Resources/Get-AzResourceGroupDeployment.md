---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988930"
---
# <span data-ttu-id="ea3fc-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ea3fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3fc-103">Ottiene le distribuzioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="ea3fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea3fc-104">SYNTAX</span></span>

### <span data-ttu-id="ea3fc-105">GetByResourceGroupDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea3fc-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea3fc-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ea3fc-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea3fc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea3fc-107">DESCRIPTION</span></span>
<span data-ttu-id="ea3fc-108">Il cmdlet **Get-AzResourceGroupDeployment** ottiene le distribuzioni in un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="ea3fc-109">Specificare il *parametro Name* o *Id* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ea3fc-110">Per impostazione predefinita, **Get-AzResourceGroupDeployment** ottiene tutte le distribuzioni per un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="ea3fc-111">Una risorsa di Azure è un'entità azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="ea3fc-112">Un gruppo di risorse di Azure è una raccolta di risorse di Azure distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="ea3fc-113">Una distribuzione è l'operazione che rende disponibili per l'uso le risorse nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="ea3fc-114">Per altre informazioni sulle risorse di Azure e sui gruppi di risorse di Azure, vedere il cmdlet New-AzResourceGroup Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ea3fc-115">È possibile usare questo cmdlet per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="ea3fc-116">Per il debug, usare questo cmdlet con Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="ea3fc-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea3fc-117">EXAMPLES</span></span>

### <span data-ttu-id="ea3fc-118">Esempio 1: Ottenere tutte le distribuzioni per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ea3fc-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="ea3fc-119">Questo comando recupera tutte le distribuzioni per il gruppo di risorse ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="ea3fc-120">L'output mostra una distribuzione per un blog di WordPress che usava un modello di raccolta.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="ea3fc-121">Esempio 2: Ottenere una distribuzione in base al nome</span><span class="sxs-lookup"><span data-stu-id="ea3fc-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="ea3fc-122">Questo comando ottiene la distribuzione DeployWebsite01 del gruppo di risorse ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="ea3fc-123">È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzResourceGroup** **o New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="ea3fc-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ea3fc-124">Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ea3fc-125">Esempio 3: Ottenere le distribuzioni di tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ea3fc-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="ea3fc-126">Questo comando recupera tutti i gruppi di risorse nell'abbonamento usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ea3fc-127">Il comando passa i gruppi di risorse al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea3fc-128">Il cmdlet corrente ottiene tutte le distribuzioni di tutti i gruppi di risorse nella sottoscrizione e passa i risultati al cmdlet Format-Table per visualizzare i valori delle proprietà **ResourceGroupName,** **DeploymentName** e **ProvisioningState.**</span><span class="sxs-lookup"><span data-stu-id="ea3fc-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="ea3fc-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea3fc-129">PARAMETERS</span></span>

### <span data-ttu-id="ea3fc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3fc-130">-DefaultProfile</span></span>
<span data-ttu-id="ea3fc-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ea3fc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea3fc-132">-Id</span><span class="sxs-lookup"><span data-stu-id="ea3fc-132">-Id</span></span>
<span data-ttu-id="ea3fc-133">Specifica l'ID della distribuzione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3fc-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ea3fc-134">-Name</span></span>
<span data-ttu-id="ea3fc-135">Specifica il nome della distribuzione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="ea3fc-136">Non sono consentiti caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea3fc-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea3fc-137">-Pre</span></span>
<span data-ttu-id="ea3fc-138">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ea3fc-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea3fc-139">-ResourceGroupName</span></span>
<span data-ttu-id="ea3fc-140">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ea3fc-141">Il cmdlet ottiene le distribuzioni per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="ea3fc-142">Non sono consentiti caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="ea3fc-143">Questo parametro è obbligatorio ed è possibile specificare un solo gruppo di risorse per ogni comando.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea3fc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3fc-144">CommonParameters</span></span>
<span data-ttu-id="ea3fc-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3fc-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea3fc-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3fc-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea3fc-147">INPUTS</span></span>

### <span data-ttu-id="ea3fc-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ea3fc-148">System.String</span></span>

## <span data-ttu-id="ea3fc-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea3fc-149">OUTPUTS</span></span>

### <span data-ttu-id="ea3fc-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="ea3fc-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea3fc-151">NOTES</span></span>

## <span data-ttu-id="ea3fc-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea3fc-152">RELATED LINKS</span></span>

[<span data-ttu-id="ea3fc-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea3fc-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="ea3fc-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea3fc-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="ea3fc-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ea3fc-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="ea3fc-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ea3fc-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea3fc-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


