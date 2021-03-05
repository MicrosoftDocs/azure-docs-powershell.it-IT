---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: 74174648a1c8b743357bb6036e213f0674ab959d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995412"
---
# <span data-ttu-id="14cc9-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="14cc9-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="14cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="14cc9-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-103">Restarts a server.</span></span>

## <span data-ttu-id="14cc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14cc9-104">SYNTAX</span></span>

### <span data-ttu-id="14cc9-105">Riavvia (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14cc9-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14cc9-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14cc9-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14cc9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14cc9-107">DESCRIPTION</span></span>
<span data-ttu-id="14cc9-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-108">Restarts a server.</span></span>

## <span data-ttu-id="14cc9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14cc9-109">EXAMPLES</span></span>

### <span data-ttu-id="14cc9-110">Esempio 1: Riavviare il server in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="14cc9-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="14cc9-111">Riavviare il server in base al nome</span><span class="sxs-lookup"><span data-stu-id="14cc9-111">Restart the server by name</span></span>

### <span data-ttu-id="14cc9-112">Esempio 2: Riavviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="14cc9-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="14cc9-113">Riavviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="14cc9-113">Restart the server by identity</span></span>

## <span data-ttu-id="14cc9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14cc9-114">PARAMETERS</span></span>

### <span data-ttu-id="14cc9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14cc9-115">-AsJob</span></span>
<span data-ttu-id="14cc9-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="14cc9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="14cc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cc9-117">-DefaultProfile</span></span>
<span data-ttu-id="14cc9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14cc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14cc9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14cc9-119">-InputObject</span></span>
<span data-ttu-id="14cc9-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="14cc9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14cc9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="14cc9-121">-Name</span></span>
<span data-ttu-id="14cc9-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-122">The name of the server.</span></span>

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

### <span data-ttu-id="14cc9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="14cc9-123">-NoWait</span></span>
<span data-ttu-id="14cc9-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="14cc9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="14cc9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14cc9-125">-PassThru</span></span>
<span data-ttu-id="14cc9-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="14cc9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="14cc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14cc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="14cc9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14cc9-128">The name of the resource group.</span></span>
<span data-ttu-id="14cc9-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="14cc9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="14cc9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14cc9-130">-SubscriptionId</span></span>
<span data-ttu-id="14cc9-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14cc9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="14cc9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14cc9-132">-Confirm</span></span>
<span data-ttu-id="14cc9-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14cc9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14cc9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14cc9-134">-WhatIf</span></span>
<span data-ttu-id="14cc9-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14cc9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14cc9-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14cc9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14cc9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cc9-137">CommonParameters</span></span>
<span data-ttu-id="14cc9-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cc9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cc9-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14cc9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cc9-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="14cc9-140">INPUTS</span></span>

### <span data-ttu-id="14cc9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="14cc9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="14cc9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14cc9-142">OUTPUTS</span></span>

### <span data-ttu-id="14cc9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14cc9-143">System.Boolean</span></span>

## <span data-ttu-id="14cc9-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="14cc9-144">NOTES</span></span>

<span data-ttu-id="14cc9-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="14cc9-145">ALIASES</span></span>

<span data-ttu-id="14cc9-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="14cc9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14cc9-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="14cc9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14cc9-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14cc9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14cc9-149">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="14cc9-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14cc9-150">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="14cc9-151">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="14cc9-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="14cc9-152">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="14cc9-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="14cc9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14cc9-154">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="14cc9-155">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="14cc9-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="14cc9-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14cc9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="14cc9-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="14cc9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="14cc9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14cc9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="14cc9-159">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="14cc9-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="14cc9-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14cc9-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="14cc9-161">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="14cc9-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="14cc9-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14cc9-162">RELATED LINKS</span></span>

