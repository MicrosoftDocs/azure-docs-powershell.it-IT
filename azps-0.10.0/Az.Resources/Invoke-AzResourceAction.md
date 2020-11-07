---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-Azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2f813b9da28ce42e9afb738af1fa0c247dffdc71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862546"
---
# <span data-ttu-id="09fa0-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="09fa0-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="09fa0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="09fa0-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="09fa0-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="09fa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09fa0-104">SYNTAX</span></span>

### <span data-ttu-id="09fa0-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09fa0-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09fa0-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="09fa0-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09fa0-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="09fa0-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fa0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09fa0-108">DESCRIPTION</span></span>
<span data-ttu-id="09fa0-109">Il cmdlet **Invoke-AzResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="09fa0-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="09fa0-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="09fa0-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="09fa0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09fa0-111">EXAMPLES</span></span>

## <span data-ttu-id="09fa0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09fa0-112">PARAMETERS</span></span>

### <span data-ttu-id="09fa0-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="09fa0-113">-Action</span></span>
<span data-ttu-id="09fa0-114">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="09fa0-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="09fa0-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09fa0-115">-ApiVersion</span></span>
<span data-ttu-id="09fa0-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="09fa0-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="09fa0-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="09fa0-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="09fa0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fa0-118">-DefaultProfile</span></span>
<span data-ttu-id="09fa0-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09fa0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09fa0-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="09fa0-120">-ExtensionResourceName</span></span>
<span data-ttu-id="09fa0-121">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="09fa0-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09fa0-122">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="09fa0-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="09fa0-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="09fa0-123">-ExtensionResourceType</span></span>
<span data-ttu-id="09fa0-124">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="09fa0-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="09fa0-125">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="09fa0-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="09fa0-126">-Force</span><span class="sxs-lookup"><span data-stu-id="09fa0-126">-Force</span></span>
<span data-ttu-id="09fa0-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09fa0-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09fa0-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="09fa0-128">-InformationAction</span></span>
<span data-ttu-id="09fa0-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="09fa0-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="09fa0-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="09fa0-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09fa0-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="09fa0-131">Continue</span></span>
- <span data-ttu-id="09fa0-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="09fa0-132">Ignore</span></span>
- <span data-ttu-id="09fa0-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="09fa0-133">Inquire</span></span>
- <span data-ttu-id="09fa0-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09fa0-134">SilentlyContinue</span></span>
- <span data-ttu-id="09fa0-135">Stop</span><span class="sxs-lookup"><span data-stu-id="09fa0-135">Stop</span></span>
- <span data-ttu-id="09fa0-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="09fa0-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa0-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09fa0-137">-InformationVariable</span></span>
<span data-ttu-id="09fa0-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="09fa0-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fa0-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="09fa0-139">-ODataQuery</span></span>
<span data-ttu-id="09fa0-140">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="09fa0-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="09fa0-141">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="09fa0-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="09fa0-142">-Parameters</span><span class="sxs-lookup"><span data-stu-id="09fa0-142">-Parameters</span></span>
<span data-ttu-id="09fa0-143">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09fa0-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="09fa0-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="09fa0-144">-Pre</span></span>
<span data-ttu-id="09fa0-145">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="09fa0-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09fa0-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fa0-146">-ResourceGroupName</span></span>
<span data-ttu-id="09fa0-147">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="09fa0-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="09fa0-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09fa0-148">-ResourceId</span></span>
<span data-ttu-id="09fa0-149">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="09fa0-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09fa0-150">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="09fa0-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="09fa0-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="09fa0-151">-ResourceName</span></span>
<span data-ttu-id="09fa0-152">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="09fa0-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="09fa0-153">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="09fa0-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="09fa0-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="09fa0-154">-ResourceType</span></span>
<span data-ttu-id="09fa0-155">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="09fa0-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="09fa0-156">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="09fa0-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="09fa0-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="09fa0-157">-TenantLevel</span></span>
<span data-ttu-id="09fa0-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="09fa0-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="09fa0-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09fa0-159">-Confirm</span></span>
<span data-ttu-id="09fa0-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09fa0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09fa0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fa0-161">-WhatIf</span></span>
<span data-ttu-id="09fa0-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09fa0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09fa0-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09fa0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09fa0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fa0-164">CommonParameters</span></span>
<span data-ttu-id="09fa0-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fa0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fa0-166">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fa0-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fa0-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09fa0-167">INPUTS</span></span>

## <span data-ttu-id="09fa0-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09fa0-168">OUTPUTS</span></span>

## <span data-ttu-id="09fa0-169">Note</span><span class="sxs-lookup"><span data-stu-id="09fa0-169">NOTES</span></span>

## <span data-ttu-id="09fa0-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09fa0-170">RELATED LINKS</span></span>
