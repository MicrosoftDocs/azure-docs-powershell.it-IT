---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677384"
---
# <span data-ttu-id="b5743-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5743-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="b5743-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5743-102">SYNOPSIS</span></span>
<span data-ttu-id="b5743-103">Ottiene i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5743-103">Gets resource groups.</span></span>

## <span data-ttu-id="b5743-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5743-104">SYNTAX</span></span>

### <span data-ttu-id="b5743-105">GetByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5743-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5743-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b5743-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5743-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5743-107">DESCRIPTION</span></span>
<span data-ttu-id="b5743-108">Il cmdlet **Get-AzResourceGroup** ottiene i gruppi di risorse Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b5743-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="b5743-109">Puoi ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse per nome o per altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5743-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="b5743-110">Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b5743-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="b5743-111">Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5743-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="b5743-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5743-112">EXAMPLES</span></span>

### <span data-ttu-id="b5743-113">Esempio 1: ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="b5743-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="b5743-114">Questo comando consente di ottenere il gruppo di risorse Azure nell'abbonamento denominato EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="b5743-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="b5743-115">Esempio 2: ottenere tutti i tag di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b5743-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="b5743-116">Questo comando consente di ottenere il gruppo di risorse denominato ContosoRG e di visualizzare i tag associati al gruppo.</span><span class="sxs-lookup"><span data-stu-id="b5743-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="b5743-117">Esempio 3: visualizzare i gruppi di risorse in base alla posizione</span><span class="sxs-lookup"><span data-stu-id="b5743-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="b5743-118">Esempio 4: visualizzare i nomi di tutti i gruppi di risorse in una determinata posizione</span><span class="sxs-lookup"><span data-stu-id="b5743-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="b5743-119">Esempio 5: visualizzare i gruppi di risorse i cui nomi iniziano con webserver</span><span class="sxs-lookup"><span data-stu-id="b5743-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### <span data-ttu-id="b5743-120">Esempio 6: ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="b5743-120">Example 6: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

<span data-ttu-id="b5743-121">Questo comando consente di ottenere il gruppo di risorse Azure nell'abbonamento che inizia con "EngineerBlog".</span><span class="sxs-lookup"><span data-stu-id="b5743-121">This command gets the Azure resource group in your subscription that start with "EngineerBlog".</span></span>

## <span data-ttu-id="b5743-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5743-122">PARAMETERS</span></span>

### <span data-ttu-id="b5743-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5743-123">-ApiVersion</span></span>
<span data-ttu-id="b5743-124">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5743-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b5743-125">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b5743-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b5743-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5743-126">-DefaultProfile</span></span>
<span data-ttu-id="b5743-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5743-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5743-128">-ID</span><span class="sxs-lookup"><span data-stu-id="b5743-128">-Id</span></span>
<span data-ttu-id="b5743-129">Specifica l'ID del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b5743-129">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="b5743-130">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="b5743-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5743-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b5743-131">-Location</span></span>
<span data-ttu-id="b5743-132">Specifica la posizione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b5743-132">Specifies the location of the resource group to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5743-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5743-133">-Name</span></span>
<span data-ttu-id="b5743-134">Specifica il nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b5743-134">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="b5743-135">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="b5743-135">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b5743-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="b5743-136">-Pre</span></span>
<span data-ttu-id="b5743-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b5743-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b5743-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5743-138">-Tag</span></span>
<span data-ttu-id="b5743-139">Hashtable di tag per filtrare i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5743-139">The tag hashtable to filter resource groups by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5743-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5743-140">CommonParameters</span></span>
<span data-ttu-id="b5743-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5743-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5743-142">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5743-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5743-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5743-143">INPUTS</span></span>

### <span data-ttu-id="b5743-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b5743-144">System.String</span></span>

### <span data-ttu-id="b5743-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b5743-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b5743-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5743-146">OUTPUTS</span></span>

### <span data-ttu-id="b5743-147">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5743-147">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="b5743-148">Note</span><span class="sxs-lookup"><span data-stu-id="b5743-148">NOTES</span></span>

## <span data-ttu-id="b5743-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5743-149">RELATED LINKS</span></span>

[<span data-ttu-id="b5743-150">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5743-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b5743-151">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5743-151">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="b5743-152">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5743-152">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


