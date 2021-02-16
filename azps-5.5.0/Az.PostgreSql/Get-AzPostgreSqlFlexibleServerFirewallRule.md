---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: a4b2f96644a2ec354b38dd13b159bb0f65f008c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179158"
---
# <span data-ttu-id="bd903-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd903-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="bd903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd903-102">SYNOPSIS</span></span>
<span data-ttu-id="bd903-103">Elencare tutte le regole del firewall in un determinato server.</span><span class="sxs-lookup"><span data-stu-id="bd903-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="bd903-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd903-104">SYNTAX</span></span>

### <span data-ttu-id="bd903-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd903-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd903-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bd903-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bd903-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd903-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd903-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd903-108">DESCRIPTION</span></span>
<span data-ttu-id="bd903-109">Elencare tutte le regole del firewall in un determinato server.</span><span class="sxs-lookup"><span data-stu-id="bd903-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="bd903-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd903-110">EXAMPLES</span></span>

### <span data-ttu-id="bd903-111">Esempio 1: Ottenere le regole del firewall in base al nome</span><span class="sxs-lookup"><span data-stu-id="bd903-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="bd903-112">Questo cmdlet ottiene le regole del firewall in base al nome.</span><span class="sxs-lookup"><span data-stu-id="bd903-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="bd903-113">Esempio 2: Ottenere le regole del firewall in base all'identità</span><span class="sxs-lookup"><span data-stu-id="bd903-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="bd903-114">Questo cmdlet ottiene le regole del firewall in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="bd903-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="bd903-115">Esempio 3: Elenca tutte le regole del firewall nel server PostgreSql specificato</span><span class="sxs-lookup"><span data-stu-id="bd903-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="bd903-116">Questo cmdlet elenca tutte le regole del firewall nel server PostgreSql specificato.</span><span class="sxs-lookup"><span data-stu-id="bd903-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="bd903-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd903-117">PARAMETERS</span></span>

### <span data-ttu-id="bd903-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd903-118">-DefaultProfile</span></span>
<span data-ttu-id="bd903-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd903-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd903-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd903-120">-InputObject</span></span>
<span data-ttu-id="bd903-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bd903-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd903-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bd903-122">-Name</span></span>
<span data-ttu-id="bd903-123">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="bd903-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="bd903-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd903-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd903-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd903-125">The name of the resource group.</span></span>
<span data-ttu-id="bd903-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bd903-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bd903-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd903-127">-ServerName</span></span>
<span data-ttu-id="bd903-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="bd903-128">The name of the server.</span></span>

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

### <span data-ttu-id="bd903-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd903-129">-SubscriptionId</span></span>
<span data-ttu-id="bd903-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bd903-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bd903-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd903-131">CommonParameters</span></span>
<span data-ttu-id="bd903-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd903-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd903-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd903-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd903-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd903-134">INPUTS</span></span>

### <span data-ttu-id="bd903-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bd903-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="bd903-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd903-136">OUTPUTS</span></span>

### <span data-ttu-id="bd903-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bd903-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="bd903-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd903-138">NOTES</span></span>

<span data-ttu-id="bd903-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bd903-139">ALIASES</span></span>

<span data-ttu-id="bd903-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bd903-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd903-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bd903-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd903-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bd903-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd903-143">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="bd903-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd903-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="bd903-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bd903-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="bd903-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bd903-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="bd903-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bd903-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="bd903-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd903-148">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="bd903-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bd903-149">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd903-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bd903-150">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bd903-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="bd903-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bd903-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bd903-152">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="bd903-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bd903-153">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bd903-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bd903-154">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bd903-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bd903-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd903-155">RELATED LINKS</span></span>

