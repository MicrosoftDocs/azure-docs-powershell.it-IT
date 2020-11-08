---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200036"
---
# <span data-ttu-id="39385-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39385-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="39385-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39385-102">SYNOPSIS</span></span>
<span data-ttu-id="39385-103">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="39385-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="39385-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39385-104">SYNTAX</span></span>

### <span data-ttu-id="39385-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39385-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39385-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="39385-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39385-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39385-107">DESCRIPTION</span></span>
<span data-ttu-id="39385-108">Crea o aggiorna una regola di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="39385-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="39385-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39385-109">EXAMPLES</span></span>

### <span data-ttu-id="39385-110">Esempio 1: aggiornare la regola di rete virtuale MySql per nome</span><span class="sxs-lookup"><span data-stu-id="39385-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="39385-111">Questo cmdlet aggiorna la regola di rete virtuale MySql per nome.</span><span class="sxs-lookup"><span data-stu-id="39385-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="39385-112">Esempio 2: aggiornare la regola della rete virtuale MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="39385-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="39385-113">Questi cmdlet aggiornano la regola della rete virtuale MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="39385-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="39385-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39385-114">PARAMETERS</span></span>

### <span data-ttu-id="39385-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39385-115">-AsJob</span></span>
<span data-ttu-id="39385-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="39385-116">Run the command as a job</span></span>

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

### <span data-ttu-id="39385-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39385-117">-DefaultProfile</span></span>
<span data-ttu-id="39385-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39385-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39385-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="39385-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="39385-120">Creare una regola del firewall prima che la rete virtuale abbia l'endpoint del servizio VNET abilitato.</span><span class="sxs-lookup"><span data-stu-id="39385-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="39385-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39385-121">-InputObject</span></span>
<span data-ttu-id="39385-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="39385-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39385-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="39385-123">-Name</span></span>
<span data-ttu-id="39385-124">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39385-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="39385-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="39385-125">-NoWait</span></span>
<span data-ttu-id="39385-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="39385-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39385-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39385-127">-PassThru</span></span>
<span data-ttu-id="39385-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="39385-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39385-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39385-129">-ResourceGroupName</span></span>
<span data-ttu-id="39385-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39385-130">The name of the resource group.</span></span>
<span data-ttu-id="39385-131">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39385-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39385-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="39385-132">-ServerName</span></span>
<span data-ttu-id="39385-133">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="39385-133">The name of the server.</span></span>

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

### <span data-ttu-id="39385-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="39385-134">-SubnetId</span></span>
<span data-ttu-id="39385-135">ID risorsa ARM della subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39385-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="39385-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39385-136">-SubscriptionId</span></span>
<span data-ttu-id="39385-137">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39385-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39385-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39385-138">-Confirm</span></span>
<span data-ttu-id="39385-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39385-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39385-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39385-140">-WhatIf</span></span>
<span data-ttu-id="39385-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39385-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39385-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39385-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39385-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39385-143">CommonParameters</span></span>
<span data-ttu-id="39385-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39385-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39385-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39385-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39385-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39385-146">INPUTS</span></span>

### <span data-ttu-id="39385-147">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="39385-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="39385-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39385-148">OUTPUTS</span></span>

### <span data-ttu-id="39385-149">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39385-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="39385-150">Note</span><span class="sxs-lookup"><span data-stu-id="39385-150">NOTES</span></span>

<span data-ttu-id="39385-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39385-151">ALIASES</span></span>

<span data-ttu-id="39385-152">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39385-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39385-153">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="39385-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39385-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39385-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39385-155">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="39385-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39385-156">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="39385-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="39385-157">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="39385-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="39385-158">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="39385-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="39385-159">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="39385-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39385-160">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="39385-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="39385-161">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39385-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39385-162">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39385-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="39385-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="39385-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="39385-164">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="39385-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="39385-165">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39385-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="39385-166">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39385-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="39385-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39385-167">RELATED LINKS</span></span>
