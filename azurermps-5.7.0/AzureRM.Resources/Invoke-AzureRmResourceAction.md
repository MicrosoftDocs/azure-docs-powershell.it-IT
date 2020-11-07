---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686695"
---
# <span data-ttu-id="56980-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="56980-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="56980-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56980-102">SYNOPSIS</span></span>
<span data-ttu-id="56980-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="56980-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56980-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56980-104">SYNTAX</span></span>

### <span data-ttu-id="56980-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56980-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56980-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="56980-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56980-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="56980-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56980-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56980-108">DESCRIPTION</span></span>
<span data-ttu-id="56980-109">Il cmdlet **Invoke-AzureRmResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="56980-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="56980-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="56980-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="56980-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56980-111">EXAMPLES</span></span>

## <span data-ttu-id="56980-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56980-112">PARAMETERS</span></span>

### <span data-ttu-id="56980-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="56980-113">-Action</span></span>
<span data-ttu-id="56980-114">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="56980-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56980-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="56980-115">-ApiVersion</span></span>
<span data-ttu-id="56980-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="56980-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="56980-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="56980-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="56980-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56980-118">-DefaultProfile</span></span>
<span data-ttu-id="56980-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56980-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56980-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="56980-120">-ExtensionResourceName</span></span>
<span data-ttu-id="56980-121">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="56980-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="56980-122">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="56980-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="56980-123">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="56980-123">server name`/`database name</span></span>

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

### <span data-ttu-id="56980-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="56980-124">-ExtensionResourceType</span></span>
<span data-ttu-id="56980-125">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="56980-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="56980-126">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="56980-126">For instance:</span></span> 

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

### <span data-ttu-id="56980-127">-Force</span><span class="sxs-lookup"><span data-stu-id="56980-127">-Force</span></span>
<span data-ttu-id="56980-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="56980-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56980-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56980-129">-InformationAction</span></span>
<span data-ttu-id="56980-130">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="56980-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56980-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56980-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56980-132">Continuare</span><span class="sxs-lookup"><span data-stu-id="56980-132">Continue</span></span>
- <span data-ttu-id="56980-133">Ignora</span><span class="sxs-lookup"><span data-stu-id="56980-133">Ignore</span></span>
- <span data-ttu-id="56980-134">Informarsi</span><span class="sxs-lookup"><span data-stu-id="56980-134">Inquire</span></span>
- <span data-ttu-id="56980-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56980-135">SilentlyContinue</span></span>
- <span data-ttu-id="56980-136">Stop</span><span class="sxs-lookup"><span data-stu-id="56980-136">Stop</span></span>
- <span data-ttu-id="56980-137">Sospensione</span><span class="sxs-lookup"><span data-stu-id="56980-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56980-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56980-138">-InformationVariable</span></span>
<span data-ttu-id="56980-139">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="56980-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56980-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="56980-140">-ODataQuery</span></span>
<span data-ttu-id="56980-141">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="56980-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="56980-142">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="56980-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="56980-143">-Parameters</span><span class="sxs-lookup"><span data-stu-id="56980-143">-Parameters</span></span>
<span data-ttu-id="56980-144">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56980-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56980-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="56980-145">-Pre</span></span>
<span data-ttu-id="56980-146">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="56980-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="56980-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56980-147">-ResourceGroupName</span></span>
<span data-ttu-id="56980-148">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="56980-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="56980-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56980-149">-ResourceId</span></span>
<span data-ttu-id="56980-150">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="56980-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="56980-151">L'ID include l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="56980-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="56980-152">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="56980-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="56980-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56980-153">-ResourceName</span></span>
<span data-ttu-id="56980-154">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="56980-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="56980-155">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="56980-155">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="56980-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="56980-156">-ResourceType</span></span>
<span data-ttu-id="56980-157">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="56980-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="56980-158">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="56980-158">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="56980-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="56980-159">-TenantLevel</span></span>
<span data-ttu-id="56980-160">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="56980-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="56980-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56980-161">-Confirm</span></span>
<span data-ttu-id="56980-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56980-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56980-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56980-163">-WhatIf</span></span>
<span data-ttu-id="56980-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56980-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56980-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56980-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56980-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56980-166">CommonParameters</span></span>
<span data-ttu-id="56980-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56980-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56980-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56980-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56980-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56980-169">INPUTS</span></span>

### <span data-ttu-id="56980-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56980-170">None</span></span>
<span data-ttu-id="56980-171">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="56980-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56980-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56980-172">OUTPUTS</span></span>

### <span data-ttu-id="56980-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="56980-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="56980-174">Note</span><span class="sxs-lookup"><span data-stu-id="56980-174">NOTES</span></span>

## <span data-ttu-id="56980-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56980-175">RELATED LINKS</span></span>
