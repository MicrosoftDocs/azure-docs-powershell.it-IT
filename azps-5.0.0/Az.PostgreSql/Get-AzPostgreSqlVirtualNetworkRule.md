---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202644"
---
# <span data-ttu-id="db0a5-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="db0a5-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="db0a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="db0a5-103">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db0a5-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="db0a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db0a5-104">SYNTAX</span></span>

### <span data-ttu-id="db0a5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db0a5-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="db0a5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="db0a5-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="db0a5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="db0a5-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="db0a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db0a5-108">DESCRIPTION</span></span>
<span data-ttu-id="db0a5-109">Ottiene una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db0a5-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="db0a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db0a5-110">EXAMPLES</span></span>

### <span data-ttu-id="db0a5-111">Esempio 1: elenca tutte le regole di rete virtuale nel server PostgreSql specificato</span><span class="sxs-lookup"><span data-stu-id="db0a5-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="db0a5-112">Questo cmdlet elenca tutte le regole di rete virtuale nel server PostgreSql specificato.</span><span class="sxs-lookup"><span data-stu-id="db0a5-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="db0a5-113">Esempio 2: ottenere la regola di rete virtuale per nome</span><span class="sxs-lookup"><span data-stu-id="db0a5-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="db0a5-114">Questo cmdlet ottiene la regola di rete virtuale per nome.</span><span class="sxs-lookup"><span data-stu-id="db0a5-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="db0a5-115">Esempio 3: ottenere la regola di rete virtuale per identità</span><span class="sxs-lookup"><span data-stu-id="db0a5-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="db0a5-116">Questo cmdlet ottiene la regola di rete virtuale per identità.</span><span class="sxs-lookup"><span data-stu-id="db0a5-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="db0a5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db0a5-117">PARAMETERS</span></span>

### <span data-ttu-id="db0a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0a5-118">-DefaultProfile</span></span>
<span data-ttu-id="db0a5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db0a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0a5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db0a5-120">-InputObject</span></span>
<span data-ttu-id="db0a5-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="db0a5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db0a5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="db0a5-122">-Name</span></span>
<span data-ttu-id="db0a5-123">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db0a5-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0a5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db0a5-124">-PassThru</span></span>
<span data-ttu-id="db0a5-125">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="db0a5-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="db0a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db0a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="db0a5-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db0a5-127">The name of the resource group.</span></span>
<span data-ttu-id="db0a5-128">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="db0a5-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="db0a5-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="db0a5-129">-ServerName</span></span>
<span data-ttu-id="db0a5-130">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="db0a5-130">The name of the server.</span></span>

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

### <span data-ttu-id="db0a5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db0a5-131">-SubscriptionId</span></span>
<span data-ttu-id="db0a5-132">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="db0a5-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="db0a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0a5-133">CommonParameters</span></span>
<span data-ttu-id="db0a5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0a5-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db0a5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0a5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db0a5-136">INPUTS</span></span>

### <span data-ttu-id="db0a5-137">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="db0a5-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="db0a5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db0a5-138">OUTPUTS</span></span>

### <span data-ttu-id="db0a5-139">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="db0a5-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="db0a5-140">Note</span><span class="sxs-lookup"><span data-stu-id="db0a5-140">NOTES</span></span>

<span data-ttu-id="db0a5-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="db0a5-141">ALIASES</span></span>

<span data-ttu-id="db0a5-142">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db0a5-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db0a5-143">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="db0a5-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db0a5-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db0a5-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db0a5-145">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="db0a5-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db0a5-146">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="db0a5-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="db0a5-147">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="db0a5-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="db0a5-148">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="db0a5-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="db0a5-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="db0a5-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db0a5-150">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="db0a5-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="db0a5-151">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db0a5-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="db0a5-152">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="db0a5-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="db0a5-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="db0a5-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="db0a5-154">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="db0a5-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="db0a5-155">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="db0a5-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="db0a5-156">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db0a5-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="db0a5-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db0a5-157">RELATED LINKS</span></span>

