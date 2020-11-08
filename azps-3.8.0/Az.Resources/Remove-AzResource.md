---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 31039d71f0c26b6fea3e19220b3932d2abd02073
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030880"
---
# <span data-ttu-id="3e20d-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="3e20d-101">Remove-AzResource</span></span>

## <span data-ttu-id="3e20d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e20d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e20d-103">Rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e20d-103">Removes a resource.</span></span>

## <span data-ttu-id="3e20d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e20d-104">SYNTAX</span></span>

### <span data-ttu-id="3e20d-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e20d-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e20d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3e20d-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e20d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3e20d-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e20d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e20d-108">DESCRIPTION</span></span>
<span data-ttu-id="3e20d-109">Il cmdlet **Remove-AzResource** rimuove una risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="3e20d-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="3e20d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e20d-110">EXAMPLES</span></span>

### <span data-ttu-id="3e20d-111">Esempio 1: rimuovere una risorsa sito Web</span><span class="sxs-lookup"><span data-stu-id="3e20d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="3e20d-112">Questo comando rimuove la risorsa sito Web denominata ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="3e20d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="3e20d-113">L'esempio usa un valore segnaposto per l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3e20d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="3e20d-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3e20d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3e20d-115">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="3e20d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3e20d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e20d-116">PARAMETERS</span></span>

### <span data-ttu-id="3e20d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3e20d-117">-ApiVersion</span></span>
<span data-ttu-id="3e20d-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="3e20d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3e20d-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="3e20d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3e20d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e20d-120">-AsJob</span></span>
<span data-ttu-id="3e20d-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3e20d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e20d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e20d-122">-DefaultProfile</span></span>
<span data-ttu-id="3e20d-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e20d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e20d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="3e20d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="3e20d-125">Specifica il nome di una risorsa di estensione della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e20d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3e20d-126">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="3e20d-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="3e20d-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="3e20d-127">-ExtensionResourceType</span></span>
<span data-ttu-id="3e20d-128">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="3e20d-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="3e20d-129">Specifica il tipo di risorsa estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e20d-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="3e20d-130">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="3e20d-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="3e20d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3e20d-131">-Force</span></span>
<span data-ttu-id="3e20d-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e20d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e20d-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="3e20d-133">-ODataQuery</span></span>
<span data-ttu-id="3e20d-134">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="3e20d-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="3e20d-135">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="3e20d-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="3e20d-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="3e20d-136">-Pre</span></span>
<span data-ttu-id="3e20d-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="3e20d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3e20d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e20d-138">-ResourceGroupName</span></span>
<span data-ttu-id="3e20d-139">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e20d-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="3e20d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e20d-140">-ResourceId</span></span>
<span data-ttu-id="3e20d-141">Specifica l'ID di risorsa completo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e20d-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3e20d-142">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="3e20d-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="3e20d-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3e20d-143">-ResourceName</span></span>
<span data-ttu-id="3e20d-144">Specifica il nome della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e20d-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3e20d-145">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="3e20d-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="3e20d-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3e20d-146">-ResourceType</span></span>
<span data-ttu-id="3e20d-147">Specifica il tipo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e20d-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="3e20d-148">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="3e20d-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="3e20d-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3e20d-149">-TenantLevel</span></span>
<span data-ttu-id="3e20d-150">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="3e20d-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="3e20d-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e20d-151">-Confirm</span></span>
<span data-ttu-id="3e20d-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e20d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e20d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e20d-153">-WhatIf</span></span>
<span data-ttu-id="3e20d-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e20d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e20d-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e20d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e20d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e20d-156">CommonParameters</span></span>
<span data-ttu-id="3e20d-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e20d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e20d-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e20d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e20d-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e20d-159">INPUTS</span></span>

### <span data-ttu-id="3e20d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3e20d-160">System.String</span></span>

## <span data-ttu-id="3e20d-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e20d-161">OUTPUTS</span></span>

### <span data-ttu-id="3e20d-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e20d-162">System.Boolean</span></span>

## <span data-ttu-id="3e20d-163">Note</span><span class="sxs-lookup"><span data-stu-id="3e20d-163">NOTES</span></span>

## <span data-ttu-id="3e20d-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e20d-164">RELATED LINKS</span></span>

[<span data-ttu-id="3e20d-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="3e20d-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="3e20d-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="3e20d-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="3e20d-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="3e20d-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="3e20d-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="3e20d-168">Set-AzResource</span></span>](./Set-AzResource.md)


