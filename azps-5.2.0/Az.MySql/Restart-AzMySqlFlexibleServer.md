---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: dacaab524db0403d4f7c1ac2df9b215e920afa18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360359"
---
# <span data-ttu-id="8ba5a-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="8ba5a-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="8ba5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ba5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba5a-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-103">Restarts a server.</span></span>

## <span data-ttu-id="8ba5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-104">SYNTAX</span></span>

### <span data-ttu-id="8ba5a-105">Restart (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ba5a-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ba5a-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ba5a-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ba5a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ba5a-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba5a-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-108">Restarts a server.</span></span>

## <span data-ttu-id="8ba5a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-109">EXAMPLES</span></span>

### <span data-ttu-id="8ba5a-110">Esempio 1: riavviare il server per nome risorsa</span><span class="sxs-lookup"><span data-stu-id="8ba5a-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="8ba5a-111">Riavviare il server per nome</span><span class="sxs-lookup"><span data-stu-id="8ba5a-111">Restart the server by name</span></span>

### <span data-ttu-id="8ba5a-112">Esempio 2: riavviare il server per identità</span><span class="sxs-lookup"><span data-stu-id="8ba5a-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="8ba5a-113">Riavviare il server per identità</span><span class="sxs-lookup"><span data-stu-id="8ba5a-113">Restart the server by identity</span></span>

## <span data-ttu-id="8ba5a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba5a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ba5a-115">-AsJob</span></span>
<span data-ttu-id="8ba5a-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="8ba5a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8ba5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba5a-117">-DefaultProfile</span></span>
<span data-ttu-id="8ba5a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba5a-119">-InputObject</span></span>
<span data-ttu-id="8ba5a-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ba5a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ba5a-121">-Name</span></span>
<span data-ttu-id="8ba5a-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-122">The name of the server.</span></span>

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

### <span data-ttu-id="8ba5a-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="8ba5a-123">-NoWait</span></span>
<span data-ttu-id="8ba5a-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="8ba5a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8ba5a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba5a-125">-PassThru</span></span>
<span data-ttu-id="8ba5a-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="8ba5a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8ba5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ba5a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-128">The name of the resource group.</span></span>
<span data-ttu-id="8ba5a-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8ba5a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ba5a-130">-SubscriptionId</span></span>
<span data-ttu-id="8ba5a-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8ba5a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ba5a-132">-Confirm</span></span>
<span data-ttu-id="8ba5a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba5a-134">-WhatIf</span></span>
<span data-ttu-id="8ba5a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba5a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba5a-137">CommonParameters</span></span>
<span data-ttu-id="8ba5a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba5a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ba5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba5a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-140">INPUTS</span></span>

### <span data-ttu-id="8ba5a-141">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8ba5a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8ba5a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ba5a-142">OUTPUTS</span></span>

### <span data-ttu-id="8ba5a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ba5a-143">System.Boolean</span></span>

## <span data-ttu-id="8ba5a-144">Note</span><span class="sxs-lookup"><span data-stu-id="8ba5a-144">NOTES</span></span>

<span data-ttu-id="8ba5a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8ba5a-145">ALIASES</span></span>

<span data-ttu-id="8ba5a-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ba5a-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ba5a-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ba5a-149">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8ba5a-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ba5a-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8ba5a-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8ba5a-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8ba5a-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8ba5a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ba5a-154">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8ba5a-155">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8ba5a-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8ba5a-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="8ba5a-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8ba5a-159">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8ba5a-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8ba5a-161">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8ba5a-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-162">RELATED LINKS</span></span>

