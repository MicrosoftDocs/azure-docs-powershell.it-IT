---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188303"
---
# <span data-ttu-id="1f7fe-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="1f7fe-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="1f7fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7fe-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-103">Restarts a server.</span></span>

## <span data-ttu-id="1f7fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-104">SYNTAX</span></span>

### <span data-ttu-id="1f7fe-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f7fe-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f7fe-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f7fe-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f7fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f7fe-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7fe-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-108">Restarts a server.</span></span>

## <span data-ttu-id="1f7fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-109">EXAMPLES</span></span>

### <span data-ttu-id="1f7fe-110">Esempio 1: riavviare il server PostgreSql per il gruppo di risorse e il nome del server</span><span class="sxs-lookup"><span data-stu-id="1f7fe-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="1f7fe-111">Questo cmdlet riavvia il server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="1f7fe-112">Esempio 2: riavviare il server PostgreSql per identità</span><span class="sxs-lookup"><span data-stu-id="1f7fe-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="1f7fe-113">Questi cmdlet riavviano il server PostgreSql per identità.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="1f7fe-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-114">PARAMETERS</span></span>

### <span data-ttu-id="1f7fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f7fe-115">-AsJob</span></span>
<span data-ttu-id="1f7fe-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1f7fe-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7fe-117">-DefaultProfile</span></span>
<span data-ttu-id="1f7fe-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f7fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f7fe-119">-InputObject</span></span>
<span data-ttu-id="1f7fe-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f7fe-121">-Name</span></span>
<span data-ttu-id="1f7fe-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="1f7fe-123">-NoWait</span></span>
<span data-ttu-id="1f7fe-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1f7fe-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f7fe-125">-PassThru</span></span>
<span data-ttu-id="1f7fe-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="1f7fe-126">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f7fe-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-128">The name of the resource group.</span></span>
<span data-ttu-id="1f7fe-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f7fe-130">-SubscriptionId</span></span>
<span data-ttu-id="1f7fe-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f7fe-132">-Confirm</span></span>
<span data-ttu-id="1f7fe-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7fe-134">-WhatIf</span></span>
<span data-ttu-id="1f7fe-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f7fe-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f7fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7fe-137">CommonParameters</span></span>
<span data-ttu-id="1f7fe-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7fe-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f7fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7fe-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-140">INPUTS</span></span>

### <span data-ttu-id="1f7fe-141">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1f7fe-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="1f7fe-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f7fe-142">OUTPUTS</span></span>

### <span data-ttu-id="1f7fe-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f7fe-143">System.Boolean</span></span>

## <span data-ttu-id="1f7fe-144">Note</span><span class="sxs-lookup"><span data-stu-id="1f7fe-144">NOTES</span></span>

<span data-ttu-id="1f7fe-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f7fe-145">ALIASES</span></span>

<span data-ttu-id="1f7fe-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1f7fe-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f7fe-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1f7fe-149">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1f7fe-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f7fe-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1f7fe-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1f7fe-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1f7fe-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1f7fe-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f7fe-154">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1f7fe-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1f7fe-156">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="1f7fe-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1f7fe-158">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1f7fe-159">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1f7fe-160">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f7fe-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1f7fe-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f7fe-161">RELATED LINKS</span></span>
