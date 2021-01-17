---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlServer.md
ms.openlocfilehash: 6af7f506f7757374efa5efc5029b8edc419ce4be
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475189"
---
# <span data-ttu-id="68d62-101">Restart-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="68d62-101">Restart-AzMySqlServer</span></span>

## <span data-ttu-id="68d62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68d62-102">SYNOPSIS</span></span>
<span data-ttu-id="68d62-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="68d62-103">Restarts a server.</span></span>

## <span data-ttu-id="68d62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68d62-104">SYNTAX</span></span>

### <span data-ttu-id="68d62-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68d62-105">Restart (Default)</span></span>
```
Restart-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68d62-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="68d62-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68d62-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68d62-107">DESCRIPTION</span></span>
<span data-ttu-id="68d62-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="68d62-108">Restarts a server.</span></span>

## <span data-ttu-id="68d62-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68d62-109">EXAMPLES</span></span>

### <span data-ttu-id="68d62-110">Esempio 1: riavviare il server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="68d62-110">Example 1: Restart MySql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="68d62-111">Questo cmdlet riavvia il server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-111">This cmdlet restarts MySql server by resource group and server name.</span></span>

### <span data-ttu-id="68d62-112">Esempio 2: riavviare il server MySql per identità</span><span class="sxs-lookup"><span data-stu-id="68d62-112">Example 2: Restart MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/restart"
PS C:\> Restart-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="68d62-113">Questi cmdlet riavviano MySql Server per identità.</span><span class="sxs-lookup"><span data-stu-id="68d62-113">These cmdlets restart MySql server by identity.</span></span>

## <span data-ttu-id="68d62-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68d62-114">PARAMETERS</span></span>

### <span data-ttu-id="68d62-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68d62-115">-AsJob</span></span>
<span data-ttu-id="68d62-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="68d62-116">Run the command as a job</span></span>

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

### <span data-ttu-id="68d62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d62-117">-DefaultProfile</span></span>
<span data-ttu-id="68d62-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68d62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68d62-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68d62-119">-InputObject</span></span>
<span data-ttu-id="68d62-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="68d62-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68d62-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="68d62-121">-Name</span></span>
<span data-ttu-id="68d62-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-122">The name of the server.</span></span>

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

### <span data-ttu-id="68d62-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="68d62-123">-NoWait</span></span>
<span data-ttu-id="68d62-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="68d62-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68d62-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68d62-125">-PassThru</span></span>
<span data-ttu-id="68d62-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="68d62-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="68d62-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d62-127">-ResourceGroupName</span></span>
<span data-ttu-id="68d62-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68d62-128">The name of the resource group.</span></span>
<span data-ttu-id="68d62-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="68d62-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="68d62-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68d62-130">-SubscriptionId</span></span>
<span data-ttu-id="68d62-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="68d62-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="68d62-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68d62-132">-Confirm</span></span>
<span data-ttu-id="68d62-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68d62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d62-134">-WhatIf</span></span>
<span data-ttu-id="68d62-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d62-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d62-137">CommonParameters</span></span>
<span data-ttu-id="68d62-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d62-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68d62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d62-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68d62-140">INPUTS</span></span>

### <span data-ttu-id="68d62-141">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="68d62-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="68d62-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68d62-142">OUTPUTS</span></span>

### <span data-ttu-id="68d62-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68d62-143">System.Boolean</span></span>

## <span data-ttu-id="68d62-144">Note</span><span class="sxs-lookup"><span data-stu-id="68d62-144">NOTES</span></span>

<span data-ttu-id="68d62-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="68d62-145">ALIASES</span></span>

<span data-ttu-id="68d62-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68d62-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68d62-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="68d62-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68d62-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68d62-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68d62-149">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="68d62-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68d62-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="68d62-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="68d62-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="68d62-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="68d62-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="68d62-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68d62-154">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="68d62-155">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="68d62-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="68d62-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="68d62-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="68d62-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="68d62-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="68d62-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="68d62-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="68d62-159">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="68d62-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="68d62-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="68d62-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="68d62-161">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="68d62-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="68d62-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68d62-162">RELATED LINKS</span></span>

