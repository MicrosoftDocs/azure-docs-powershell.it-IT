---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687583"
---
# <span data-ttu-id="a54f6-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="a54f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a54f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a54f6-103">Rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a54f6-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a54f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a54f6-104">SYNTAX</span></span>

### <span data-ttu-id="a54f6-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a54f6-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a54f6-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a54f6-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a54f6-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a54f6-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a54f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a54f6-108">DESCRIPTION</span></span>
<span data-ttu-id="a54f6-109">Il cmdlet **Remove-AzureRmResource** rimuove una risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="a54f6-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="a54f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a54f6-110">EXAMPLES</span></span>

### <span data-ttu-id="a54f6-111">Esempio 1: rimuovere una risorsa sito Web</span><span class="sxs-lookup"><span data-stu-id="a54f6-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="a54f6-112">Questo comando rimuove la risorsa sito Web denominata ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="a54f6-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="a54f6-113">L'esempio usa un valore segnaposto per l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a54f6-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="a54f6-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a54f6-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a54f6-115">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a54f6-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a54f6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a54f6-116">PARAMETERS</span></span>

### <span data-ttu-id="a54f6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a54f6-117">-ApiVersion</span></span>
<span data-ttu-id="a54f6-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a54f6-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a54f6-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="a54f6-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a54f6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a54f6-120">-AsJob</span></span>
<span data-ttu-id="a54f6-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a54f6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a54f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54f6-122">-DefaultProfile</span></span>
<span data-ttu-id="a54f6-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a54f6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a54f6-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a54f6-124">-ExtensionResourceName</span></span>
<span data-ttu-id="a54f6-125">Specifica il nome di una risorsa di estensione della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54f6-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a54f6-126">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="a54f6-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a54f6-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a54f6-127">-ExtensionResourceType</span></span>
<span data-ttu-id="a54f6-128">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="a54f6-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a54f6-129">Specifica il tipo di risorsa estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a54f6-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="a54f6-130">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a54f6-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a54f6-131">-Force</span><span class="sxs-lookup"><span data-stu-id="a54f6-131">-Force</span></span>
<span data-ttu-id="a54f6-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a54f6-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a54f6-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a54f6-133">-ODataQuery</span></span>
<span data-ttu-id="a54f6-134">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a54f6-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="a54f6-135">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="a54f6-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a54f6-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="a54f6-136">-Pre</span></span>
<span data-ttu-id="a54f6-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a54f6-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a54f6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54f6-138">-ResourceGroupName</span></span>
<span data-ttu-id="a54f6-139">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a54f6-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="a54f6-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a54f6-140">-ResourceId</span></span>
<span data-ttu-id="a54f6-141">Specifica l'ID di risorsa completo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54f6-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a54f6-142">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a54f6-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a54f6-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a54f6-143">-ResourceName</span></span>
<span data-ttu-id="a54f6-144">Specifica il nome della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54f6-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a54f6-145">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a54f6-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a54f6-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a54f6-146">-ResourceType</span></span>
<span data-ttu-id="a54f6-147">Specifica il tipo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54f6-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a54f6-148">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a54f6-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a54f6-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a54f6-149">-TenantLevel</span></span>
<span data-ttu-id="a54f6-150">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="a54f6-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a54f6-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a54f6-151">-Confirm</span></span>
<span data-ttu-id="a54f6-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54f6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a54f6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a54f6-153">-WhatIf</span></span>
<span data-ttu-id="a54f6-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a54f6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a54f6-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a54f6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a54f6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54f6-156">CommonParameters</span></span>
<span data-ttu-id="a54f6-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54f6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54f6-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54f6-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54f6-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a54f6-159">INPUTS</span></span>

### <span data-ttu-id="a54f6-160">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a54f6-160">None</span></span>

## <span data-ttu-id="a54f6-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a54f6-161">OUTPUTS</span></span>

### <span data-ttu-id="a54f6-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a54f6-162">System.Boolean</span></span>

## <span data-ttu-id="a54f6-163">Note</span><span class="sxs-lookup"><span data-stu-id="a54f6-163">NOTES</span></span>

## <span data-ttu-id="a54f6-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a54f6-164">RELATED LINKS</span></span>

[<span data-ttu-id="a54f6-165">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="a54f6-166">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="a54f6-167">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="a54f6-168">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a54f6-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a54f6-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)

