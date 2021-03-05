---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 6d2dd13f08fd9e621f30f586e7c46c828387e31e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963773"
---
# <span data-ttu-id="93c78-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="93c78-101">Remove-AzResource</span></span>

## <span data-ttu-id="93c78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c78-102">SYNOPSIS</span></span>
<span data-ttu-id="93c78-103">Rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="93c78-103">Removes a resource.</span></span>

## <span data-ttu-id="93c78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93c78-104">SYNTAX</span></span>

### <span data-ttu-id="93c78-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93c78-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93c78-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="93c78-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93c78-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="93c78-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93c78-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93c78-108">DESCRIPTION</span></span>
<span data-ttu-id="93c78-109">Il cmdlet **Remove-AzResource** rimuove una risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="93c78-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="93c78-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93c78-110">EXAMPLES</span></span>

### <span data-ttu-id="93c78-111">Esempio 1: Rimuovere una risorsa del sito Web</span><span class="sxs-lookup"><span data-stu-id="93c78-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="93c78-112">Questo comando rimuove la risorsa del sito Web denominata ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="93c78-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="93c78-113">Nell'esempio viene utilizzato un valore segnaposto per l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="93c78-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="93c78-114">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="93c78-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="93c78-115">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="93c78-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="93c78-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93c78-116">PARAMETERS</span></span>

### <span data-ttu-id="93c78-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93c78-117">-ApiVersion</span></span>
<span data-ttu-id="93c78-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="93c78-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="93c78-119">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="93c78-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="93c78-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93c78-120">-AsJob</span></span>
<span data-ttu-id="93c78-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="93c78-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93c78-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c78-122">-DefaultProfile</span></span>
<span data-ttu-id="93c78-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93c78-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93c78-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="93c78-124">-ExtensionResourceName</span></span>
<span data-ttu-id="93c78-125">Specifica il nome di una risorsa di estensione della risorsa che il cmdlet rimuove.</span><span class="sxs-lookup"><span data-stu-id="93c78-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="93c78-126">Ad esempio, per specificare un database, usare il formato seguente: nome database nome `/` server</span><span class="sxs-lookup"><span data-stu-id="93c78-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="93c78-127">-ExtensionResourceType</span></span>
<span data-ttu-id="93c78-128">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="93c78-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="93c78-129">Specifica il tipo di risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="93c78-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="93c78-130">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="93c78-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-131">-Force</span><span class="sxs-lookup"><span data-stu-id="93c78-131">-Force</span></span>
<span data-ttu-id="93c78-132">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="93c78-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93c78-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="93c78-133">-ODataQuery</span></span>
<span data-ttu-id="93c78-134">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="93c78-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="93c78-135">Questo cmdlet aggiunge questo valore alla richiesta in aggiunta ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="93c78-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="93c78-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="93c78-136">-Pre</span></span>
<span data-ttu-id="93c78-137">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="93c78-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="93c78-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c78-138">-ResourceGroupName</span></span>
<span data-ttu-id="93c78-139">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="93c78-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93c78-140">-ResourceId</span></span>
<span data-ttu-id="93c78-141">Specifica l'ID risorsa completo della risorsa che questo cmdlet rimuove.</span><span class="sxs-lookup"><span data-stu-id="93c78-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="93c78-142">L'ID include la sottoscrizione, come nell'esempio seguente: `/subscriptions/` ID sottoscrizione`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="93c78-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93c78-143">-ResourceName</span></span>
<span data-ttu-id="93c78-144">Specifica il nome della risorsa rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93c78-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="93c78-145">Ad esempio, per specificare un database, usare il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="93c78-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="93c78-146">-ResourceType</span></span>
<span data-ttu-id="93c78-147">Specifica il tipo di risorsa che il cmdlet rimuove.</span><span class="sxs-lookup"><span data-stu-id="93c78-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="93c78-148">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="93c78-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="93c78-149">-TenantLevel</span></span>
<span data-ttu-id="93c78-150">Indica che questo cmdlet opera a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="93c78-150">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c78-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93c78-151">-Confirm</span></span>
<span data-ttu-id="93c78-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93c78-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c78-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c78-153">-WhatIf</span></span>
<span data-ttu-id="93c78-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93c78-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c78-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93c78-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c78-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c78-156">CommonParameters</span></span>
<span data-ttu-id="93c78-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c78-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c78-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93c78-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c78-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="93c78-159">INPUTS</span></span>

### <span data-ttu-id="93c78-160">System.String</span><span class="sxs-lookup"><span data-stu-id="93c78-160">System.String</span></span>

## <span data-ttu-id="93c78-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93c78-161">OUTPUTS</span></span>

### <span data-ttu-id="93c78-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93c78-162">System.Boolean</span></span>

## <span data-ttu-id="93c78-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="93c78-163">NOTES</span></span>

## <span data-ttu-id="93c78-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93c78-164">RELATED LINKS</span></span>

[<span data-ttu-id="93c78-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="93c78-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="93c78-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="93c78-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="93c78-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="93c78-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="93c78-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="93c78-168">Set-AzResource</span></span>](./Set-AzResource.md)


