---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520405"
---
# <span data-ttu-id="5d035-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d035-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="5d035-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d035-102">SYNOPSIS</span></span>
<span data-ttu-id="5d035-103">Ottiene i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d035-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d035-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d035-104">SYNTAX</span></span>

### <span data-ttu-id="5d035-105">GetByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d035-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d035-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="5d035-106">GetByResourceGroupId</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d035-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d035-107">DESCRIPTION</span></span>
<span data-ttu-id="5d035-108">Il cmdlet **Get-AzureRmResourceGroup** ottiene i gruppi di risorse Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="5d035-108">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="5d035-109">Puoi ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse per nome o per altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d035-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="5d035-110">Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="5d035-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="5d035-111">Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5d035-111">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5d035-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d035-112">EXAMPLES</span></span>

### <span data-ttu-id="5d035-113">Esempio 1: ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="5d035-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="5d035-114">Questo comando consente di ottenere il gruppo di risorse Azure nell'abbonamento denominato EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="5d035-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="5d035-115">Esempio 2: ottenere tutti i tag di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5d035-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="5d035-116">Questo comando consente di ottenere il gruppo di risorse denominato ContosoRG e di visualizzare i tag associati al gruppo.</span><span class="sxs-lookup"><span data-stu-id="5d035-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="5d035-117">Esempio 3: visualizzare i gruppi di risorse in base alla posizione</span><span class="sxs-lookup"><span data-stu-id="5d035-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="5d035-118">Esempio 4: visualizzare i nomi di tutti i gruppi di risorse in una determinata posizione</span><span class="sxs-lookup"><span data-stu-id="5d035-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="5d035-119">Esempio 5: visualizzare i gruppi di risorse i cui nomi iniziano con webserver</span><span class="sxs-lookup"><span data-stu-id="5d035-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="5d035-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d035-120">PARAMETERS</span></span>

### <span data-ttu-id="5d035-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5d035-121">-ApiVersion</span></span>
<span data-ttu-id="5d035-122">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d035-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5d035-123">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="5d035-123">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d035-124">-DefaultProfile</span></span>
<span data-ttu-id="5d035-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5d035-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5d035-126">-Id</span></span>
<span data-ttu-id="5d035-127">Specifica l'ID del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5d035-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="5d035-128">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="5d035-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5d035-129">-Location</span></span>
<span data-ttu-id="5d035-130">Specifica la posizione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5d035-130">Specifies the location of the resource group to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d035-131">-Name</span></span>
<span data-ttu-id="5d035-132">Specifica il nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5d035-132">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="5d035-133">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="5d035-133">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d035-134">-Pre</span></span>
<span data-ttu-id="5d035-135">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5d035-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d035-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d035-136">CommonParameters</span></span>
<span data-ttu-id="5d035-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d035-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d035-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d035-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d035-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d035-139">INPUTS</span></span>

### <span data-ttu-id="5d035-140">Stringa</span><span class="sxs-lookup"><span data-stu-id="5d035-140">String</span></span>
<span data-ttu-id="5d035-141">È possibile reindirizzare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="5d035-141">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5d035-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d035-142">OUTPUTS</span></span>

### <span data-ttu-id="5d035-143">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d035-143">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="5d035-144">Questo cmdlet restituisce i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d035-144">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="5d035-145">Note</span><span class="sxs-lookup"><span data-stu-id="5d035-145">NOTES</span></span>

## <span data-ttu-id="5d035-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d035-146">RELATED LINKS</span></span>

[<span data-ttu-id="5d035-147">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d035-147">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="5d035-148">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d035-148">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="5d035-149">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d035-149">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


