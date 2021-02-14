---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203378"
---
# <span data-ttu-id="43d67-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="43d67-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="43d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d67-102">SYNOPSIS</span></span>
<span data-ttu-id="43d67-103">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="43d67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43d67-104">SYNTAX</span></span>

### <span data-ttu-id="43d67-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43d67-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d67-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="43d67-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d67-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43d67-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43d67-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="43d67-108">DESCRIPTION</span></span>
<span data-ttu-id="43d67-109">Ottiene informazioni su una configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="43d67-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43d67-110">EXAMPLES</span></span>

### <span data-ttu-id="43d67-111">Esempio 1: Elencare tutte le configurazioni nel server MySql specificato</span><span class="sxs-lookup"><span data-stu-id="43d67-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="43d67-112">Questo cmdlet elenca tutte le configurazioni nel server MySql specificato.</span><span class="sxs-lookup"><span data-stu-id="43d67-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="43d67-113">Esempio 2: Ottenere la configurazione MySql specificata in base al nome</span><span class="sxs-lookup"><span data-stu-id="43d67-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="43d67-114">Questo cmdlet viene specificato in base al nome della configurazione MySql.</span><span class="sxs-lookup"><span data-stu-id="43d67-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="43d67-115">Esempio 3: Configurazione dell'elenco in base all'identità</span><span class="sxs-lookup"><span data-stu-id="43d67-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="43d67-116">Questo cmdlet viene specificato per la configurazione mySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="43d67-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="43d67-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d67-117">PARAMETERS</span></span>

### <span data-ttu-id="43d67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d67-118">-DefaultProfile</span></span>
<span data-ttu-id="43d67-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43d67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d67-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d67-120">-InputObject</span></span>
<span data-ttu-id="43d67-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43d67-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d67-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43d67-122">-Name</span></span>
<span data-ttu-id="43d67-123">Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="43d67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d67-124">-ResourceGroupName</span></span>
<span data-ttu-id="43d67-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43d67-125">The name of the resource group.</span></span>
<span data-ttu-id="43d67-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="43d67-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43d67-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43d67-127">-ServerName</span></span>
<span data-ttu-id="43d67-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-128">The name of the server.</span></span>

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

### <span data-ttu-id="43d67-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43d67-129">-SubscriptionId</span></span>
<span data-ttu-id="43d67-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43d67-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43d67-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d67-131">CommonParameters</span></span>
<span data-ttu-id="43d67-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d67-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d67-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43d67-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d67-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="43d67-134">INPUTS</span></span>

### <span data-ttu-id="43d67-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="43d67-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="43d67-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43d67-136">OUTPUTS</span></span>

### <span data-ttu-id="43d67-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="43d67-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="43d67-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="43d67-138">NOTES</span></span>

<span data-ttu-id="43d67-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43d67-139">ALIASES</span></span>

<span data-ttu-id="43d67-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="43d67-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43d67-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="43d67-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d67-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43d67-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43d67-143">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="43d67-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d67-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="43d67-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="43d67-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="43d67-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="43d67-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="43d67-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d67-148">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="43d67-149">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="43d67-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="43d67-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43d67-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43d67-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="43d67-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="43d67-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="43d67-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="43d67-153">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="43d67-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="43d67-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43d67-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="43d67-155">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="43d67-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="43d67-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43d67-156">RELATED LINKS</span></span>

