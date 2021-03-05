---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 572943ea0f694b5a3a68ff4c1c030a1a3a1fc0f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968734"
---
# <span data-ttu-id="43090-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="43090-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="43090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43090-102">SYNOPSIS</span></span>
<span data-ttu-id="43090-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="43090-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="43090-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43090-104">SYNTAX</span></span>

### <span data-ttu-id="43090-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43090-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43090-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43090-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43090-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43090-107">DESCRIPTION</span></span>
<span data-ttu-id="43090-108">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="43090-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="43090-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43090-109">EXAMPLES</span></span>

### <span data-ttu-id="43090-110">Esempio 1: Aggiornare la regola di rete virtuale MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="43090-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="43090-111">Questo cmdlet aggiorna la regola della rete virtuale MySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="43090-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="43090-112">Esempio 2: Aggiornare la regola della rete virtuale MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="43090-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="43090-113">Questi cmdlet aggiornano la regola della rete virtuale MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="43090-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="43090-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43090-114">PARAMETERS</span></span>

### <span data-ttu-id="43090-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43090-115">-AsJob</span></span>
<span data-ttu-id="43090-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="43090-116">Run the command as a job</span></span>

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

### <span data-ttu-id="43090-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43090-117">-DefaultProfile</span></span>
<span data-ttu-id="43090-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43090-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43090-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="43090-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="43090-120">Creare una regola del firewall prima che per la rete virtuale sia abilitato l'endpoint del servizio vnet.</span><span class="sxs-lookup"><span data-stu-id="43090-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="43090-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43090-121">-InputObject</span></span>
<span data-ttu-id="43090-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43090-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43090-123">-Name</span><span class="sxs-lookup"><span data-stu-id="43090-123">-Name</span></span>
<span data-ttu-id="43090-124">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="43090-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="43090-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="43090-125">-NoWait</span></span>
<span data-ttu-id="43090-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="43090-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="43090-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43090-127">-PassThru</span></span>
<span data-ttu-id="43090-128">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="43090-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="43090-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43090-129">-ResourceGroupName</span></span>
<span data-ttu-id="43090-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43090-130">The name of the resource group.</span></span>
<span data-ttu-id="43090-131">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="43090-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43090-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43090-132">-ServerName</span></span>
<span data-ttu-id="43090-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="43090-133">The name of the server.</span></span>

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

### <span data-ttu-id="43090-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="43090-134">-SubnetId</span></span>
<span data-ttu-id="43090-135">ID ARM della risorsa della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="43090-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43090-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43090-136">-SubscriptionId</span></span>
<span data-ttu-id="43090-137">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43090-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43090-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43090-138">-Confirm</span></span>
<span data-ttu-id="43090-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43090-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43090-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43090-140">-WhatIf</span></span>
<span data-ttu-id="43090-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43090-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43090-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43090-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43090-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43090-143">CommonParameters</span></span>
<span data-ttu-id="43090-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43090-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43090-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43090-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43090-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="43090-146">INPUTS</span></span>

### <span data-ttu-id="43090-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="43090-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="43090-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43090-148">OUTPUTS</span></span>

### <span data-ttu-id="43090-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="43090-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="43090-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="43090-150">NOTES</span></span>

<span data-ttu-id="43090-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43090-151">ALIASES</span></span>

<span data-ttu-id="43090-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="43090-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43090-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="43090-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43090-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43090-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43090-155">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="43090-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43090-156">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="43090-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="43090-157">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="43090-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="43090-158">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="43090-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="43090-159">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="43090-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43090-160">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="43090-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="43090-161">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="43090-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="43090-162">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43090-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43090-163">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="43090-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="43090-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="43090-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="43090-165">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="43090-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="43090-166">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43090-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="43090-167">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="43090-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="43090-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43090-168">RELATED LINKS</span></span>

