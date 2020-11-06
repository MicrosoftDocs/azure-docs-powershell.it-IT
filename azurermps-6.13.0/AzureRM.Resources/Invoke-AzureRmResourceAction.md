---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 0a8fa9f13e77617a7f9efbd31909edfd64bf353a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514836"
---
# <span data-ttu-id="ccdda-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="ccdda-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="ccdda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccdda-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdda-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ccdda-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccdda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccdda-104">SYNTAX</span></span>

### <span data-ttu-id="ccdda-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccdda-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ccdda-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ccdda-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdda-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ccdda-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdda-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccdda-108">DESCRIPTION</span></span>
<span data-ttu-id="ccdda-109">Il cmdlet **Invoke-AzureRmResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="ccdda-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="ccdda-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ccdda-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="ccdda-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccdda-111">EXAMPLES</span></span>

## <span data-ttu-id="ccdda-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccdda-112">PARAMETERS</span></span>

### <span data-ttu-id="ccdda-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="ccdda-113">-Action</span></span>
<span data-ttu-id="ccdda-114">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="ccdda-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="ccdda-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ccdda-115">-ApiVersion</span></span>
<span data-ttu-id="ccdda-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ccdda-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ccdda-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="ccdda-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ccdda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdda-118">-DefaultProfile</span></span>
<span data-ttu-id="ccdda-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ccdda-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccdda-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ccdda-120">-ExtensionResourceName</span></span>
<span data-ttu-id="ccdda-121">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ccdda-122">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="ccdda-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="ccdda-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ccdda-123">-ExtensionResourceType</span></span>
<span data-ttu-id="ccdda-124">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="ccdda-125">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ccdda-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ccdda-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ccdda-126">-Force</span></span>
<span data-ttu-id="ccdda-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ccdda-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccdda-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ccdda-128">-InformationAction</span></span>
<span data-ttu-id="ccdda-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ccdda-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ccdda-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ccdda-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccdda-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="ccdda-131">Continue</span></span>
- <span data-ttu-id="ccdda-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="ccdda-132">Ignore</span></span>
- <span data-ttu-id="ccdda-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ccdda-133">Inquire</span></span>
- <span data-ttu-id="ccdda-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ccdda-134">SilentlyContinue</span></span>
- <span data-ttu-id="ccdda-135">Stop</span><span class="sxs-lookup"><span data-stu-id="ccdda-135">Stop</span></span>
- <span data-ttu-id="ccdda-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ccdda-136">Suspend</span></span>

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

### <span data-ttu-id="ccdda-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ccdda-137">-InformationVariable</span></span>
<span data-ttu-id="ccdda-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ccdda-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ccdda-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ccdda-139">-ODataQuery</span></span>
<span data-ttu-id="ccdda-140">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="ccdda-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ccdda-141">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="ccdda-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ccdda-142">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ccdda-142">-Parameters</span></span>
<span data-ttu-id="ccdda-143">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdda-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="ccdda-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="ccdda-144">-Pre</span></span>
<span data-ttu-id="ccdda-145">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ccdda-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ccdda-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdda-146">-ResourceGroupName</span></span>
<span data-ttu-id="ccdda-147">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="ccdda-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccdda-148">-ResourceId</span></span>
<span data-ttu-id="ccdda-149">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ccdda-150">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ccdda-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ccdda-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ccdda-151">-ResourceName</span></span>
<span data-ttu-id="ccdda-152">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="ccdda-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="ccdda-153">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ccdda-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ccdda-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ccdda-154">-ResourceType</span></span>
<span data-ttu-id="ccdda-155">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ccdda-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="ccdda-156">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ccdda-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ccdda-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ccdda-157">-TenantLevel</span></span>
<span data-ttu-id="ccdda-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="ccdda-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ccdda-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccdda-159">-Confirm</span></span>
<span data-ttu-id="ccdda-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdda-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdda-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdda-161">-WhatIf</span></span>
<span data-ttu-id="ccdda-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccdda-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdda-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccdda-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdda-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdda-164">CommonParameters</span></span>
<span data-ttu-id="ccdda-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdda-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdda-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdda-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdda-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccdda-167">INPUTS</span></span>

## <span data-ttu-id="ccdda-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccdda-168">OUTPUTS</span></span>

## <span data-ttu-id="ccdda-169">Note</span><span class="sxs-lookup"><span data-stu-id="ccdda-169">NOTES</span></span>

## <span data-ttu-id="ccdda-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccdda-170">RELATED LINKS</span></span>
