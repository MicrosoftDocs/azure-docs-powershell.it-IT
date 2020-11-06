---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514132"
---
# <span data-ttu-id="12ae1-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="12ae1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="12ae1-103">Ottiene le risorse.</span><span class="sxs-lookup"><span data-stu-id="12ae1-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12ae1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ae1-104">SYNTAX</span></span>

### <span data-ttu-id="12ae1-105">GetAllResources (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12ae1-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="12ae1-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="12ae1-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="12ae1-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="12ae1-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12ae1-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="12ae1-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="12ae1-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ae1-112">Getresourcecollection</span><span class="sxs-lookup"><span data-stu-id="12ae1-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ae1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12ae1-113">DESCRIPTION</span></span>
<span data-ttu-id="12ae1-114">Il cmdlet **Get-AzureRmResource** ottiene le risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="12ae1-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="12ae1-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ae1-115">EXAMPLES</span></span>

### <span data-ttu-id="12ae1-116">Esempio 1: ottenere tutte le risorse di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="12ae1-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="12ae1-117">Questo comando consente di ottenere una risorsa del tipo Microsoft. Web/sites in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="12ae1-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="12ae1-118">Esempio 2: ottenere una risorsa per nome</span><span class="sxs-lookup"><span data-stu-id="12ae1-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="12ae1-119">Questo comando ottiene una risorsa denominata ContosoWebsite in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="12ae1-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="12ae1-120">Esempio 3: visualizzare tutto lo stato degli account di archiviazione in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="12ae1-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="12ae1-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12ae1-121">PARAMETERS</span></span>

### <span data-ttu-id="12ae1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12ae1-122">-ApiVersion</span></span>
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

### <span data-ttu-id="12ae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ae1-123">-DefaultProfile</span></span>
<span data-ttu-id="12ae1-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="12ae1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12ae1-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="12ae1-125">-ExpandProperties</span></span>
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

### <span data-ttu-id="12ae1-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="12ae1-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="12ae1-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-128">-MyCollection</span><span class="sxs-lookup"><span data-stu-id="12ae1-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="12ae1-129">-ODataQuery</span></span>
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

### <span data-ttu-id="12ae1-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="12ae1-130">-Pre</span></span>
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

### <span data-ttu-id="12ae1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ae1-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ae1-132">-ResourceId</span></span>
<span data-ttu-id="12ae1-133">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="12ae1-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="12ae1-134">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="12ae1-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="12ae1-135">Questo cmdlet ottiene la risorsa con questo ID.</span><span class="sxs-lookup"><span data-stu-id="12ae1-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="12ae1-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="12ae1-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="12ae1-138">-TenantLevel</span></span>
<span data-ttu-id="12ae1-139">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="12ae1-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-140">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="12ae1-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12ae1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ae1-141">CommonParameters</span></span>
<span data-ttu-id="12ae1-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ae1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ae1-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ae1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ae1-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12ae1-144">INPUTS</span></span>

### <span data-ttu-id="12ae1-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="12ae1-145">None</span></span>
<span data-ttu-id="12ae1-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="12ae1-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12ae1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ae1-147">OUTPUTS</span></span>

### <span data-ttu-id="12ae1-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="12ae1-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="12ae1-149">Note</span><span class="sxs-lookup"><span data-stu-id="12ae1-149">NOTES</span></span>

## <span data-ttu-id="12ae1-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ae1-150">RELATED LINKS</span></span>

[<span data-ttu-id="12ae1-151">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="12ae1-152">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="12ae1-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="12ae1-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="12ae1-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="12ae1-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


