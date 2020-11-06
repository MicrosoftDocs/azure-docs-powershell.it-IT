---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519547"
---
# <span data-ttu-id="fe5e5-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="fe5e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5e5-103">Ottiene le risorse.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe5e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe5e5-104">SYNTAX</span></span>

### <span data-ttu-id="fe5e5-105">Set di parametri tutte le risorse dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-105">The list all resources parameter set.</span></span> <span data-ttu-id="fe5e5-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="fe5e5-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-107">Ottenere una singola risorsa per il relativo ID.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-108">Ottenere una singola risorsa a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-109">Elenca le risorse in base all'ambito specificato a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-110">Ottenere risorse per nome e gruppo</span><span class="sxs-lookup"><span data-stu-id="fe5e5-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-111">Ottenere una risorsa per nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-112">Ottenere la risorsa per nome, gruppo e tipo</span><span class="sxs-lookup"><span data-stu-id="fe5e5-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-113">Raccolta di risorse Get</span><span class="sxs-lookup"><span data-stu-id="fe5e5-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5e5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe5e5-114">DESCRIPTION</span></span>
<span data-ttu-id="fe5e5-115">Il cmdlet **Get-AzureRmResource** ottiene le risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="fe5e5-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe5e5-116">EXAMPLES</span></span>

### <span data-ttu-id="fe5e5-117">Esempio 1: ottenere una risorsa</span><span class="sxs-lookup"><span data-stu-id="fe5e5-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="fe5e5-118">Questo comando consente di ottenere una risorsa del tipo Microsoft. Web/sites, denominata ContosoWebsite in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="fe5e5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe5e5-119">PARAMETERS</span></span>

### <span data-ttu-id="fe5e5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe5e5-120">-ApiVersion</span></span>
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

### <span data-ttu-id="fe5e5-121">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="fe5e5-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="fe5e5-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fe5e5-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fe5e5-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-124">-MyCollection</span><span class="sxs-lookup"><span data-stu-id="fe5e5-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fe5e5-125">-ODataQuery</span></span>
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

### <span data-ttu-id="fe5e5-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe5e5-126">-Pre</span></span>
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

### <span data-ttu-id="fe5e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5e5-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe5e5-128">-ResourceId</span></span>
<span data-ttu-id="fe5e5-129">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="fe5e5-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="fe5e5-130">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fe5e5-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="fe5e5-131">Questo cmdlet ottiene la risorsa con questo ID.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fe5e5-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fe5e5-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fe5e5-134">-TenantLevel</span></span>
<span data-ttu-id="fe5e5-135">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-136">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="fe5e5-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5e5-137">-DefaultProfile</span></span>
<span data-ttu-id="fe5e5-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe5e5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5e5-139">CommonParameters</span></span>
<span data-ttu-id="fe5e5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5e5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5e5-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5e5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5e5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe5e5-142">INPUTS</span></span>

## <span data-ttu-id="fe5e5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe5e5-143">OUTPUTS</span></span>

### <span data-ttu-id="fe5e5-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fe5e5-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fe5e5-145">Note</span><span class="sxs-lookup"><span data-stu-id="fe5e5-145">NOTES</span></span>

## <span data-ttu-id="fe5e5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe5e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="fe5e5-147">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="fe5e5-148">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fe5e5-149">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fe5e5-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fe5e5-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe5e5-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


