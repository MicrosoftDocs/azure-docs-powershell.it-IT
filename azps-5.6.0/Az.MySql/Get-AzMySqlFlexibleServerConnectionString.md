---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011950"
---
# <span data-ttu-id="8aadc-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="8aadc-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="8aadc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aadc-102">SYNOPSIS</span></span>
<span data-ttu-id="8aadc-103">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="8aadc-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="8aadc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8aadc-104">SYNTAX</span></span>

### <span data-ttu-id="8aadc-105">Ottieni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8aadc-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8aadc-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8aadc-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8aadc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8aadc-107">DESCRIPTION</span></span>
<span data-ttu-id="8aadc-108">Ottenere la stringa di connessione in base al provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="8aadc-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="8aadc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8aadc-109">EXAMPLES</span></span>

### <span data-ttu-id="8aadc-110">Esempio 1: Ottenere la stringa di connessione in base al nome</span><span class="sxs-lookup"><span data-stu-id="8aadc-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="8aadc-111">Questo cmdlet mostra la stringa di connessione di un client per nome server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="8aadc-112">Esempio 2: Ottenere la stringa di connessione del server MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="8aadc-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="8aadc-113">Questo cmdlet ottiene la stringa di connessione del server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="8aadc-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="8aadc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aadc-114">PARAMETERS</span></span>

### <span data-ttu-id="8aadc-115">-Client</span><span class="sxs-lookup"><span data-stu-id="8aadc-115">-Client</span></span>
<span data-ttu-id="8aadc-116">Provider di connessione client.</span><span class="sxs-lookup"><span data-stu-id="8aadc-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aadc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aadc-117">-DefaultProfile</span></span>
<span data-ttu-id="8aadc-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8aadc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aadc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8aadc-119">-InputObject</span></span>
<span data-ttu-id="8aadc-120">Server per la stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="8aadc-120">The server for the connection string.</span></span>
<span data-ttu-id="8aadc-121">Per creare, vedere la sezione NOTE per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8aadc-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8aadc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8aadc-122">-Name</span></span>
<span data-ttu-id="8aadc-123">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aadc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aadc-124">-ResourceGroupName</span></span>
<span data-ttu-id="8aadc-125">Nome del gruppo di risorse che contiene la risorsa. È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="8aadc-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aadc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8aadc-126">-SubscriptionId</span></span>
<span data-ttu-id="8aadc-127">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8aadc-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aadc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aadc-128">CommonParameters</span></span>
<span data-ttu-id="8aadc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aadc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aadc-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8aadc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aadc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="8aadc-131">INPUTS</span></span>

### <span data-ttu-id="8aadc-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8aadc-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8aadc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8aadc-133">OUTPUTS</span></span>

### <span data-ttu-id="8aadc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8aadc-134">System.String</span></span>

## <span data-ttu-id="8aadc-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="8aadc-135">NOTES</span></span>

<span data-ttu-id="8aadc-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8aadc-136">ALIASES</span></span>

<span data-ttu-id="8aadc-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8aadc-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8aadc-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8aadc-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8aadc-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8aadc-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8aadc-140"><IMySqlIdentity>INPUTOBJECT: server per la stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="8aadc-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="8aadc-141">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8aadc-142">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="8aadc-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8aadc-143">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8aadc-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8aadc-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8aadc-145">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8aadc-146">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="8aadc-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8aadc-147">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8aadc-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8aadc-148">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8aadc-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="8aadc-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8aadc-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8aadc-150">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="8aadc-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8aadc-151">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8aadc-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8aadc-152">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8aadc-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8aadc-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8aadc-153">RELATED LINKS</span></span>

