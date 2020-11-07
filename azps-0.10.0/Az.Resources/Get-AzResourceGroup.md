---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862570"
---
# <span data-ttu-id="b099d-101">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b099d-101">Get-AzResourceGroup</span></span>

## <span data-ttu-id="b099d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b099d-102">SYNOPSIS</span></span>
<span data-ttu-id="b099d-103">Ottiene i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="b099d-103">Gets resource groups.</span></span>

## <span data-ttu-id="b099d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b099d-104">SYNTAX</span></span>

### <span data-ttu-id="b099d-105">GetByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b099d-105">GetByResourceGroupName (Default)</span></span>
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b099d-106">GetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="b099d-106">GetByResourceGroupId</span></span>
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b099d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b099d-107">DESCRIPTION</span></span>
<span data-ttu-id="b099d-108">Il cmdlet **Get-AzResourceGroup** ottiene i gruppi di risorse Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b099d-108">The **Get-AzResourceGroup** cmdlet gets Azure resource groups in the current subscription.</span></span>
<span data-ttu-id="b099d-109">Puoi ottenere tutti i gruppi di risorse oppure specificare un gruppo di risorse per nome o per altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="b099d-109">You can get all resource groups, or specify a resource group by name or by other properties.</span></span>
<span data-ttu-id="b099d-110">Per impostazione predefinita, questo cmdlet recupera tutti i gruppi di risorse nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b099d-110">By default, this cmdlet gets all resource groups in the current subscription.</span></span>
<span data-ttu-id="b099d-111">Per altre informazioni sulle risorse Azure e sui gruppi di risorse Azure, vedere il cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b099d-111">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="b099d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b099d-112">EXAMPLES</span></span>

### <span data-ttu-id="b099d-113">Esempio 1: ottenere un gruppo di risorse per nome</span><span class="sxs-lookup"><span data-stu-id="b099d-113">Example 1: Get a resource group by name</span></span>
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

<span data-ttu-id="b099d-114">Questo comando consente di ottenere il gruppo di risorse Azure nell'abbonamento denominato EngineerBlog.</span><span class="sxs-lookup"><span data-stu-id="b099d-114">This command gets the Azure resource group in your subscription named EngineerBlog.</span></span>

### <span data-ttu-id="b099d-115">Esempio 2: ottenere tutti i tag di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b099d-115">Example 2: Get all tags of a resource group</span></span>
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="b099d-116">Questo comando consente di ottenere il gruppo di risorse denominato ContosoRG e di visualizzare i tag associati al gruppo.</span><span class="sxs-lookup"><span data-stu-id="b099d-116">This command gets the resource group named ContosoRG, and displays the tags associated with that group.</span></span>

### <span data-ttu-id="b099d-117">Esempio 3: visualizzare i gruppi di risorse in base alla posizione</span><span class="sxs-lookup"><span data-stu-id="b099d-117">Example 3: Show the Resource groups by location</span></span>
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### <span data-ttu-id="b099d-118">Esempio 4: visualizzare i nomi di tutti i gruppi di risorse in una determinata posizione</span><span class="sxs-lookup"><span data-stu-id="b099d-118">Example 4: Show the names of all the Resource groups in a particular location</span></span>
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### <span data-ttu-id="b099d-119">Esempio 5: visualizzare i gruppi di risorse i cui nomi iniziano con webserver</span><span class="sxs-lookup"><span data-stu-id="b099d-119">Example 5: Show the Resource groups whose names begin with WebServer</span></span>
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## <span data-ttu-id="b099d-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b099d-120">PARAMETERS</span></span>

### <span data-ttu-id="b099d-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b099d-121">-ApiVersion</span></span>
<span data-ttu-id="b099d-122">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b099d-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b099d-123">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b099d-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b099d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b099d-124">-DefaultProfile</span></span>
<span data-ttu-id="b099d-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b099d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b099d-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b099d-126">-Id</span></span>
<span data-ttu-id="b099d-127">Specifica l'ID del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b099d-127">Specifies the ID of the resource group to get.</span></span>
<span data-ttu-id="b099d-128">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="b099d-128">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="b099d-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b099d-129">-Location</span></span>
<span data-ttu-id="b099d-130">Specifica la posizione del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b099d-130">Specifies the location of the resource group to get.</span></span>

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

### <span data-ttu-id="b099d-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="b099d-131">-Name</span></span>
<span data-ttu-id="b099d-132">Specifica il nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b099d-132">Specifies the name of the resource group to get.</span></span> <span data-ttu-id="b099d-133">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="b099d-133">This parameter supports wildcards at the beginning and/or the end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b099d-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="b099d-134">-Pre</span></span>
<span data-ttu-id="b099d-135">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b099d-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b099d-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="b099d-136">-Tag</span></span>
<span data-ttu-id="b099d-137">Hashtable di tag per filtrare i gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="b099d-137">The tag hashtable to filter resource groups by.</span></span>

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

### <span data-ttu-id="b099d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b099d-138">CommonParameters</span></span>
<span data-ttu-id="b099d-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b099d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b099d-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b099d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b099d-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b099d-141">INPUTS</span></span>

### <span data-ttu-id="b099d-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b099d-142">None</span></span>

## <span data-ttu-id="b099d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b099d-143">OUTPUTS</span></span>

### <span data-ttu-id="b099d-144">Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b099d-144">Microsoft.Azure.Commands.ResourceManagement.PSResourceGroup</span></span>

## <span data-ttu-id="b099d-145">Note</span><span class="sxs-lookup"><span data-stu-id="b099d-145">NOTES</span></span>

## <span data-ttu-id="b099d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b099d-146">RELATED LINKS</span></span>

[<span data-ttu-id="b099d-147">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b099d-147">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b099d-148">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b099d-148">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="b099d-149">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b099d-149">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


