---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862337"
---
# <span data-ttu-id="334dd-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="334dd-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="334dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="334dd-102">SYNOPSIS</span></span>
<span data-ttu-id="334dd-103">Modifica un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-103">Modifies a resource group.</span></span>

## <span data-ttu-id="334dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="334dd-104">SYNTAX</span></span>

### <span data-ttu-id="334dd-105">SetByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="334dd-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="334dd-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="334dd-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="334dd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="334dd-107">DESCRIPTION</span></span>
<span data-ttu-id="334dd-108">Il cmdlet **set-AzResourceGroup** modifica le proprietà di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="334dd-109">Puoi usare questo cmdlet per aggiungere, modificare o eliminare i tag Azure applicati a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="334dd-110">Specifica il parametro *Name* per identificare il gruppo di risorse e il parametro *tag* per modificare i tag.</span><span class="sxs-lookup"><span data-stu-id="334dd-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="334dd-111">Non è possibile usare questo cmdlet per cambiare il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="334dd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="334dd-112">EXAMPLES</span></span>

### <span data-ttu-id="334dd-113">Esempio 1: applicare un contrassegno a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="334dd-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="334dd-114">Questo comando applica un tag Department con un valore di un gruppo di risorse che non contiene tag esistenti.</span><span class="sxs-lookup"><span data-stu-id="334dd-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="334dd-115">Esempio 2: aggiungere tag a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="334dd-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="334dd-116">Questo esempio aggiunge un tag di stato con un valore approvato e un tag FY2016 a un gruppo di risorse con tag esistenti.</span><span class="sxs-lookup"><span data-stu-id="334dd-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="334dd-117">Poiché i tag specificati sostituiscono i tag esistenti, è necessario includere i tag esistenti nella nuova raccolta di tag oppure perderli.</span><span class="sxs-lookup"><span data-stu-id="334dd-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="334dd-118">Il primo comando ottiene il gruppo di risorse ContosoRG e usa il metodo dot per ottenere il valore della proprietà Tags.</span><span class="sxs-lookup"><span data-stu-id="334dd-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="334dd-119">Il comando Archivia i tag nella variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="334dd-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="334dd-120">Il secondo comando ottiene i contrassegni nella variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="334dd-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="334dd-121">Il terzo comando usa l'operatore di assegnazione + = per aggiungere i tag status e FY2016 alla matrice di tag nella variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="334dd-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="334dd-122">Il quarto comando usa il parametro *tag* di **set-AzResourceGroup** per applicare i tag nella variabile $Tags al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="334dd-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="334dd-123">Il quinto comando consente di ottenere tutti i tag applicati al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="334dd-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="334dd-124">L'output mostra che il gruppo di risorse ha il tag Department e i due nuovi tag, status e FY2015.</span><span class="sxs-lookup"><span data-stu-id="334dd-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="334dd-125">Esempio 3: eliminare tutti i tag per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="334dd-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="334dd-126">Questo comando specifica il parametro *tag* con un valore di tabella hash vuoto per eliminare tutti i tag dal gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="334dd-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="334dd-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="334dd-127">PARAMETERS</span></span>

### <span data-ttu-id="334dd-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="334dd-128">-ApiVersion</span></span>
<span data-ttu-id="334dd-129">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="334dd-130">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="334dd-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="334dd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="334dd-131">-DefaultProfile</span></span>
<span data-ttu-id="334dd-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="334dd-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="334dd-133">-ID</span><span class="sxs-lookup"><span data-stu-id="334dd-133">-Id</span></span>
<span data-ttu-id="334dd-134">Specifica l'ID del gruppo di risorse da modificare.</span><span class="sxs-lookup"><span data-stu-id="334dd-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="334dd-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="334dd-135">-Name</span></span>
<span data-ttu-id="334dd-136">Specifica il nome del gruppo di risorse da modificare.</span><span class="sxs-lookup"><span data-stu-id="334dd-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334dd-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="334dd-137">-Pre</span></span>
<span data-ttu-id="334dd-138">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="334dd-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="334dd-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="334dd-139">-Tag</span></span>
<span data-ttu-id="334dd-140">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="334dd-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="334dd-141">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"} un tag è una coppia nome-valore che è possibile creare e applicare alle risorse e ai gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="334dd-142">Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *tag* di Get-AzResource e Get-AzResourceGroup per cercare risorse e gruppi in base al nome del tag o al nome e al valore.</span><span class="sxs-lookup"><span data-stu-id="334dd-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="334dd-143">È possibile usare i tag per suddividere in categorie le risorse, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="334dd-144">Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="334dd-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="334dd-145">Per eliminare un contrassegno, immettere una tabella hash con tutti i tag attualmente applicati al gruppo di risorse, da **Get-AzResourceGroup** , ad eccezione del contrassegno che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="334dd-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="334dd-146">Per eliminare tutti i tag da un gruppo di risorse, specificare una tabella hash vuota: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="334dd-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="334dd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334dd-147">CommonParameters</span></span>
<span data-ttu-id="334dd-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334dd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334dd-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334dd-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334dd-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="334dd-150">INPUTS</span></span>

### <span data-ttu-id="334dd-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="334dd-151">None</span></span>

## <span data-ttu-id="334dd-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="334dd-152">OUTPUTS</span></span>

### <span data-ttu-id="334dd-153">Microsoft. Azure. Commands. resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="334dd-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="334dd-154">Note</span><span class="sxs-lookup"><span data-stu-id="334dd-154">NOTES</span></span>

## <span data-ttu-id="334dd-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="334dd-155">RELATED LINKS</span></span>

[<span data-ttu-id="334dd-156">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="334dd-156">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="334dd-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="334dd-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="334dd-158">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="334dd-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="334dd-159">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="334dd-159">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
