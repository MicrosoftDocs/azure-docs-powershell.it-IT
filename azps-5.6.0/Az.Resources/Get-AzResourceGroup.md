---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: e431e1e9186cdaf0ec722b5a609a3f0a9f186bd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973534"
---
# <span data-ttu-id="a65a1-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a65a1-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="a65a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a65a1-103">Ottiene gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="a65a1-103">Gets resource groups.</span></span>

## <span data-ttu-id="a65a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a65a1-104">SYNTAX</span></span>

### <span data-ttu-id="a65a1-105">GetByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a65a1-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a65a1-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a65a1-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a65a1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a65a1-107">DESCRIPTION</span></span>
<span data-ttu-id="a65a1-108">Il cmdlet **Get-AzResourceGroup** ottiene i gruppi di risorse di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a65a1-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="a65a1-109">È possibile ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse in base al nome o ad altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="a65a1-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="a65a1-110">Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a65a1-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="a65a1-111">Per altre informazioni sulle risorse di Azure e sui gruppi di risorse di Azure, vedere il cmdlet New-AzResourceGroup Azure.</span><span class="sxs-lookup"><span data-stu-id="a65a1-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="a65a1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a65a1-112">EXAMPLES</span></span>

### <span data-ttu-id="a65a1-113">Esempio 1: Ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="a65a1-113">Example 1: Get a resource group by name</span></span>
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="a65a1-114">Questo comando recupera il gruppo di risorse di Azure nell'abbonamento denominato EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="a65a1-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="a65a1-115">Esempio 2: Ottenere tutti i tag di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a65a1-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="a65a1-116">Questo comando recupera il gruppo di risorse denominato ContosoRG e visualizza i tag associati al gruppo.</span><span class="sxs-lookup"><span data-stu-id="a65a1-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="a65a1-117">Esempio 3: Ottenere gruppi di risorse in base al tag</span><span class="sxs-lookup"><span data-stu-id="a65a1-117">Example 3: Get resource groups based on tag</span></span>
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### <span data-ttu-id="a65a1-118">Esempio 4: Visualizzare i gruppi di risorse per posizione</span><span class="sxs-lookup"><span data-stu-id="a65a1-118">Example 4: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="a65a1-119">Esempio 5: Visualizzare i nomi di tutti i gruppi di risorse in una posizione specifica</span><span class="sxs-lookup"><span data-stu-id="a65a1-119">Example 5: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="a65a1-120">Esempio 6: Visualizzare i gruppi di risorse i cui nomi iniziano con WebServer</span><span class="sxs-lookup"><span data-stu-id="a65a1-120">Example 6: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## <span data-ttu-id="a65a1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a65a1-121">PARAMETERS</span></span>

### <span data-ttu-id="a65a1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a65a1-122">-ApiVersion</span></span>
<span data-ttu-id="a65a1-123">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="a65a1-123">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a65a1-124">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="a65a1-124">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a65a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65a1-125">-DefaultProfile</span></span>
<span data-ttu-id="a65a1-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a65a1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a65a1-127">-Id</span><span class="sxs-lookup"><span data-stu-id="a65a1-127">-Id</span></span>
<span data-ttu-id="a65a1-128">Specifica l'ID del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a65a1-128">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="a65a1-129">Non sono consentiti caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="a65a1-129">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a65a1-130">-Location</span><span class="sxs-lookup"><span data-stu-id="a65a1-130">-Location</span></span>
<span data-ttu-id="a65a1-131">Specifica la posizione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a65a1-131">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="a65a1-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a65a1-132">-Name</span></span>
<span data-ttu-id="a65a1-133">Specifica il nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="a65a1-133">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="a65a1-134">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="a65a1-134">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

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

### <span data-ttu-id="a65a1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="a65a1-135">-Pre</span></span>
<span data-ttu-id="a65a1-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a65a1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a65a1-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a65a1-137">-Tag</span></span>
<span data-ttu-id="a65a1-138">Tabella hash del tag in base a cui filtrare i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="a65a1-138">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="a65a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65a1-139">CommonParameters</span></span>
<span data-ttu-id="a65a1-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65a1-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a65a1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65a1-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="a65a1-142">INPUTS</span></span>

### <span data-ttu-id="a65a1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a65a1-143">System.String</span></span>

### <span data-ttu-id="a65a1-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a65a1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a65a1-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a65a1-145">OUTPUTS</span></span>

### <span data-ttu-id="a65a1-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a65a1-146">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="a65a1-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="a65a1-147">NOTES</span></span>

## <span data-ttu-id="a65a1-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a65a1-148">RELATED LINKS</span></span>

[<span data-ttu-id="a65a1-149">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a65a1-149">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="a65a1-150">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a65a1-150">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="a65a1-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a65a1-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

