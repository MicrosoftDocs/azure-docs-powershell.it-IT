---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190046"
---
# <span data-ttu-id="cfeda-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cfeda-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="cfeda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfeda-102">SYNOPSIS</span></span>
<span data-ttu-id="cfeda-103">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="cfeda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfeda-104">SYNTAX</span></span>

### <span data-ttu-id="cfeda-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfeda-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cfeda-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cfeda-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cfeda-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cfeda-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfeda-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfeda-108">DESCRIPTION</span></span>
<span data-ttu-id="cfeda-109">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="cfeda-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfeda-110">EXAMPLES</span></span>

### <span data-ttu-id="cfeda-111">Esempio 1: Ottenere le regole del firewall in base al nome</span><span class="sxs-lookup"><span data-stu-id="cfeda-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="cfeda-112">Questo cmdlet ottiene le regole del firewall in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cfeda-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="cfeda-113">Esempio 2: Ottenere le regole del firewall in base all'identità</span><span class="sxs-lookup"><span data-stu-id="cfeda-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="cfeda-114">Questo cmdlet ottiene le regole del firewall in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="cfeda-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="cfeda-115">Esempio 3: Elenca tutte le regole del firewall nel server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="cfeda-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="cfeda-116">Questo cmdlet elenca tutte le regole del firewall nel server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="cfeda-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="cfeda-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfeda-117">PARAMETERS</span></span>

### <span data-ttu-id="cfeda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfeda-118">-DefaultProfile</span></span>
<span data-ttu-id="cfeda-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfeda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfeda-120">-InputObject</span></span>
<span data-ttu-id="cfeda-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cfeda-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfeda-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cfeda-122">-Name</span></span>
<span data-ttu-id="cfeda-123">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfeda-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfeda-124">-ResourceGroupName</span></span>
<span data-ttu-id="cfeda-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfeda-125">The name of the resource group.</span></span>
<span data-ttu-id="cfeda-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cfeda-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfeda-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cfeda-127">-ServerName</span></span>
<span data-ttu-id="cfeda-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfeda-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cfeda-129">-SubscriptionId</span></span>
<span data-ttu-id="cfeda-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfeda-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfeda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfeda-131">CommonParameters</span></span>
<span data-ttu-id="cfeda-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfeda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfeda-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cfeda-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfeda-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfeda-134">INPUTS</span></span>

### <span data-ttu-id="cfeda-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cfeda-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cfeda-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfeda-136">OUTPUTS</span></span>

### <span data-ttu-id="cfeda-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="cfeda-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="cfeda-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfeda-138">NOTES</span></span>

<span data-ttu-id="cfeda-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cfeda-139">ALIASES</span></span>

<span data-ttu-id="cfeda-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cfeda-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cfeda-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cfeda-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cfeda-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cfeda-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cfeda-143">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="cfeda-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cfeda-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cfeda-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="cfeda-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cfeda-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cfeda-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cfeda-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cfeda-148">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cfeda-149">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="cfeda-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cfeda-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cfeda-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cfeda-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cfeda-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="cfeda-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cfeda-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cfeda-153">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="cfeda-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cfeda-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfeda-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cfeda-155">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cfeda-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cfeda-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfeda-156">RELATED LINKS</span></span>

