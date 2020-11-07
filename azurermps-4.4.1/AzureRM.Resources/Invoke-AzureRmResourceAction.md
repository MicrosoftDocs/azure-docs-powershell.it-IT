---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685659"
---
# <span data-ttu-id="cc9a1-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="cc9a1-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="cc9a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9a1-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc9a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc9a1-104">SYNTAX</span></span>

### <span data-ttu-id="cc9a1-105">ID risorsa (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cc9a1-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc9a1-106">Risorsa che risiede a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc9a1-107">Risorsa che risiede a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc9a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc9a1-108">DESCRIPTION</span></span>
<span data-ttu-id="cc9a1-109">Il cmdlet **Invoke-AzureRmResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="cc9a1-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="cc9a1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc9a1-111">EXAMPLES</span></span>

## <span data-ttu-id="cc9a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc9a1-112">PARAMETERS</span></span>

### <span data-ttu-id="cc9a1-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="cc9a1-113">-Action</span></span>
<span data-ttu-id="cc9a1-114">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="cc9a1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cc9a1-115">-ApiVersion</span></span>
<span data-ttu-id="cc9a1-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cc9a1-117">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="cc9a1-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="cc9a1-118">-ExtensionResourceName</span></span>
<span data-ttu-id="cc9a1-119">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="cc9a1-120">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="cc9a1-121">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="cc9a1-121">server name`/`database name</span></span>

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

### <span data-ttu-id="cc9a1-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="cc9a1-122">-ExtensionResourceType</span></span>
<span data-ttu-id="cc9a1-123">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="cc9a1-124">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-124">For instance:</span></span> 

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

### <span data-ttu-id="cc9a1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cc9a1-125">-Force</span></span>
<span data-ttu-id="cc9a1-126">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc9a1-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cc9a1-127">-InformationAction</span></span>
<span data-ttu-id="cc9a1-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc9a1-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc9a1-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="cc9a1-130">Continue</span></span>
- <span data-ttu-id="cc9a1-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="cc9a1-131">Ignore</span></span>
- <span data-ttu-id="cc9a1-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="cc9a1-132">Inquire</span></span>
- <span data-ttu-id="cc9a1-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cc9a1-133">SilentlyContinue</span></span>
- <span data-ttu-id="cc9a1-134">Stop</span><span class="sxs-lookup"><span data-stu-id="cc9a1-134">Stop</span></span>
- <span data-ttu-id="cc9a1-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="cc9a1-135">Suspend</span></span>

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

### <span data-ttu-id="cc9a1-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cc9a1-136">-InformationVariable</span></span>
<span data-ttu-id="cc9a1-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cc9a1-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="cc9a1-138">-ODataQuery</span></span>
<span data-ttu-id="cc9a1-139">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="cc9a1-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="cc9a1-140">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="cc9a1-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="cc9a1-141">-Parameters</span></span>
<span data-ttu-id="cc9a1-142">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="cc9a1-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="cc9a1-143">-Pre</span></span>
<span data-ttu-id="cc9a1-144">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cc9a1-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9a1-145">-ResourceGroupName</span></span>
<span data-ttu-id="cc9a1-146">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="cc9a1-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc9a1-147">-ResourceId</span></span>
<span data-ttu-id="cc9a1-148">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="cc9a1-149">L'ID include l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="cc9a1-150">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="cc9a1-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="cc9a1-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cc9a1-151">-ResourceName</span></span>
<span data-ttu-id="cc9a1-152">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="cc9a1-153">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-153">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="cc9a1-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cc9a1-154">-ResourceType</span></span>
<span data-ttu-id="cc9a1-155">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="cc9a1-156">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="cc9a1-156">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="cc9a1-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="cc9a1-157">-TenantLevel</span></span>
<span data-ttu-id="cc9a1-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="cc9a1-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cc9a1-159">-Confirm</span></span>
<span data-ttu-id="cc9a1-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc9a1-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc9a1-161">-WhatIf</span></span>
<span data-ttu-id="cc9a1-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc9a1-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc9a1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9a1-164">-DefaultProfile</span></span>
<span data-ttu-id="cc9a1-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc9a1-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9a1-166">CommonParameters</span></span>
<span data-ttu-id="cc9a1-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc9a1-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9a1-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc9a1-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9a1-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc9a1-169">INPUTS</span></span>

## <span data-ttu-id="cc9a1-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc9a1-170">OUTPUTS</span></span>

### <span data-ttu-id="cc9a1-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cc9a1-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cc9a1-172">Note</span><span class="sxs-lookup"><span data-stu-id="cc9a1-172">NOTES</span></span>

## <span data-ttu-id="cc9a1-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc9a1-173">RELATED LINKS</span></span>

