---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: d8dc345ae9f307bbd5f1cd003edf1cba4a7ea6b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193159"
---
# <span data-ttu-id="e1f37-101">Get-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="e1f37-101">Get-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="e1f37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f37-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f37-103">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-103">Gets information about a server.</span></span>

## <span data-ttu-id="e1f37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1f37-104">SYNTAX</span></span>

### <span data-ttu-id="e1f37-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1f37-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1f37-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e1f37-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1f37-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1f37-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f37-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="e1f37-108">List</span></span>
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e1f37-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1f37-109">DESCRIPTION</span></span>
<span data-ttu-id="e1f37-110">Ottiene informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-110">Gets information about a server.</span></span>

## <span data-ttu-id="e1f37-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1f37-111">EXAMPLES</span></span>

### <span data-ttu-id="e1f37-112">Esempio 1: Ottenere il server PostgreSql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="e1f37-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="e1f37-113">Questo cmdlet ottiene i server PostgreSql con contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="e1f37-113">This cmdlet gets PostgreSql servers with default context.</span></span>

### <span data-ttu-id="e1f37-114">Esempio 2: Ottenere il server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="e1f37-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="e1f37-115">Questo cmdlet ottiene i server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-115">This cmdlet gets PostgreSql servers by resource group and server name.</span></span>

### <span data-ttu-id="e1f37-116">Esempio 3: Elenca tutti i server PostgreSql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e1f37-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

<span data-ttu-id="e1f37-117">Questo cmdlet elenca tutti i server PostgreSql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e1f37-117">This cmdlet lists all the PostgreSql servers in the specified resource group.</span></span>

### <span data-ttu-id="e1f37-118">Esempio 4: Ottenere il server PostgreSql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="e1f37-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="e1f37-119">Questo elenco di cmdlet ottiene i server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="e1f37-119">This cmdlet lists gets PostgreSql servers by identity.</span></span>

## <span data-ttu-id="e1f37-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f37-120">PARAMETERS</span></span>

### <span data-ttu-id="e1f37-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f37-121">-DefaultProfile</span></span>
<span data-ttu-id="e1f37-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f37-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f37-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1f37-123">-InputObject</span></span>
<span data-ttu-id="e1f37-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e1f37-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1f37-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e1f37-125">-Name</span></span>
<span data-ttu-id="e1f37-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-126">The name of the server.</span></span>

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

### <span data-ttu-id="e1f37-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f37-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1f37-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1f37-128">The name of the resource group.</span></span>
<span data-ttu-id="e1f37-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e1f37-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e1f37-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1f37-130">-SubscriptionId</span></span>
<span data-ttu-id="e1f37-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1f37-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f37-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f37-132">CommonParameters</span></span>
<span data-ttu-id="e1f37-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f37-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f37-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1f37-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f37-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1f37-135">INPUTS</span></span>

### <span data-ttu-id="e1f37-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e1f37-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e1f37-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1f37-137">OUTPUTS</span></span>

### <span data-ttu-id="e1f37-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e1f37-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="e1f37-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1f37-139">NOTES</span></span>

<span data-ttu-id="e1f37-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e1f37-140">ALIASES</span></span>

<span data-ttu-id="e1f37-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e1f37-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e1f37-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e1f37-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1f37-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1f37-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e1f37-144">INPUTOBJECT <IPostgreSqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e1f37-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1f37-145">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e1f37-146">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="e1f37-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e1f37-147">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e1f37-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e1f37-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1f37-149">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e1f37-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e1f37-150">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e1f37-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e1f37-151">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e1f37-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="e1f37-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e1f37-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e1f37-153">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="e1f37-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e1f37-154">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e1f37-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e1f37-155">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1f37-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e1f37-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1f37-156">RELATED LINKS</span></span>

