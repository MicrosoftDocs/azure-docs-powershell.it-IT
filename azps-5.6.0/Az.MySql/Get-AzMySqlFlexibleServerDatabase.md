---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: b060657d9e8d69ebddf639847de7718ec626fdb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991030"
---
# <span data-ttu-id="67fbe-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="67fbe-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="67fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="67fbe-103">Ottiene informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="67fbe-103">Gets information about a database.</span></span>

## <span data-ttu-id="67fbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67fbe-104">SYNTAX</span></span>

### <span data-ttu-id="67fbe-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67fbe-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67fbe-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="67fbe-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="67fbe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="67fbe-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="67fbe-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67fbe-108">DESCRIPTION</span></span>
<span data-ttu-id="67fbe-109">Ottiene informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="67fbe-109">Gets information about a database.</span></span>

## <span data-ttu-id="67fbe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67fbe-110">EXAMPLES</span></span>

### <span data-ttu-id="67fbe-111">Esempio 1: Ottenere un database MySql in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="67fbe-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="67fbe-112">Questo cmdlet ottiene il server MySql in base al nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="67fbe-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="67fbe-113">Esempio 2: Ottenere database MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="67fbe-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="67fbe-114">Questo cmdlet ottiene un server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="67fbe-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="67fbe-115">Esempio 3: Elenca tutti i database MySql nel server specificato</span><span class="sxs-lookup"><span data-stu-id="67fbe-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="67fbe-116">Questo cmdlet elenca tutti i server MySql nel server specificato.</span><span class="sxs-lookup"><span data-stu-id="67fbe-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="67fbe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67fbe-117">PARAMETERS</span></span>

### <span data-ttu-id="67fbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67fbe-118">-DefaultProfile</span></span>
<span data-ttu-id="67fbe-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67fbe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67fbe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67fbe-120">-InputObject</span></span>
<span data-ttu-id="67fbe-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="67fbe-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67fbe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="67fbe-122">-Name</span></span>
<span data-ttu-id="67fbe-123">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="67fbe-123">The name of the database.</span></span>

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

### <span data-ttu-id="67fbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67fbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="67fbe-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67fbe-125">The name of the resource group.</span></span>
<span data-ttu-id="67fbe-126">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="67fbe-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="67fbe-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="67fbe-127">-ServerName</span></span>
<span data-ttu-id="67fbe-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="67fbe-128">The name of the server.</span></span>

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

### <span data-ttu-id="67fbe-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67fbe-129">-SubscriptionId</span></span>
<span data-ttu-id="67fbe-130">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="67fbe-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="67fbe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67fbe-131">CommonParameters</span></span>
<span data-ttu-id="67fbe-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67fbe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67fbe-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67fbe-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67fbe-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="67fbe-134">INPUTS</span></span>

### <span data-ttu-id="67fbe-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="67fbe-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="67fbe-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67fbe-136">OUTPUTS</span></span>

### <span data-ttu-id="67fbe-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="67fbe-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="67fbe-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="67fbe-138">NOTES</span></span>

<span data-ttu-id="67fbe-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="67fbe-139">ALIASES</span></span>

<span data-ttu-id="67fbe-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="67fbe-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67fbe-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="67fbe-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67fbe-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67fbe-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67fbe-143">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="67fbe-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67fbe-144">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="67fbe-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="67fbe-145">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="67fbe-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="67fbe-146">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="67fbe-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="67fbe-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="67fbe-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67fbe-148">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="67fbe-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="67fbe-149">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="67fbe-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="67fbe-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67fbe-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="67fbe-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="67fbe-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="67fbe-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="67fbe-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="67fbe-153">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="67fbe-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="67fbe-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="67fbe-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="67fbe-155">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="67fbe-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="67fbe-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67fbe-156">RELATED LINKS</span></span>

