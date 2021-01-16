---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330256"
---
# <span data-ttu-id="d7b53-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7b53-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="d7b53-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7b53-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b53-103">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d7b53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7b53-104">SYNTAX</span></span>

### <span data-ttu-id="d7b53-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7b53-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7b53-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d7b53-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7b53-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7b53-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7b53-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7b53-108">DESCRIPTION</span></span>
<span data-ttu-id="d7b53-109">Ottiene informazioni su una configurazione di server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="d7b53-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7b53-110">EXAMPLES</span></span>

### <span data-ttu-id="d7b53-111">Esempio 1: elencare tutte le configurazioni in un server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="d7b53-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="d7b53-112">Questo cmdlet elenca tutte le configurazioni in un server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="d7b53-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="d7b53-113">Esempio 2: ottenere la configurazione MySql specificata per nome</span><span class="sxs-lookup"><span data-stu-id="d7b53-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="d7b53-114">Questo cmdlet ottiene la configurazione di MySql specificata per nome.</span><span class="sxs-lookup"><span data-stu-id="d7b53-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="d7b53-115">Esempio 3: configurazione elenco per identità</span><span class="sxs-lookup"><span data-stu-id="d7b53-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="d7b53-116">Questo cmdlet ottiene la configurazione di MySql specificata in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d7b53-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="d7b53-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7b53-117">PARAMETERS</span></span>

### <span data-ttu-id="d7b53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b53-118">-DefaultProfile</span></span>
<span data-ttu-id="d7b53-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7b53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b53-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7b53-120">-InputObject</span></span>
<span data-ttu-id="d7b53-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d7b53-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7b53-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7b53-122">-Name</span></span>
<span data-ttu-id="d7b53-123">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d7b53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b53-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7b53-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7b53-125">The name of the resource group.</span></span>
<span data-ttu-id="d7b53-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d7b53-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7b53-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d7b53-127">-ServerName</span></span>
<span data-ttu-id="d7b53-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-128">The name of the server.</span></span>

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

### <span data-ttu-id="d7b53-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7b53-129">-SubscriptionId</span></span>
<span data-ttu-id="d7b53-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d7b53-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7b53-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b53-131">CommonParameters</span></span>
<span data-ttu-id="d7b53-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b53-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b53-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7b53-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b53-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7b53-134">INPUTS</span></span>

### <span data-ttu-id="d7b53-135">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d7b53-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d7b53-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7b53-136">OUTPUTS</span></span>

### <span data-ttu-id="d7b53-137">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d7b53-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="d7b53-138">Note</span><span class="sxs-lookup"><span data-stu-id="d7b53-138">NOTES</span></span>

<span data-ttu-id="d7b53-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d7b53-139">ALIASES</span></span>

<span data-ttu-id="d7b53-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7b53-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7b53-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d7b53-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7b53-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7b53-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7b53-143">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d7b53-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7b53-144">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d7b53-145">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d7b53-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d7b53-146">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d7b53-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d7b53-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7b53-148">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d7b53-149">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d7b53-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d7b53-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d7b53-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7b53-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d7b53-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7b53-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d7b53-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d7b53-153">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d7b53-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d7b53-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d7b53-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7b53-155">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d7b53-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d7b53-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7b53-156">RELATED LINKS</span></span>

