---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359015"
---
# <span data-ttu-id="5f986-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f986-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="5f986-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f986-102">SYNOPSIS</span></span>
<span data-ttu-id="5f986-103">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="5f986-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5f986-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f986-104">SYNTAX</span></span>

### <span data-ttu-id="5f986-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f986-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f986-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="5f986-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f986-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5f986-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f986-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f986-108">DESCRIPTION</span></span>
<span data-ttu-id="5f986-109">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="5f986-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5f986-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f986-110">EXAMPLES</span></span>

### <span data-ttu-id="5f986-111">Esempio 1: elencare tutte le configurazioni in un server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="5f986-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="5f986-112">Questo cmdlet elenca tutte le configurazioni in un server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="5f986-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="5f986-113">Esempio 2: ottenere la configurazione MySql specificata per nome</span><span class="sxs-lookup"><span data-stu-id="5f986-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="5f986-114">Questo cmdlet ottiene la configurazione di MySql specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="5f986-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="5f986-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f986-115">PARAMETERS</span></span>

### <span data-ttu-id="5f986-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f986-116">-DefaultProfile</span></span>
<span data-ttu-id="5f986-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f986-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f986-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f986-118">-InputObject</span></span>
<span data-ttu-id="5f986-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5f986-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f986-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f986-120">-Name</span></span>
<span data-ttu-id="5f986-121">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="5f986-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f986-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f986-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f986-123">The name of the resource group.</span></span>
<span data-ttu-id="5f986-124">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5f986-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f986-125">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5f986-125">-ServerName</span></span>
<span data-ttu-id="5f986-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-126">The name of the server.</span></span>

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

### <span data-ttu-id="5f986-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f986-127">-SubscriptionId</span></span>
<span data-ttu-id="5f986-128">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f986-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5f986-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f986-129">CommonParameters</span></span>
<span data-ttu-id="5f986-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f986-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f986-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f986-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f986-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f986-132">INPUTS</span></span>

### <span data-ttu-id="5f986-133">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5f986-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5f986-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f986-134">OUTPUTS</span></span>

### <span data-ttu-id="5f986-135">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f986-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="5f986-136">Note</span><span class="sxs-lookup"><span data-stu-id="5f986-136">NOTES</span></span>

<span data-ttu-id="5f986-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5f986-137">ALIASES</span></span>

<span data-ttu-id="5f986-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f986-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f986-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5f986-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f986-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f986-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f986-141">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5f986-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f986-142">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5f986-143">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="5f986-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5f986-144">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5f986-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="5f986-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f986-146">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5f986-147">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="5f986-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5f986-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f986-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f986-149">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5f986-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f986-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5f986-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5f986-151">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="5f986-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5f986-152">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f986-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f986-153">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f986-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5f986-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f986-154">RELATED LINKS</span></span>

