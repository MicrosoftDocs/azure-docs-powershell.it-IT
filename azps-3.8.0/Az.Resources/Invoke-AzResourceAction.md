---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021734"
---
# <span data-ttu-id="6d69b-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="6d69b-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="6d69b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d69b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d69b-103">Richiama un'azione su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d69b-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="6d69b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d69b-104">SYNTAX</span></span>

### <span data-ttu-id="6d69b-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d69b-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d69b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6d69b-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d69b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6d69b-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d69b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d69b-108">DESCRIPTION</span></span>
<span data-ttu-id="6d69b-109">Il cmdlet **Invoke-AzResourceAction** richiama un'azione su una risorsa Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="6d69b-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="6d69b-110">Per ottenere un elenco di azioni supportate, usare lo strumento Esplora risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d69b-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="6d69b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d69b-111">EXAMPLES</span></span>

### <span data-ttu-id="6d69b-112">Esempio 1: richiamare l'avvio di una VM con ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d69b-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="6d69b-113">Questo comando avvia la macchina virtuale con {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="6d69b-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="6d69b-114">Esempio 2: richiamare poweroffing una VM con resourceName</span><span class="sxs-lookup"><span data-stu-id="6d69b-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="6d69b-115">Questo comando Arresta la macchina virtuale con {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="6d69b-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="6d69b-116">Il comando specifica il parametro *Force* , quindi non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6d69b-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6d69b-117">Esempio 3: richiamare la registrazione di un provider di risorse con ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d69b-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="6d69b-118">Questo comando registra un provider di risorse "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="6d69b-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="6d69b-119">Il comando specifica il parametro *Force* , quindi non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6d69b-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6d69b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d69b-120">PARAMETERS</span></span>

### <span data-ttu-id="6d69b-121">-Azione</span><span class="sxs-lookup"><span data-stu-id="6d69b-121">-Action</span></span>
<span data-ttu-id="6d69b-122">Specifica il nome dell'azione da richiamare.</span><span class="sxs-lookup"><span data-stu-id="6d69b-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="6d69b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d69b-123">-ApiVersion</span></span>
<span data-ttu-id="6d69b-124">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="6d69b-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d69b-125">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6d69b-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6d69b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d69b-126">-DefaultProfile</span></span>
<span data-ttu-id="6d69b-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d69b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d69b-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6d69b-128">-ExtensionResourceName</span></span>
<span data-ttu-id="6d69b-129">Specifica il nome di una risorsa di estensione per la risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="6d69b-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6d69b-130">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="6d69b-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="6d69b-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6d69b-131">-ExtensionResourceType</span></span>
<span data-ttu-id="6d69b-132">Specifica il tipo della risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="6d69b-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="6d69b-133">Ad esempio: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6d69b-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6d69b-134">-Force</span><span class="sxs-lookup"><span data-stu-id="6d69b-134">-Force</span></span>
<span data-ttu-id="6d69b-135">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6d69b-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d69b-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6d69b-136">-ODataQuery</span></span>
<span data-ttu-id="6d69b-137">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="6d69b-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6d69b-138">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="6d69b-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6d69b-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="6d69b-139">-Parameters</span></span>
<span data-ttu-id="6d69b-140">Specifica i parametri, come tabella hash, per l'azione richiamata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d69b-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="6d69b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="6d69b-141">-Pre</span></span>
<span data-ttu-id="6d69b-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6d69b-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6d69b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d69b-143">-ResourceGroupName</span></span>
<span data-ttu-id="6d69b-144">Specifica il nome di un gruppo di risorse in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="6d69b-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="6d69b-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d69b-145">-ResourceId</span></span>
<span data-ttu-id="6d69b-146">Specifica l'ID di risorsa completo della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="6d69b-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6d69b-147">L'ID include l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6d69b-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6d69b-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6d69b-148">-ResourceName</span></span>
<span data-ttu-id="6d69b-149">Specifica il nome della risorsa della risorsa in cui questo cmdlet richiama un'azione.</span><span class="sxs-lookup"><span data-stu-id="6d69b-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6d69b-150">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6d69b-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6d69b-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6d69b-151">-ResourceType</span></span>
<span data-ttu-id="6d69b-152">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6d69b-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="6d69b-153">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6d69b-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6d69b-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6d69b-154">-TenantLevel</span></span>
<span data-ttu-id="6d69b-155">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="6d69b-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6d69b-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d69b-156">-Confirm</span></span>
<span data-ttu-id="6d69b-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d69b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d69b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d69b-158">-WhatIf</span></span>
<span data-ttu-id="6d69b-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d69b-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d69b-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d69b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d69b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d69b-161">CommonParameters</span></span>
<span data-ttu-id="6d69b-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d69b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d69b-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d69b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d69b-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d69b-164">INPUTS</span></span>

### <span data-ttu-id="6d69b-165">System. String</span><span class="sxs-lookup"><span data-stu-id="6d69b-165">System.String</span></span>

## <span data-ttu-id="6d69b-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d69b-166">OUTPUTS</span></span>

### <span data-ttu-id="6d69b-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6d69b-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6d69b-168">Note</span><span class="sxs-lookup"><span data-stu-id="6d69b-168">NOTES</span></span>

## <span data-ttu-id="6d69b-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d69b-169">RELATED LINKS</span></span>
