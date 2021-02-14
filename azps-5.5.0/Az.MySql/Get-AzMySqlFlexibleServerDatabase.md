---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203359"
---
# <span data-ttu-id="d8928-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="d8928-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="d8928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8928-102">SYNOPSIS</span></span>
<span data-ttu-id="d8928-103">Ottiene informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="d8928-103">Gets information about a database.</span></span>

## <span data-ttu-id="d8928-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8928-104">SYNTAX</span></span>

### <span data-ttu-id="d8928-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8928-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8928-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d8928-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8928-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8928-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8928-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8928-108">DESCRIPTION</span></span>
<span data-ttu-id="d8928-109">Ottiene informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="d8928-109">Gets information about a database.</span></span>

## <span data-ttu-id="d8928-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8928-110">EXAMPLES</span></span>

### <span data-ttu-id="d8928-111">Esempio 1: Ottenere un database MySql in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="d8928-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="d8928-112">Questo cmdlet ottiene il server MySql in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8928-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="d8928-113">Esempio 2: Ottenere database MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="d8928-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="d8928-114">Questo cmdlet ottiene un server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="d8928-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="d8928-115">Esempio 3: Elenca tutti i database MySql nel server specificato</span><span class="sxs-lookup"><span data-stu-id="d8928-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="d8928-116">Questo cmdlet elenca tutti i server MySql nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="d8928-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="d8928-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8928-117">PARAMETERS</span></span>

### <span data-ttu-id="d8928-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8928-118">-DefaultProfile</span></span>
<span data-ttu-id="d8928-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8928-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8928-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8928-120">-InputObject</span></span>
<span data-ttu-id="d8928-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d8928-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8928-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d8928-122">-Name</span></span>
<span data-ttu-id="d8928-123">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="d8928-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8928-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8928-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8928-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8928-125">The name of the resource group.</span></span>
<span data-ttu-id="d8928-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d8928-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d8928-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d8928-127">-ServerName</span></span>
<span data-ttu-id="d8928-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="d8928-128">The name of the server.</span></span>

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

### <span data-ttu-id="d8928-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8928-129">-SubscriptionId</span></span>
<span data-ttu-id="d8928-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d8928-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d8928-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8928-131">CommonParameters</span></span>
<span data-ttu-id="d8928-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8928-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8928-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8928-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8928-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8928-134">INPUTS</span></span>

### <span data-ttu-id="d8928-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d8928-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d8928-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8928-136">OUTPUTS</span></span>

### <span data-ttu-id="d8928-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="d8928-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="d8928-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8928-138">NOTES</span></span>

<span data-ttu-id="d8928-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d8928-139">ALIASES</span></span>

<span data-ttu-id="d8928-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="d8928-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8928-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d8928-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8928-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8928-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8928-143">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="d8928-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8928-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="d8928-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d8928-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="d8928-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d8928-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="d8928-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d8928-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="d8928-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8928-148">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="d8928-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d8928-149">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="d8928-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d8928-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8928-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d8928-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d8928-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d8928-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d8928-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d8928-153">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="d8928-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d8928-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d8928-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d8928-155">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d8928-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d8928-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8928-156">RELATED LINKS</span></span>

