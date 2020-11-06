---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518000"
---
# <span data-ttu-id="f0efd-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="f0efd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0efd-102">SYNOPSIS</span></span>
<span data-ttu-id="f0efd-103">Rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0efd-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0efd-104">SYNTAX</span></span>

### <span data-ttu-id="f0efd-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0efd-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0efd-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f0efd-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0efd-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0efd-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0efd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0efd-108">DESCRIPTION</span></span>
<span data-ttu-id="f0efd-109">Il cmdlet **Remove-AzureRmResource** rimuove una risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="f0efd-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="f0efd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0efd-110">EXAMPLES</span></span>

### <span data-ttu-id="f0efd-111">Esempio 1: rimuovere una risorsa sito Web</span><span class="sxs-lookup"><span data-stu-id="f0efd-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="f0efd-112">Questo comando rimuove la risorsa sito Web denominata ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="f0efd-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="f0efd-113">L'esempio usa un valore segnaposto per l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f0efd-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="f0efd-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f0efd-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f0efd-115">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="f0efd-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f0efd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0efd-116">PARAMETERS</span></span>

### <span data-ttu-id="f0efd-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0efd-117">-ApiVersion</span></span>
<span data-ttu-id="f0efd-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f0efd-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0efd-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="f0efd-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f0efd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0efd-120">-AsJob</span></span>
<span data-ttu-id="f0efd-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f0efd-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0efd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0efd-122">-DefaultProfile</span></span>
<span data-ttu-id="f0efd-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0efd-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0efd-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f0efd-124">-ExtensionResourceName</span></span>
<span data-ttu-id="f0efd-125">Specifica il nome di una risorsa di estensione della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0efd-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f0efd-126">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="f0efd-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="f0efd-127">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="f0efd-127">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f0efd-128">-ExtensionResourceType</span></span>
<span data-ttu-id="f0efd-129">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="f0efd-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="f0efd-130">Specifica il tipo di risorsa estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0efd-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="f0efd-131">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f0efd-131">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f0efd-132">-Force</span></span>
<span data-ttu-id="f0efd-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f0efd-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0efd-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f0efd-134">-ODataQuery</span></span>
<span data-ttu-id="f0efd-135">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="f0efd-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f0efd-136">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="f0efd-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="f0efd-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0efd-137">-Pre</span></span>
<span data-ttu-id="f0efd-138">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f0efd-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f0efd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0efd-139">-ResourceGroupName</span></span>
<span data-ttu-id="f0efd-140">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f0efd-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0efd-141">-ResourceId</span></span>
<span data-ttu-id="f0efd-142">Specifica l'ID di risorsa completo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0efd-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f0efd-143">L'ID include l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="f0efd-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="f0efd-144">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f0efd-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f0efd-145">-ResourceName</span></span>
<span data-ttu-id="f0efd-146">Specifica il nome della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0efd-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f0efd-147">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="f0efd-147">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f0efd-148">-ResourceType</span></span>
<span data-ttu-id="f0efd-149">Specifica il tipo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0efd-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="f0efd-150">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="f0efd-150">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f0efd-151">-TenantLevel</span></span>
<span data-ttu-id="f0efd-152">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="f0efd-152">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0efd-153">-Confirm</span></span>
<span data-ttu-id="f0efd-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0efd-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0efd-155">-WhatIf</span></span>
<span data-ttu-id="f0efd-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0efd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0efd-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0efd-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0efd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0efd-158">CommonParameters</span></span>
<span data-ttu-id="f0efd-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0efd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0efd-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0efd-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0efd-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0efd-161">INPUTS</span></span>

### <span data-ttu-id="f0efd-162">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0efd-162">None</span></span>
<span data-ttu-id="f0efd-163">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f0efd-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0efd-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0efd-164">OUTPUTS</span></span>

### <span data-ttu-id="f0efd-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0efd-165">System.Boolean</span></span>

## <span data-ttu-id="f0efd-166">Note</span><span class="sxs-lookup"><span data-stu-id="f0efd-166">NOTES</span></span>

## <span data-ttu-id="f0efd-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0efd-167">RELATED LINKS</span></span>

[<span data-ttu-id="f0efd-168">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="f0efd-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="f0efd-170">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="f0efd-171">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f0efd-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0efd-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


