---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 2703a5f32142ddd8d5754c89924360564b45d0f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862573"
---
# <span data-ttu-id="325a4-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="325a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="325a4-102">SYNOPSIS</span></span>
<span data-ttu-id="325a4-103">Ottiene le distribuzioni in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="325a4-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="325a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="325a4-104">SYNTAX</span></span>

### <span data-ttu-id="325a4-105">GetByResourceGroupDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="325a4-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="325a4-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="325a4-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="325a4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="325a4-107">DESCRIPTION</span></span>
<span data-ttu-id="325a4-108">Il cmdlet **Get-AzResourceGroupDeployment** ottiene le distribuzioni in un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="325a4-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="325a4-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="325a4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="325a4-110">Per impostazione predefinita, **Get-AzResourceGroupDeployment** ottiene tutte le distribuzioni per un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="325a4-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="325a4-111">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.</span><span class="sxs-lookup"><span data-stu-id="325a4-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="325a4-112">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="325a4-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="325a4-113">Una distribuzione è l'operazione che rende disponibili le risorse del gruppo risorse per l'uso.</span><span class="sxs-lookup"><span data-stu-id="325a4-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="325a4-114">Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="325a4-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="325a4-115">Puoi usare questo cmdlet per il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="325a4-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="325a4-116">Per il debug, usa questo cmdlet con il cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="325a4-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="325a4-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="325a4-117">EXAMPLES</span></span>

### <span data-ttu-id="325a4-118">Esempio 1: ottenere tutte le distribuzioni per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="325a4-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="325a4-119">Questo comando consente di ottenere tutte le distribuzioni per il gruppo di risorse ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="325a4-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="325a4-120">L'output Mostra una distribuzione per un Blog di WordPress che ha usato un modello di raccolta.</span><span class="sxs-lookup"><span data-stu-id="325a4-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="325a4-121">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="325a4-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="325a4-122">Questo comando consente di ottenere la distribuzione DeployWebsite01 del gruppo di risorse ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="325a4-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="325a4-123">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzResourceGroup** o **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="325a4-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="325a4-124">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="325a4-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="325a4-125">Esempio 3: ottenere le distribuzioni di tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="325a4-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="325a4-126">Questo comando consente di ottenere tutti i gruppi di risorse nell'abbonamento usando il cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="325a4-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="325a4-127">Il comando passa i gruppi di risorse al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="325a4-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="325a4-128">Il cmdlet corrente ottiene tutte le distribuzioni di tutti i gruppi di risorse nell'abbonamento e passa i risultati al cmdlet Format-Table per visualizzare i valori delle proprietà **ResourceGroupName** , **DeploymentName** e **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="325a4-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="325a4-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="325a4-129">PARAMETERS</span></span>

### <span data-ttu-id="325a4-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="325a4-130">-ApiVersion</span></span>
<span data-ttu-id="325a4-131">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="325a4-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="325a4-132">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="325a4-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="325a4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325a4-133">-DefaultProfile</span></span>
<span data-ttu-id="325a4-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="325a4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325a4-135">-ID</span><span class="sxs-lookup"><span data-stu-id="325a4-135">-Id</span></span>
<span data-ttu-id="325a4-136">Specifica l'ID della distribuzione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="325a4-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="325a4-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="325a4-137">-Name</span></span>
<span data-ttu-id="325a4-138">Specifica il nome della distribuzione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="325a4-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="325a4-139">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="325a4-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="325a4-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="325a4-140">-Pre</span></span>
<span data-ttu-id="325a4-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="325a4-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="325a4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325a4-142">-ResourceGroupName</span></span>
<span data-ttu-id="325a4-143">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="325a4-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="325a4-144">Il cmdlet ottiene le distribuzioni per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="325a4-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="325a4-145">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="325a4-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="325a4-146">Questo parametro è obbligatorio ed è possibile specificare un solo gruppo di risorse in ogni comando.</span><span class="sxs-lookup"><span data-stu-id="325a4-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="325a4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325a4-147">CommonParameters</span></span>
<span data-ttu-id="325a4-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325a4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325a4-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325a4-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325a4-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="325a4-150">INPUTS</span></span>

### <span data-ttu-id="325a4-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="325a4-151">None</span></span>

## <span data-ttu-id="325a4-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="325a4-152">OUTPUTS</span></span>

### <span data-ttu-id="325a4-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="325a4-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="325a4-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="325a4-155">Note</span><span class="sxs-lookup"><span data-stu-id="325a4-155">NOTES</span></span>

## <span data-ttu-id="325a4-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="325a4-156">RELATED LINKS</span></span>

[<span data-ttu-id="325a4-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="325a4-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="325a4-158">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="325a4-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="325a4-159">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-159">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="325a4-160">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-160">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="325a4-161">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-161">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="325a4-162">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="325a4-162">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


