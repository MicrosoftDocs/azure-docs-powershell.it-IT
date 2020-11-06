---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519520"
---
# <span data-ttu-id="85841-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="85841-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85841-102">SYNOPSIS</span></span>
<span data-ttu-id="85841-103">Rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="85841-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85841-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85841-104">SYNTAX</span></span>

### <span data-ttu-id="85841-105">ID risorsa (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85841-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85841-106">Risorsa che risiede a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="85841-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85841-107">Risorsa che risiede a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="85841-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85841-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85841-108">DESCRIPTION</span></span>
<span data-ttu-id="85841-109">Il cmdlet **Remove-AzureRmResource** rimuove una risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="85841-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="85841-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85841-110">EXAMPLES</span></span>

### <span data-ttu-id="85841-111">Esempio 1: rimuovere una risorsa sito Web</span><span class="sxs-lookup"><span data-stu-id="85841-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="85841-112">Questo comando rimuove la risorsa sito Web denominata ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="85841-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="85841-113">L'esempio usa un valore segnaposto per l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="85841-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="85841-114">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="85841-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="85841-115">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="85841-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="85841-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85841-116">PARAMETERS</span></span>

### <span data-ttu-id="85841-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="85841-117">-ApiVersion</span></span>
<span data-ttu-id="85841-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="85841-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="85841-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="85841-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="85841-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="85841-120">-ExtensionResourceName</span></span>
<span data-ttu-id="85841-121">Specifica il nome di una risorsa di estensione della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85841-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="85841-122">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="85841-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="85841-123">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="85841-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="85841-124">-ExtensionResourceType</span></span>
<span data-ttu-id="85841-125">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="85841-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="85841-126">Specifica il tipo di risorsa estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="85841-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="85841-127">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="85841-127">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-128">-Force</span><span class="sxs-lookup"><span data-stu-id="85841-128">-Force</span></span>
<span data-ttu-id="85841-129">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="85841-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85841-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="85841-130">-ODataQuery</span></span>
<span data-ttu-id="85841-131">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="85841-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="85841-132">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="85841-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="85841-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="85841-133">-Pre</span></span>
<span data-ttu-id="85841-134">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="85841-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="85841-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85841-135">-ResourceGroupName</span></span>
<span data-ttu-id="85841-136">Specifica il nome del gruppo di risorse da cui questo cmdlet rimuove una risorsa.</span><span class="sxs-lookup"><span data-stu-id="85841-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85841-137">-ResourceId</span></span>
<span data-ttu-id="85841-138">Specifica l'ID di risorsa completo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85841-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="85841-139">L'ID include l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="85841-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="85841-140">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="85841-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="85841-141">-ResourceName</span></span>
<span data-ttu-id="85841-142">Specifica il nome della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85841-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="85841-143">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="85841-143">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="85841-144">-ResourceType</span></span>
<span data-ttu-id="85841-145">Specifica il tipo della risorsa rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85841-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="85841-146">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="85841-146">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85841-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="85841-147">-TenantLevel</span></span>
<span data-ttu-id="85841-148">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="85841-148">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85841-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85841-149">-Confirm</span></span>
<span data-ttu-id="85841-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85841-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85841-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85841-151">-WhatIf</span></span>
<span data-ttu-id="85841-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85841-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85841-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85841-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85841-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85841-154">-DefaultProfile</span></span>
<span data-ttu-id="85841-155">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85841-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85841-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85841-156">CommonParameters</span></span>
<span data-ttu-id="85841-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85841-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85841-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85841-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85841-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85841-159">INPUTS</span></span>

## <span data-ttu-id="85841-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85841-160">OUTPUTS</span></span>

### <span data-ttu-id="85841-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85841-161">System.Boolean</span></span>

## <span data-ttu-id="85841-162">Note</span><span class="sxs-lookup"><span data-stu-id="85841-162">NOTES</span></span>

## <span data-ttu-id="85841-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85841-163">RELATED LINKS</span></span>

[<span data-ttu-id="85841-164">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="85841-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="85841-166">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="85841-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="85841-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="85841-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


