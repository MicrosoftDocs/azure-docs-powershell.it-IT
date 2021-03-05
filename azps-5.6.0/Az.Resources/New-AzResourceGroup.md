---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008606"
---
# <span data-ttu-id="f9518-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9518-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="f9518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9518-102">SYNOPSIS</span></span>
<span data-ttu-id="f9518-103">Crea un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9518-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="f9518-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9518-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9518-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9518-105">DESCRIPTION</span></span>
<span data-ttu-id="f9518-106">Il cmdlet **New-AzResourceGroup** crea un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9518-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="f9518-107">È possibile creare un gruppo di risorse usando solo un nome e un percorso e quindi usare il cmdlet New-AzResource per creare risorse da aggiungere al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="f9518-108">Per aggiungere una distribuzione a un gruppo di risorse esistente, usare il cmdlet New-AzResourceGroupDeployment distribuzione.</span><span class="sxs-lookup"><span data-stu-id="f9518-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="f9518-109">Per aggiungere una risorsa a un gruppo di risorse esistente, usare il cmdlet **New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="f9518-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="f9518-110">Una risorsa di Azure è un'entità di Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.</span><span class="sxs-lookup"><span data-stu-id="f9518-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="f9518-111">Un gruppo di risorse di Azure è una raccolta di risorse di Azure distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="f9518-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="f9518-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9518-112">EXAMPLES</span></span>

### <span data-ttu-id="f9518-113">Esempio 1: Creare un gruppo di risorse vuoto</span><span class="sxs-lookup"><span data-stu-id="f9518-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="f9518-114">Questo comando crea un gruppo di risorse senza risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="f9518-115">È possibile usare i cmdlet **New-AzResource** o **New-AzResourceGroupDeployment** per aggiungere risorse e distribuzioni a questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="f9518-116">Esempio 2: Creare un gruppo di risorse vuoto usando parametri posizionali</span><span class="sxs-lookup"><span data-stu-id="f9518-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="f9518-117">Questo comando crea un gruppo di risorse senza risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="f9518-118">Esempio 3: Creare un gruppo di risorse con contrassegni</span><span class="sxs-lookup"><span data-stu-id="f9518-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="f9518-119">Questo comando crea un gruppo di risorse vuoto.</span><span class="sxs-lookup"><span data-stu-id="f9518-119">This command creates an empty resource group.</span></span> <span data-ttu-id="f9518-120">Questo comando è uguale a quello dell'esempio 1, con la differenza che assegna tag al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="f9518-121">Il primo tag, denominato Vuoto, può essere usato per identificare i gruppi di risorse che non hanno risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="f9518-122">Il secondo tag si chiama Department e ha valore Marketing.</span><span class="sxs-lookup"><span data-stu-id="f9518-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="f9518-123">È possibile usare un tag come questo per categorizzare i gruppi di risorse per l'amministrazione o la pianificazione del budget.</span><span class="sxs-lookup"><span data-stu-id="f9518-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="f9518-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9518-124">PARAMETERS</span></span>

### <span data-ttu-id="f9518-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f9518-125">-ApiVersion</span></span>
<span data-ttu-id="f9518-126">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f9518-127">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="f9518-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f9518-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9518-128">-DefaultProfile</span></span>
<span data-ttu-id="f9518-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f9518-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9518-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f9518-130">-Force</span></span>
<span data-ttu-id="f9518-131">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="f9518-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9518-132">-Location</span><span class="sxs-lookup"><span data-stu-id="f9518-132">-Location</span></span>
<span data-ttu-id="f9518-133">Specifica la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="f9518-134">Specificare la posizione di un data center di Azure, ad esempio Stati Uniti occidentali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="f9518-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="f9518-135">È possibile inserire un gruppo di risorse in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="f9518-135">You can place a resource group in any location.</span></span> <span data-ttu-id="f9518-136">Il gruppo di risorse non deve essere nella stessa posizione della sottoscrizione di Azure o nella stessa posizione delle relative risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="f9518-137">Per determinare quale posizione supporta ogni tipo di risorsa, usare il cmdlet Get-AzResourceProvider con il *parametro ProviderNtassi.*</span><span class="sxs-lookup"><span data-stu-id="f9518-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9518-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f9518-138">-Name</span></span>
<span data-ttu-id="f9518-139">Specifica un nome per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="f9518-140">Il nome della risorsa deve essere univoco nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f9518-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="f9518-141">Se esiste già un gruppo di risorse con questo nome, il comando richiede conferma prima di sostituire il gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="f9518-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9518-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="f9518-142">-Pre</span></span>
<span data-ttu-id="f9518-143">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f9518-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f9518-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9518-144">-Tag</span></span>
<span data-ttu-id="f9518-145">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f9518-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9518-146">Ad esempio: @{key0="value0";key1=$null;key2="value2"} Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="f9518-147">Dopo aver assegnato tag a risorse e gruppi, è possibile usare il parametro *Tag* di Get-AzResource e Get-AzResourceGroup per cercare risorse e gruppi in base al nome del tag o al nome e al valore.</span><span class="sxs-lookup"><span data-stu-id="f9518-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="f9518-148">È possibile usare i contrassegni per categorizzare le risorse, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="f9518-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="f9518-149">Per ottenere i tag predefiniti, usare il cmdlet Get-AzTag predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9518-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9518-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9518-150">-Confirm</span></span>
<span data-ttu-id="f9518-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9518-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9518-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9518-152">-WhatIf</span></span>
<span data-ttu-id="f9518-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9518-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9518-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9518-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9518-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9518-155">CommonParameters</span></span>
<span data-ttu-id="f9518-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9518-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9518-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9518-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9518-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9518-158">INPUTS</span></span>

### <span data-ttu-id="f9518-159">System.String</span><span class="sxs-lookup"><span data-stu-id="f9518-159">System.String</span></span>

### <span data-ttu-id="f9518-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9518-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9518-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9518-161">OUTPUTS</span></span>

### <span data-ttu-id="f9518-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9518-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="f9518-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9518-163">NOTES</span></span>

## <span data-ttu-id="f9518-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9518-164">RELATED LINKS</span></span>

[<span data-ttu-id="f9518-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f9518-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="f9518-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9518-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="f9518-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="f9518-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="f9518-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f9518-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f9518-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9518-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="f9518-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9518-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
