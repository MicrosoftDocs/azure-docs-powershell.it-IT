---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186638"
---
# <span data-ttu-id="2ebfe-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ebfe-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="2ebfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ebfe-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebfe-103">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="2ebfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ebfe-104">SYNTAX</span></span>

### <span data-ttu-id="2ebfe-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ebfe-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ebfe-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="2ebfe-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ebfe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2ebfe-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ebfe-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ebfe-108">DESCRIPTION</span></span>
<span data-ttu-id="2ebfe-109">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="2ebfe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ebfe-110">EXAMPLES</span></span>

### <span data-ttu-id="2ebfe-111">Esempio 1: Elencare tutte le configurazioni nel server PostgreSql</span><span class="sxs-lookup"><span data-stu-id="2ebfe-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="2ebfe-112">Questo cmdlet elenca tutte le configurazioni nel server PostgreSql specificato.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="2ebfe-113">Esempio 2: Ottenere la configurazione PostgreSql specificata in base al nome</span><span class="sxs-lookup"><span data-stu-id="2ebfe-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="2ebfe-114">Questo cmdlet viene specificato per nome per la configurazione PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="2ebfe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ebfe-115">PARAMETERS</span></span>

### <span data-ttu-id="2ebfe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebfe-116">-DefaultProfile</span></span>
<span data-ttu-id="2ebfe-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ebfe-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ebfe-118">-InputObject</span></span>
<span data-ttu-id="2ebfe-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2ebfe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2ebfe-120">-Name</span></span>
<span data-ttu-id="2ebfe-121">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebfe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebfe-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ebfe-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-123">The name of the resource group.</span></span>
<span data-ttu-id="2ebfe-124">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ebfe-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ebfe-125">-ServerName</span></span>
<span data-ttu-id="2ebfe-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-126">The name of the server.</span></span>

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

### <span data-ttu-id="2ebfe-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ebfe-127">-SubscriptionId</span></span>
<span data-ttu-id="2ebfe-128">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ebfe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebfe-129">CommonParameters</span></span>
<span data-ttu-id="2ebfe-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebfe-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebfe-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ebfe-132">INPUTS</span></span>

### <span data-ttu-id="2ebfe-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2ebfe-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="2ebfe-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ebfe-134">OUTPUTS</span></span>

### <span data-ttu-id="2ebfe-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ebfe-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="2ebfe-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ebfe-136">NOTES</span></span>

<span data-ttu-id="2ebfe-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2ebfe-137">ALIASES</span></span>

<span data-ttu-id="2ebfe-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2ebfe-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2ebfe-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ebfe-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2ebfe-141">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2ebfe-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2ebfe-142">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2ebfe-143">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2ebfe-144">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2ebfe-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2ebfe-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2ebfe-146">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2ebfe-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2ebfe-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="2ebfe-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2ebfe-150">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2ebfe-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2ebfe-152">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2ebfe-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2ebfe-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ebfe-153">RELATED LINKS</span></span>

