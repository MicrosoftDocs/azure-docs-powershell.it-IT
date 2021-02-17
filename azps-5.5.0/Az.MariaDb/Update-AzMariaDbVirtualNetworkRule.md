---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192238"
---
# <span data-ttu-id="b0794-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0794-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="b0794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0794-102">SYNOPSIS</span></span>
<span data-ttu-id="b0794-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="b0794-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b0794-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0794-104">SYNTAX</span></span>

### <span data-ttu-id="b0794-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0794-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b0794-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b0794-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b0794-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b0794-107">DESCRIPTION</span></span>
<span data-ttu-id="b0794-108">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="b0794-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="b0794-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0794-109">EXAMPLES</span></span>

### <span data-ttu-id="b0794-110">Esempio 1: Aggiornare la regola di rete virtuale MariaDB</span><span class="sxs-lookup"><span data-stu-id="b0794-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="b0794-111">Questo comando aggiorna una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0794-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="b0794-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0794-112">PARAMETERS</span></span>

### <span data-ttu-id="b0794-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0794-113">-AsJob</span></span>
<span data-ttu-id="b0794-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b0794-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b0794-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0794-115">-DefaultProfile</span></span>
<span data-ttu-id="b0794-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0794-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0794-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b0794-118">Creare una regola del firewall prima che la rete virtuale abbia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="b0794-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b0794-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0794-119">-InputObject</span></span>
<span data-ttu-id="b0794-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b0794-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b0794-121">-Name</span></span>
<span data-ttu-id="b0794-122">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0794-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b0794-123">-NoWait</span></span>
<span data-ttu-id="b0794-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b0794-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b0794-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0794-125">-PassThru</span></span>
<span data-ttu-id="b0794-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="b0794-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b0794-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0794-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0794-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0794-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b0794-129">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b0794-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0794-130">-ServerName</span></span>
<span data-ttu-id="b0794-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="b0794-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b0794-132">-SubnetId</span></span>
<span data-ttu-id="b0794-133">ID ARM della risorsa della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0794-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="b0794-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0794-134">-SubscriptionId</span></span>
<span data-ttu-id="b0794-135">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0794-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0794-136">-Confirm</span></span>
<span data-ttu-id="b0794-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0794-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0794-138">-WhatIf</span></span>
<span data-ttu-id="b0794-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0794-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0794-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0794-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0794-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0794-141">CommonParameters</span></span>
<span data-ttu-id="b0794-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0794-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0794-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0794-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0794-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="b0794-144">INPUTS</span></span>

### <span data-ttu-id="b0794-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="b0794-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b0794-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0794-146">OUTPUTS</span></span>

### <span data-ttu-id="b0794-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0794-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b0794-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b0794-148">NOTES</span></span>

<span data-ttu-id="b0794-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b0794-149">ALIASES</span></span>

<span data-ttu-id="b0794-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="b0794-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0794-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b0794-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0794-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b0794-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0794-153">INPUTOBJECT <IMariaDbIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="b0794-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0794-154">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="b0794-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b0794-155">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="b0794-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b0794-156">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="b0794-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b0794-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="b0794-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0794-158">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b0794-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b0794-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b0794-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b0794-160">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="b0794-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b0794-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b0794-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b0794-162">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="b0794-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b0794-163">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0794-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b0794-164">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b0794-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b0794-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0794-165">RELATED LINKS</span></span>

