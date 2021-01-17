---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378461"
---
# <span data-ttu-id="05fa3-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="05fa3-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="05fa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="05fa3-103">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-103">Gets information about a server.</span></span>

## <span data-ttu-id="05fa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05fa3-104">SYNTAX</span></span>

### <span data-ttu-id="05fa3-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05fa3-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05fa3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="05fa3-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05fa3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05fa3-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05fa3-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="05fa3-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="05fa3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05fa3-109">DESCRIPTION</span></span>
<span data-ttu-id="05fa3-110">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-110">Gets information about a server.</span></span>

## <span data-ttu-id="05fa3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05fa3-111">EXAMPLES</span></span>

### <span data-ttu-id="05fa3-112">Esempio 1: ottenere il server PostgreSql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="05fa3-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="05fa3-113">Questo cmdlet ottiene il server PostgreSql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="05fa3-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="05fa3-114">Esempio 2: ottenere il server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="05fa3-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="05fa3-115">Questo cmdlet ottiene il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="05fa3-116">Esempio 3: elenca tutti i server PostgreSql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="05fa3-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="05fa3-117">Questo cmdlet elenca tutti i server PostgreSql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="05fa3-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="05fa3-118">Esempio 4: ottenere il server PostgreSql per identità</span><span class="sxs-lookup"><span data-stu-id="05fa3-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="05fa3-119">Questo cmdlet elenca il server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="05fa3-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="05fa3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05fa3-120">PARAMETERS</span></span>

### <span data-ttu-id="05fa3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05fa3-121">-DefaultProfile</span></span>
<span data-ttu-id="05fa3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05fa3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05fa3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05fa3-123">-InputObject</span></span>
<span data-ttu-id="05fa3-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="05fa3-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05fa3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="05fa3-125">-Name</span></span>
<span data-ttu-id="05fa3-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-126">The name of the server.</span></span>

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

### <span data-ttu-id="05fa3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05fa3-127">-ResourceGroupName</span></span>
<span data-ttu-id="05fa3-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05fa3-128">The name of the resource group.</span></span>
<span data-ttu-id="05fa3-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="05fa3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="05fa3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05fa3-130">-SubscriptionId</span></span>
<span data-ttu-id="05fa3-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="05fa3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="05fa3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05fa3-132">CommonParameters</span></span>
<span data-ttu-id="05fa3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05fa3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05fa3-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05fa3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05fa3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05fa3-135">INPUTS</span></span>

### <span data-ttu-id="05fa3-136">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="05fa3-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="05fa3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05fa3-137">OUTPUTS</span></span>

### <span data-ttu-id="05fa3-138">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="05fa3-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="05fa3-139">Note</span><span class="sxs-lookup"><span data-stu-id="05fa3-139">NOTES</span></span>

<span data-ttu-id="05fa3-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="05fa3-140">ALIASES</span></span>

<span data-ttu-id="05fa3-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05fa3-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05fa3-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="05fa3-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05fa3-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="05fa3-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05fa3-144">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="05fa3-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05fa3-145">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="05fa3-146">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="05fa3-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="05fa3-147">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="05fa3-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="05fa3-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05fa3-149">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="05fa3-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="05fa3-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05fa3-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="05fa3-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="05fa3-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="05fa3-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="05fa3-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="05fa3-153">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="05fa3-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="05fa3-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="05fa3-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="05fa3-155">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="05fa3-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="05fa3-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05fa3-156">RELATED LINKS</span></span>

