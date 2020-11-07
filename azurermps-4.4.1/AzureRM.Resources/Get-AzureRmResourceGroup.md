---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 0963d439efd4ab65a2117773cb6b7bb97043972c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686795"
---
# <span data-ttu-id="6f963-101">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f963-101">Get-AzureRmResourceGroup</span></span>

## <span data-ttu-id="6f963-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f963-102">SYNOPSIS</span></span>
<span data-ttu-id="6f963-103">Ottiene i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f963-103">Gets resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f963-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f963-104">SYNTAX</span></span>

### <span data-ttu-id="6f963-105">Elenca il gruppo di risorse in base al nome.</span><span class="sxs-lookup"><span data-stu-id="6f963-105">Lists the resource group based on the name.</span></span> <span data-ttu-id="6f963-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="6f963-106">(Default)</span></span>
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f963-107">Elenca il gruppo di risorse basato sull'ID.</span><span class="sxs-lookup"><span data-stu-id="6f963-107">Lists the resource group based on the Id.</span></span>
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f963-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f963-108">DESCRIPTION</span></span>
<span data-ttu-id="6f963-109">Il cmdlet **Get-AzureRmResourceGroup** ottiene i gruppi di risorse Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6f963-109">The **Get-AzureRmResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="6f963-110">Puoi ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse per nome o per altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f963-110">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="6f963-111">Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6f963-111">By default, this cmdlet gets all resource groups in the current subscription.</span></span>

<span data-ttu-id="6f963-112">Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6f963-112">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

## <span data-ttu-id="6f963-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f963-113">EXAMPLES</span></span>

### <span data-ttu-id="6f963-114">Esempio 1: ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="6f963-114">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="6f963-115">Questo comando consente di ottenere il gruppo di risorse Azure nell'abbonamento denominato EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="6f963-115">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="6f963-116">Esempio 2: ottenere tutti i tag di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6f963-116">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="6f963-117">Questo comando consente di ottenere il gruppo di risorse denominato ContosoRG e di visualizzare i tag associati al gruppo.</span><span class="sxs-lookup"><span data-stu-id="6f963-117">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

## <span data-ttu-id="6f963-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f963-118">PARAMETERS</span></span>

### <span data-ttu-id="6f963-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f963-119">-ApiVersion</span></span>
<span data-ttu-id="6f963-120">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f963-120">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6f963-121">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6f963-121">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6f963-122">-ID</span><span class="sxs-lookup"><span data-stu-id="6f963-122">-Id</span></span>
<span data-ttu-id="6f963-123">Specifica l'ID del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6f963-123">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="6f963-124">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6f963-124">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the Id.
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f963-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6f963-125">-Location</span></span>
<span data-ttu-id="6f963-126">Specifica la posizione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6f963-126">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f963-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f963-127">-Name</span></span>
<span data-ttu-id="6f963-128">Specifica il nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6f963-128">Specifies the name of the resource group to get.</span></span>
<span data-ttu-id="6f963-129">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6f963-129">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based on the name.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f963-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f963-130">-Pre</span></span>
<span data-ttu-id="6f963-131">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6f963-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f963-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f963-132">-DefaultProfile</span></span>
<span data-ttu-id="6f963-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f963-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f963-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f963-134">CommonParameters</span></span>
<span data-ttu-id="6f963-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f963-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f963-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f963-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f963-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f963-137">INPUTS</span></span>

### <span data-ttu-id="6f963-138">Stringa</span><span class="sxs-lookup"><span data-stu-id="6f963-138">String</span></span>
<span data-ttu-id="6f963-139">È possibile reindirizzare l'input al cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="6f963-139">You can pipe input to the cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6f963-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f963-140">OUTPUTS</span></span>

### <span data-ttu-id="6f963-141">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f963-141">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>
<span data-ttu-id="6f963-142">Questo cmdlet restituisce i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f963-142">This cmdlet returns resource groups.</span></span>

## <span data-ttu-id="6f963-143">Note</span><span class="sxs-lookup"><span data-stu-id="6f963-143">NOTES</span></span>

## <span data-ttu-id="6f963-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f963-144">RELATED LINKS</span></span>

[<span data-ttu-id="6f963-145">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f963-145">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="6f963-146">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f963-146">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="6f963-147">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f963-147">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


