---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358973"
---
# <span data-ttu-id="9897c-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="9897c-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="9897c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9897c-102">SYNOPSIS</span></span>
<span data-ttu-id="9897c-103">Ottiene le informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="9897c-103">Gets information about a database.</span></span>

## <span data-ttu-id="9897c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9897c-104">SYNTAX</span></span>

### <span data-ttu-id="9897c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9897c-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9897c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="9897c-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9897c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9897c-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9897c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9897c-108">DESCRIPTION</span></span>
<span data-ttu-id="9897c-109">Ottiene le informazioni su un database.</span><span class="sxs-lookup"><span data-stu-id="9897c-109">Gets information about a database.</span></span>

## <span data-ttu-id="9897c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9897c-110">EXAMPLES</span></span>

### <span data-ttu-id="9897c-111">Esempio 1: ottenere un database MySql in base al nome di risorsa</span><span class="sxs-lookup"><span data-stu-id="9897c-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="9897c-112">Questo cmdlet ottiene il server MySql in base al nome di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9897c-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="9897c-113">Esempio 2: ottenere i database MySql per identità</span><span class="sxs-lookup"><span data-stu-id="9897c-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="9897c-114">Questo cmdlet ottiene un server MySql per identità.</span><span class="sxs-lookup"><span data-stu-id="9897c-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="9897c-115">Esempio 3: elenca tutti i database MySql nel server specificato</span><span class="sxs-lookup"><span data-stu-id="9897c-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="9897c-116">Questo cmdlet elenca tutti i server MySql in specificato il server.</span><span class="sxs-lookup"><span data-stu-id="9897c-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="9897c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9897c-117">PARAMETERS</span></span>

### <span data-ttu-id="9897c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9897c-118">-DefaultProfile</span></span>
<span data-ttu-id="9897c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9897c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9897c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9897c-120">-InputObject</span></span>
<span data-ttu-id="9897c-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9897c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9897c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9897c-122">-Name</span></span>
<span data-ttu-id="9897c-123">Nome del database.</span><span class="sxs-lookup"><span data-stu-id="9897c-123">The name of the database.</span></span>

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

### <span data-ttu-id="9897c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9897c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9897c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9897c-125">The name of the resource group.</span></span>
<span data-ttu-id="9897c-126">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9897c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9897c-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9897c-127">-ServerName</span></span>
<span data-ttu-id="9897c-128">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9897c-128">The name of the server.</span></span>

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

### <span data-ttu-id="9897c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9897c-129">-SubscriptionId</span></span>
<span data-ttu-id="9897c-130">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9897c-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9897c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9897c-131">CommonParameters</span></span>
<span data-ttu-id="9897c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9897c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9897c-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9897c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9897c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9897c-134">INPUTS</span></span>

### <span data-ttu-id="9897c-135">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9897c-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9897c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9897c-136">OUTPUTS</span></span>

### <span data-ttu-id="9897c-137">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="9897c-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="9897c-138">Note</span><span class="sxs-lookup"><span data-stu-id="9897c-138">NOTES</span></span>

<span data-ttu-id="9897c-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9897c-139">ALIASES</span></span>

<span data-ttu-id="9897c-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9897c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9897c-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9897c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9897c-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9897c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9897c-143">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9897c-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9897c-144">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="9897c-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9897c-145">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="9897c-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9897c-146">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="9897c-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9897c-147">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9897c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9897c-148">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="9897c-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9897c-149">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="9897c-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9897c-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9897c-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9897c-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="9897c-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="9897c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9897c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9897c-153">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="9897c-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9897c-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9897c-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9897c-155">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9897c-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9897c-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9897c-156">RELATED LINKS</span></span>

