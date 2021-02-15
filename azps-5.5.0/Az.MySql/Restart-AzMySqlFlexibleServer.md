---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restart-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restart-AzMySqlFlexibleServer.md
ms.openlocfilehash: dacaab524db0403d4f7c1ac2df9b215e920afa18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203349"
---
# <span data-ttu-id="bfb63-101">Restart-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="bfb63-101">Restart-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="bfb63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb63-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb63-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-103">Restarts a server.</span></span>

## <span data-ttu-id="bfb63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfb63-104">SYNTAX</span></span>

### <span data-ttu-id="bfb63-105">Riavvia (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfb63-105">Restart (Default)</span></span>
```
Restart-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfb63-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bfb63-106">RestartViaIdentity</span></span>
```
Restart-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfb63-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfb63-107">DESCRIPTION</span></span>
<span data-ttu-id="bfb63-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-108">Restarts a server.</span></span>

## <span data-ttu-id="bfb63-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfb63-109">EXAMPLES</span></span>

### <span data-ttu-id="bfb63-110">Esempio 1: Riavviare il server in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="bfb63-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="bfb63-111">Riavviare il server in base al nome</span><span class="sxs-lookup"><span data-stu-id="bfb63-111">Restart the server by name</span></span>

### <span data-ttu-id="bfb63-112">Esempio 2: Riavviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="bfb63-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/restart"
PS C:\> Restart-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="bfb63-113">Riavviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="bfb63-113">Restart the server by identity</span></span>

## <span data-ttu-id="bfb63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfb63-114">PARAMETERS</span></span>

### <span data-ttu-id="bfb63-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfb63-115">-AsJob</span></span>
<span data-ttu-id="bfb63-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="bfb63-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bfb63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb63-117">-DefaultProfile</span></span>
<span data-ttu-id="bfb63-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfb63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfb63-119">-InputObject</span></span>
<span data-ttu-id="bfb63-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bfb63-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bfb63-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb63-121">-Name</span></span>
<span data-ttu-id="bfb63-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-122">The name of the server.</span></span>

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

### <span data-ttu-id="bfb63-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bfb63-123">-NoWait</span></span>
<span data-ttu-id="bfb63-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="bfb63-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bfb63-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfb63-125">-PassThru</span></span>
<span data-ttu-id="bfb63-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="bfb63-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bfb63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb63-127">-ResourceGroupName</span></span>
<span data-ttu-id="bfb63-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfb63-128">The name of the resource group.</span></span>
<span data-ttu-id="bfb63-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bfb63-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bfb63-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfb63-130">-SubscriptionId</span></span>
<span data-ttu-id="bfb63-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfb63-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bfb63-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfb63-132">-Confirm</span></span>
<span data-ttu-id="bfb63-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb63-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb63-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb63-134">-WhatIf</span></span>
<span data-ttu-id="bfb63-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb63-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb63-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfb63-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb63-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb63-137">CommonParameters</span></span>
<span data-ttu-id="bfb63-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb63-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb63-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfb63-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb63-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfb63-140">INPUTS</span></span>

### <span data-ttu-id="bfb63-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bfb63-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bfb63-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfb63-142">OUTPUTS</span></span>

### <span data-ttu-id="bfb63-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfb63-143">System.Boolean</span></span>

## <span data-ttu-id="bfb63-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfb63-144">NOTES</span></span>

<span data-ttu-id="bfb63-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bfb63-145">ALIASES</span></span>

<span data-ttu-id="bfb63-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="bfb63-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfb63-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bfb63-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfb63-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfb63-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfb63-149">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="bfb63-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfb63-150">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bfb63-151">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="bfb63-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bfb63-152">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bfb63-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="bfb63-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfb63-154">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bfb63-155">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="bfb63-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bfb63-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfb63-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bfb63-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="bfb63-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="bfb63-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="bfb63-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bfb63-159">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="bfb63-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bfb63-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bfb63-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bfb63-161">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfb63-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bfb63-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfb63-162">RELATED LINKS</span></span>

