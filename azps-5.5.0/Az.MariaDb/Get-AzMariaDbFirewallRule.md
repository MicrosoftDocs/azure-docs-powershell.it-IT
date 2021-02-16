---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190254"
---
# <span data-ttu-id="81084-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81084-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="81084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81084-102">SYNOPSIS</span></span>
<span data-ttu-id="81084-103">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="81084-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="81084-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81084-104">SYNTAX</span></span>

### <span data-ttu-id="81084-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81084-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81084-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="81084-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81084-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81084-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81084-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="81084-108">DESCRIPTION</span></span>
<span data-ttu-id="81084-109">Ottiene informazioni su una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="81084-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="81084-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81084-110">EXAMPLES</span></span>

### <span data-ttu-id="81084-111">Esempio 1: Elencare tutte le regole del firewall in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="81084-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="81084-112">Questo comando elenca tutte le regole del girewall in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="81084-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="81084-113">Esempio 2: Ottenere una regola del firewall in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="81084-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="81084-114">Questo comando ottiene una regola del firewall in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="81084-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="81084-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81084-115">PARAMETERS</span></span>

### <span data-ttu-id="81084-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81084-116">-DefaultProfile</span></span>
<span data-ttu-id="81084-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81084-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81084-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81084-118">-InputObject</span></span>
<span data-ttu-id="81084-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="81084-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81084-120">-Name</span><span class="sxs-lookup"><span data-stu-id="81084-120">-Name</span></span>
<span data-ttu-id="81084-121">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="81084-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="81084-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81084-122">-ResourceGroupName</span></span>
<span data-ttu-id="81084-123">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="81084-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="81084-124">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="81084-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="81084-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81084-125">-ServerName</span></span>
<span data-ttu-id="81084-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="81084-126">The name of the server.</span></span>

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

### <span data-ttu-id="81084-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81084-127">-SubscriptionId</span></span>
<span data-ttu-id="81084-128">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="81084-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="81084-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81084-129">CommonParameters</span></span>
<span data-ttu-id="81084-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81084-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81084-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81084-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81084-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="81084-132">INPUTS</span></span>

### <span data-ttu-id="81084-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="81084-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="81084-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81084-134">OUTPUTS</span></span>

### <span data-ttu-id="81084-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="81084-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="81084-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="81084-136">NOTES</span></span>

<span data-ttu-id="81084-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="81084-137">ALIASES</span></span>

<span data-ttu-id="81084-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="81084-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81084-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="81084-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81084-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81084-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81084-141">INPUTOBJECT <IMariaDbIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="81084-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81084-142">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="81084-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81084-143">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="81084-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81084-144">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="81084-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81084-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="81084-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81084-146">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="81084-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81084-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="81084-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="81084-148">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="81084-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="81084-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="81084-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81084-150">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="81084-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81084-151">`[SubscriptionId <String>]`: ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="81084-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="81084-152">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="81084-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81084-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81084-153">RELATED LINKS</span></span>

