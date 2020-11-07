---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854869"
---
# <span data-ttu-id="b87b1-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="b87b1-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="b87b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b87b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b87b1-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b87b1-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="b87b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b87b1-104">SYNTAX</span></span>

### <span data-ttu-id="b87b1-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b87b1-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b87b1-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b87b1-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b87b1-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b87b1-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b87b1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b87b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b87b1-109">Il cmdlet **Invoke-AzResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="b87b1-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="b87b1-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b87b1-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="b87b1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b87b1-111">EXAMPLES</span></span>

## <span data-ttu-id="b87b1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b87b1-112">PARAMETERS</span></span>

### <span data-ttu-id="b87b1-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="b87b1-113">-Action</span></span>
<span data-ttu-id="b87b1-114">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="b87b1-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87b1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b87b1-115">-ApiVersion</span></span>
<span data-ttu-id="b87b1-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b87b1-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b87b1-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="b87b1-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b87b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87b1-118">-DefaultProfile</span></span>
<span data-ttu-id="b87b1-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b87b1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b87b1-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b87b1-120">-ExtensionResourceName</span></span>
<span data-ttu-id="b87b1-121">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="b87b1-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b87b1-122">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="b87b1-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="b87b1-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b87b1-123">-ExtensionResourceType</span></span>
<span data-ttu-id="b87b1-124">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="b87b1-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="b87b1-125">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b87b1-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b87b1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b87b1-126">-Force</span></span>
<span data-ttu-id="b87b1-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b87b1-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b87b1-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b87b1-128">-ODataQuery</span></span>
<span data-ttu-id="b87b1-129">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="b87b1-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="b87b1-130">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="b87b1-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b87b1-131">-Parameters</span><span class="sxs-lookup"><span data-stu-id="b87b1-131">-Parameters</span></span>
<span data-ttu-id="b87b1-132">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b87b1-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87b1-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="b87b1-133">-Pre</span></span>
<span data-ttu-id="b87b1-134">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b87b1-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b87b1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b87b1-135">-ResourceGroupName</span></span>
<span data-ttu-id="b87b1-136">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="b87b1-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="b87b1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b87b1-137">-ResourceId</span></span>
<span data-ttu-id="b87b1-138">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="b87b1-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b87b1-139">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b87b1-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b87b1-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b87b1-140">-ResourceName</span></span>
<span data-ttu-id="b87b1-141">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="b87b1-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="b87b1-142">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b87b1-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b87b1-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b87b1-143">-ResourceType</span></span>
<span data-ttu-id="b87b1-144">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b87b1-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="b87b1-145">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b87b1-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b87b1-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b87b1-146">-TenantLevel</span></span>
<span data-ttu-id="b87b1-147">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="b87b1-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b87b1-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b87b1-148">-Confirm</span></span>
<span data-ttu-id="b87b1-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b87b1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b87b1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b87b1-150">-WhatIf</span></span>
<span data-ttu-id="b87b1-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b87b1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b87b1-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b87b1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b87b1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87b1-153">CommonParameters</span></span>
<span data-ttu-id="b87b1-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b87b1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87b1-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b87b1-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87b1-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b87b1-156">INPUTS</span></span>

### <span data-ttu-id="b87b1-157">System. String</span><span class="sxs-lookup"><span data-stu-id="b87b1-157">System.String</span></span>

## <span data-ttu-id="b87b1-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b87b1-158">OUTPUTS</span></span>

### <span data-ttu-id="b87b1-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b87b1-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b87b1-160">Note</span><span class="sxs-lookup"><span data-stu-id="b87b1-160">NOTES</span></span>

## <span data-ttu-id="b87b1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b87b1-161">RELATED LINKS</span></span>
