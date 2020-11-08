---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192371"
---
# <span data-ttu-id="194ba-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="194ba-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="194ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="194ba-102">SYNOPSIS</span></span>
<span data-ttu-id="194ba-103">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="194ba-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="194ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="194ba-104">SYNTAX</span></span>

### <span data-ttu-id="194ba-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="194ba-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="194ba-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="194ba-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="194ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="194ba-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="194ba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194ba-108">DESCRIPTION</span></span>
<span data-ttu-id="194ba-109">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="194ba-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="194ba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="194ba-110">EXAMPLES</span></span>

### <span data-ttu-id="194ba-111">Esempio 1: elencare tutte le configurazioni in un server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="194ba-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="194ba-112">Questo cmdlet elenca tutte le configurazioni in un server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="194ba-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="194ba-113">Esempio 2: ottenere la configurazione MySql specificata per nome</span><span class="sxs-lookup"><span data-stu-id="194ba-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="194ba-114">Questo cmdlet ottiene la configurazione di MySql specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="194ba-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="194ba-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="194ba-115">PARAMETERS</span></span>

### <span data-ttu-id="194ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="194ba-116">-DefaultProfile</span></span>
<span data-ttu-id="194ba-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="194ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="194ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="194ba-118">-InputObject</span></span>
<span data-ttu-id="194ba-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="194ba-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="194ba-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="194ba-120">-Name</span></span>
<span data-ttu-id="194ba-121">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="194ba-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="194ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="194ba-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="194ba-123">The name of the resource group.</span></span>
<span data-ttu-id="194ba-124">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="194ba-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="194ba-125">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="194ba-125">-ServerName</span></span>
<span data-ttu-id="194ba-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="194ba-126">The name of the server.</span></span>

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

### <span data-ttu-id="194ba-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="194ba-127">-SubscriptionId</span></span>
<span data-ttu-id="194ba-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="194ba-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="194ba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194ba-129">CommonParameters</span></span>
<span data-ttu-id="194ba-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194ba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194ba-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="194ba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194ba-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="194ba-132">INPUTS</span></span>

### <span data-ttu-id="194ba-133">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="194ba-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="194ba-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="194ba-134">OUTPUTS</span></span>

### <span data-ttu-id="194ba-135">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="194ba-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="194ba-136">Note</span><span class="sxs-lookup"><span data-stu-id="194ba-136">NOTES</span></span>

<span data-ttu-id="194ba-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="194ba-137">ALIASES</span></span>

<span data-ttu-id="194ba-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="194ba-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="194ba-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="194ba-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="194ba-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="194ba-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="194ba-141">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="194ba-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="194ba-142">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="194ba-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="194ba-143">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="194ba-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="194ba-144">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="194ba-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="194ba-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="194ba-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="194ba-146">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="194ba-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="194ba-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="194ba-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="194ba-148">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="194ba-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="194ba-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="194ba-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="194ba-150">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="194ba-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="194ba-151">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="194ba-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="194ba-152">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="194ba-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="194ba-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="194ba-153">RELATED LINKS</span></span>

