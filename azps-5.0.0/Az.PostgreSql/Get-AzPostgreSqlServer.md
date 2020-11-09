---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310134"
---
# <span data-ttu-id="907ae-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="907ae-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="907ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="907ae-102">SYNOPSIS</span></span>
<span data-ttu-id="907ae-103">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="907ae-103">Gets information about a server.</span></span>

## <span data-ttu-id="907ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="907ae-104">SYNTAX</span></span>

### <span data-ttu-id="907ae-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="907ae-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="907ae-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="907ae-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="907ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="907ae-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="907ae-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="907ae-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="907ae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="907ae-109">DESCRIPTION</span></span>
<span data-ttu-id="907ae-110">Ottiene le informazioni su un server.</span><span class="sxs-lookup"><span data-stu-id="907ae-110">Gets information about a server.</span></span>

## <span data-ttu-id="907ae-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="907ae-111">EXAMPLES</span></span>

### <span data-ttu-id="907ae-112">Esempio 1: ottenere il server PostgreSql con il contesto predefinito</span><span class="sxs-lookup"><span data-stu-id="907ae-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="907ae-113">Questo cmdlet ottiene il server PostgreSql con il contesto predefinito.</span><span class="sxs-lookup"><span data-stu-id="907ae-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="907ae-114">Esempio 2: ottenere il server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="907ae-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="907ae-115">Questo cmdlet ottiene il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="907ae-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="907ae-116">Esempio 3: elenca tutti i server PostgreSql nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="907ae-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="907ae-117">Questo cmdlet elenca tutti i server PostgreSql nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="907ae-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="907ae-118">Esempio 4: ottenere il server PostgreSql per identità</span><span class="sxs-lookup"><span data-stu-id="907ae-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="907ae-119">Questo cmdlet elenca il server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="907ae-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="907ae-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="907ae-120">PARAMETERS</span></span>

### <span data-ttu-id="907ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907ae-121">-DefaultProfile</span></span>
<span data-ttu-id="907ae-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="907ae-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907ae-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="907ae-123">-InputObject</span></span>
<span data-ttu-id="907ae-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="907ae-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="907ae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="907ae-125">-Name</span></span>
<span data-ttu-id="907ae-126">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="907ae-126">The name of the server.</span></span>

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

### <span data-ttu-id="907ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="907ae-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="907ae-128">The name of the resource group.</span></span>
<span data-ttu-id="907ae-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="907ae-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="907ae-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="907ae-130">-SubscriptionId</span></span>
<span data-ttu-id="907ae-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="907ae-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="907ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907ae-132">CommonParameters</span></span>
<span data-ttu-id="907ae-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907ae-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="907ae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907ae-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="907ae-135">INPUTS</span></span>

### <span data-ttu-id="907ae-136">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="907ae-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="907ae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="907ae-137">OUTPUTS</span></span>

### <span data-ttu-id="907ae-138">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="907ae-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="907ae-139">Note</span><span class="sxs-lookup"><span data-stu-id="907ae-139">NOTES</span></span>

<span data-ttu-id="907ae-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="907ae-140">ALIASES</span></span>

<span data-ttu-id="907ae-141">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="907ae-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="907ae-142">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="907ae-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="907ae-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="907ae-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="907ae-144">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="907ae-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="907ae-145">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="907ae-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="907ae-146">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="907ae-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="907ae-147">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="907ae-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="907ae-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="907ae-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="907ae-149">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="907ae-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="907ae-150">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="907ae-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="907ae-151">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="907ae-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="907ae-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="907ae-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="907ae-153">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="907ae-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="907ae-154">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="907ae-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="907ae-155">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="907ae-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="907ae-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="907ae-156">RELATED LINKS</span></span>

