---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516087"
---
# <span data-ttu-id="66cbb-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66cbb-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="66cbb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="66cbb-103">Crea un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="66cbb-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66cbb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66cbb-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66cbb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="66cbb-106">Il cmdlet **New-AzureRmResourceGroup** crea un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="66cbb-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="66cbb-107">È possibile creare un gruppo di risorse usando solo un nome e un percorso e quindi usare il cmdlet New-AzureRmResource per creare risorse da aggiungere al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="66cbb-108">Per aggiungere una distribuzione a un gruppo di risorse esistente, usare il cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="66cbb-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="66cbb-109">Per aggiungere una risorsa a un gruppo di risorse esistente, usare il cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="66cbb-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="66cbb-110">Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web.</span><span class="sxs-lookup"><span data-stu-id="66cbb-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="66cbb-111">Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità.</span><span class="sxs-lookup"><span data-stu-id="66cbb-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="66cbb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66cbb-112">EXAMPLES</span></span>

### <span data-ttu-id="66cbb-113">Esempio 1: creare un gruppo di risorse vuoto</span><span class="sxs-lookup"><span data-stu-id="66cbb-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="66cbb-114">Questo comando crea un gruppo di risorse che non contiene risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="66cbb-115">È possibile usare i cmdlet **New-AzureRmResource** o **New-AzureRmResourceGroupDeployment** per aggiungere risorse e distribuzioni a questo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="66cbb-116">Esempio 2: creare un gruppo di risorse con tag</span><span class="sxs-lookup"><span data-stu-id="66cbb-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="66cbb-117">Questo comando crea un gruppo di risorse vuoto.</span><span class="sxs-lookup"><span data-stu-id="66cbb-117">This command creates an empty resource group.</span></span> <span data-ttu-id="66cbb-118">Questo comando è uguale al comando dell'esempio 1, ad eccezione del fatto che assegna i tag al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="66cbb-119">Il primo tag, denominato Empty, può essere usato per identificare i gruppi di risorse che non hanno risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="66cbb-120">Il secondo tag è denominato reparto e ha un valore di marketing.</span><span class="sxs-lookup"><span data-stu-id="66cbb-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="66cbb-121">Puoi usare un tag come questo per categorizzare i gruppi di risorse per l'amministrazione o il budget.</span><span class="sxs-lookup"><span data-stu-id="66cbb-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="66cbb-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66cbb-122">PARAMETERS</span></span>

### <span data-ttu-id="66cbb-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="66cbb-123">-ApiVersion</span></span>
<span data-ttu-id="66cbb-124">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="66cbb-125">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="66cbb-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="66cbb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="66cbb-126">-Force</span></span>
<span data-ttu-id="66cbb-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="66cbb-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66cbb-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="66cbb-128">-Location</span></span>
<span data-ttu-id="66cbb-129">Specifica la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="66cbb-130">Specificare una posizione nel centro dati di Azure, ad esempio ovest degli Stati Uniti o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="66cbb-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="66cbb-131">È possibile inserire un gruppo di risorse in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="66cbb-131">You can place a resource group in any location.</span></span> <span data-ttu-id="66cbb-132">Il gruppo risorse non deve trovarsi nella stessa posizione dell'abbonamento a Azure o nella stessa posizione delle proprie risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="66cbb-133">Per determinare quale posizione supporta ogni tipo di risorsa, usare il cmdlet Get-AzureRmResourceProvider con il parametro *ProviderNamespace* .</span><span class="sxs-lookup"><span data-stu-id="66cbb-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66cbb-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="66cbb-134">-Name</span></span>
<span data-ttu-id="66cbb-135">Specifica un nome per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="66cbb-136">Il nome della risorsa deve essere univoco nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="66cbb-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="66cbb-137">Se un gruppo di risorse con quel nome esiste già, il comando richiede la conferma prima di sostituire il gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="66cbb-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66cbb-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="66cbb-138">-Pre</span></span>
<span data-ttu-id="66cbb-139">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="66cbb-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66cbb-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="66cbb-140">-Tag</span></span>
<span data-ttu-id="66cbb-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="66cbb-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66cbb-142">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="66cbb-142">For example:</span></span>

<span data-ttu-id="66cbb-143">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="66cbb-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="66cbb-144">Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="66cbb-145">Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *tag* di Get-AzureRmResource e Get-AzureRmResourceGroup per cercare risorse e gruppi per nome di tag o per nome e valore.</span><span class="sxs-lookup"><span data-stu-id="66cbb-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="66cbb-146">È possibile usare i tag per suddividere in categorie le risorse, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="66cbb-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="66cbb-147">Per ottenere i tag predefiniti, usare il cmdlet Get-AzureRMTag.</span><span class="sxs-lookup"><span data-stu-id="66cbb-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="66cbb-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66cbb-148">-Confirm</span></span>
<span data-ttu-id="66cbb-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66cbb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66cbb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66cbb-150">-WhatIf</span></span>
<span data-ttu-id="66cbb-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66cbb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66cbb-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66cbb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66cbb-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66cbb-153">-DefaultProfile</span></span>
<span data-ttu-id="66cbb-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66cbb-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66cbb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66cbb-155">CommonParameters</span></span>
<span data-ttu-id="66cbb-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66cbb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66cbb-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66cbb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66cbb-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66cbb-158">INPUTS</span></span>

### <span data-ttu-id="66cbb-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="66cbb-159">None</span></span>

## <span data-ttu-id="66cbb-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66cbb-160">OUTPUTS</span></span>

### <span data-ttu-id="66cbb-161">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66cbb-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="66cbb-162">Note</span><span class="sxs-lookup"><span data-stu-id="66cbb-162">NOTES</span></span>

## <span data-ttu-id="66cbb-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66cbb-163">RELATED LINKS</span></span>

[<span data-ttu-id="66cbb-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="66cbb-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="66cbb-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66cbb-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="66cbb-166">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="66cbb-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="66cbb-167">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="66cbb-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="66cbb-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66cbb-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="66cbb-169">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66cbb-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
