---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1cbc4b8274a619514268e8412f7f9123a5e9e58a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202183"
---
# <span data-ttu-id="42dd0-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="42dd0-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="42dd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="42dd0-103">Testare la connessione al server di database</span><span class="sxs-lookup"><span data-stu-id="42dd0-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="42dd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42dd0-104">SYNTAX</span></span>

### <span data-ttu-id="42dd0-105">Test (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42dd0-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42dd0-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="42dd0-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42dd0-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="42dd0-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="42dd0-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="42dd0-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="42dd0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42dd0-109">DESCRIPTION</span></span>
<span data-ttu-id="42dd0-110">Testare la connessione al server di database</span><span class="sxs-lookup"><span data-stu-id="42dd0-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="42dd0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42dd0-111">EXAMPLES</span></span>

### <span data-ttu-id="42dd0-112">Esempio 1: Verificare la connessione in base al nome</span><span class="sxs-lookup"><span data-stu-id="42dd0-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="42dd0-113">Verificare la connessione in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="42dd0-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="42dd0-114">Esempio 2: Verificare la connessione in base all'identità</span><span class="sxs-lookup"><span data-stu-id="42dd0-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="42dd0-115">Verificare la connessione in base all'identità</span><span class="sxs-lookup"><span data-stu-id="42dd0-115">Test connection by the identity</span></span>

### <span data-ttu-id="42dd0-116">Esempio 3: Verificare la query in base al nome</span><span class="sxs-lookup"><span data-stu-id="42dd0-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="42dd0-117">Testare una query in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="42dd0-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="42dd0-118">Esempio 4: Verificare la connessione in base all'identità</span><span class="sxs-lookup"><span data-stu-id="42dd0-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="42dd0-119">Testare una query in base all'identità</span><span class="sxs-lookup"><span data-stu-id="42dd0-119">Test a query by the identity</span></span>

## <span data-ttu-id="42dd0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42dd0-120">PARAMETERS</span></span>

### <span data-ttu-id="42dd0-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="42dd0-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="42dd0-122">Password dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="42dd0-122">The password of the administrator.</span></span>
<span data-ttu-id="42dd0-123">Minimo 8 caratteri e massimo 128 caratteri.</span><span class="sxs-lookup"><span data-stu-id="42dd0-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="42dd0-124">La password deve contenere caratteri di tre delle categorie seguenti: lettere maiuscole inglesi, lettere minuscole inglesi, numeri e caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="42dd0-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="42dd0-125">-AdministratorUserName</span></span>
<span data-ttu-id="42dd0-126">Nome utente dell'amministratore per il server.</span><span class="sxs-lookup"><span data-stu-id="42dd0-126">Administrator username for the server.</span></span>
<span data-ttu-id="42dd0-127">Una volta impostata, non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="42dd0-127">Once set, it cannot be changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="42dd0-128">-DatabaseName</span></span>
<span data-ttu-id="42dd0-129">Nome del database da connettere.</span><span class="sxs-lookup"><span data-stu-id="42dd0-129">The database name to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dd0-130">-DefaultProfile</span></span>
<span data-ttu-id="42dd0-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42dd0-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42dd0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42dd0-132">-InputObject</span></span>
<span data-ttu-id="42dd0-133">Il server da connettere.</span><span class="sxs-lookup"><span data-stu-id="42dd0-133">The server to connect.</span></span>
<span data-ttu-id="42dd0-134">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="42dd0-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-135">-Name</span><span class="sxs-lookup"><span data-stu-id="42dd0-135">-Name</span></span>
<span data-ttu-id="42dd0-136">Nome del server da connettere.</span><span class="sxs-lookup"><span data-stu-id="42dd0-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="42dd0-137">-QueryText</span></span>
<span data-ttu-id="42dd0-138">Query per il database da testare</span><span class="sxs-lookup"><span data-stu-id="42dd0-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dd0-139">-ResourceGroupName</span></span>
<span data-ttu-id="42dd0-140">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="42dd0-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dd0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dd0-141">CommonParameters</span></span>
<span data-ttu-id="42dd0-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42dd0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dd0-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42dd0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dd0-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="42dd0-144">INPUTS</span></span>

### <span data-ttu-id="42dd0-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="42dd0-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="42dd0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42dd0-146">OUTPUTS</span></span>

### <span data-ttu-id="42dd0-147">System.String</span><span class="sxs-lookup"><span data-stu-id="42dd0-147">System.String</span></span>

## <span data-ttu-id="42dd0-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="42dd0-148">NOTES</span></span>

<span data-ttu-id="42dd0-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="42dd0-149">ALIASES</span></span>

<span data-ttu-id="42dd0-150">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="42dd0-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="42dd0-151">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="42dd0-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="42dd0-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="42dd0-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="42dd0-153"><IPostgreSqlIdentity>INPUTOBJECT: il server da connettere.</span><span class="sxs-lookup"><span data-stu-id="42dd0-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="42dd0-154">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="42dd0-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="42dd0-155">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="42dd0-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="42dd0-156">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="42dd0-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="42dd0-157">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="42dd0-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="42dd0-158">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="42dd0-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="42dd0-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42dd0-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="42dd0-160">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="42dd0-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="42dd0-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="42dd0-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="42dd0-162">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="42dd0-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="42dd0-163">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="42dd0-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="42dd0-164">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="42dd0-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="42dd0-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42dd0-165">RELATED LINKS</span></span>

