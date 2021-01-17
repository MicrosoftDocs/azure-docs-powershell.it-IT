---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378475"
---
# <span data-ttu-id="06d2b-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06d2b-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="06d2b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="06d2b-103">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="06d2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06d2b-104">SYNTAX</span></span>

### <span data-ttu-id="06d2b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="06d2b-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06d2b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="06d2b-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="06d2b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06d2b-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d2b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06d2b-108">DESCRIPTION</span></span>
<span data-ttu-id="06d2b-109">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="06d2b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06d2b-110">EXAMPLES</span></span>

### <span data-ttu-id="06d2b-111">Esempio 1: elenca tutte le regole del firewall nel server PostgreSql specificato</span><span class="sxs-lookup"><span data-stu-id="06d2b-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="06d2b-112">Questo cmdlet elenca tutta la regola del firewall nel server PostgreSql specificato.</span><span class="sxs-lookup"><span data-stu-id="06d2b-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="06d2b-113">Esempio 2: ottenere la regola del firewall per nome</span><span class="sxs-lookup"><span data-stu-id="06d2b-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="06d2b-114">Questo cmdlet ottiene la regola del firewall per nome.</span><span class="sxs-lookup"><span data-stu-id="06d2b-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="06d2b-115">Esempio 3: ottenere la regola del firewall per identità</span><span class="sxs-lookup"><span data-stu-id="06d2b-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="06d2b-116">Questo cmdlet ottiene la regola del firewall per identità.</span><span class="sxs-lookup"><span data-stu-id="06d2b-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="06d2b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06d2b-117">PARAMETERS</span></span>

### <span data-ttu-id="06d2b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d2b-118">-DefaultProfile</span></span>
<span data-ttu-id="06d2b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06d2b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d2b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d2b-120">-InputObject</span></span>
<span data-ttu-id="06d2b-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="06d2b-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="06d2b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="06d2b-122">-Name</span></span>
<span data-ttu-id="06d2b-123">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="06d2b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d2b-124">-ResourceGroupName</span></span>
<span data-ttu-id="06d2b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06d2b-125">The name of the resource group.</span></span>
<span data-ttu-id="06d2b-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="06d2b-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="06d2b-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="06d2b-127">-ServerName</span></span>
<span data-ttu-id="06d2b-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-128">The name of the server.</span></span>

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

### <span data-ttu-id="06d2b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06d2b-129">-SubscriptionId</span></span>
<span data-ttu-id="06d2b-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="06d2b-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="06d2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d2b-131">CommonParameters</span></span>
<span data-ttu-id="06d2b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d2b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d2b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d2b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06d2b-134">INPUTS</span></span>

### <span data-ttu-id="06d2b-135">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="06d2b-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="06d2b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06d2b-136">OUTPUTS</span></span>

### <span data-ttu-id="06d2b-137">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06d2b-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="06d2b-138">Note</span><span class="sxs-lookup"><span data-stu-id="06d2b-138">NOTES</span></span>

<span data-ttu-id="06d2b-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="06d2b-139">ALIASES</span></span>

<span data-ttu-id="06d2b-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06d2b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06d2b-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="06d2b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06d2b-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06d2b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06d2b-143">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="06d2b-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06d2b-144">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="06d2b-145">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="06d2b-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="06d2b-146">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="06d2b-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="06d2b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06d2b-148">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="06d2b-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="06d2b-149">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="06d2b-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="06d2b-150">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="06d2b-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="06d2b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="06d2b-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="06d2b-152">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="06d2b-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="06d2b-153">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="06d2b-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="06d2b-154">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="06d2b-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="06d2b-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06d2b-155">RELATED LINKS</span></span>

