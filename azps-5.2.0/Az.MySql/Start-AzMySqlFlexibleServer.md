---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: bdda5653a3b7f612fc96d3522bffe15e92649bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360314"
---
# <span data-ttu-id="f13b3-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="f13b3-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="f13b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f13b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f13b3-103">Avvia un server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-103">Starts a server.</span></span>

## <span data-ttu-id="f13b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f13b3-104">SYNTAX</span></span>

### <span data-ttu-id="f13b3-105">Inizio (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f13b3-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f13b3-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f13b3-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f13b3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f13b3-107">DESCRIPTION</span></span>
<span data-ttu-id="f13b3-108">Avvia un server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-108">Starts a server.</span></span>

## <span data-ttu-id="f13b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f13b3-109">EXAMPLES</span></span>

### <span data-ttu-id="f13b3-110">Esempio 1: avviare il server in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="f13b3-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="f13b3-111">Avviare il server per nome</span><span class="sxs-lookup"><span data-stu-id="f13b3-111">Start the server by name</span></span>

### <span data-ttu-id="f13b3-112">Esempio 2: avviare il server per identità</span><span class="sxs-lookup"><span data-stu-id="f13b3-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="f13b3-113">Avviare il server per identità</span><span class="sxs-lookup"><span data-stu-id="f13b3-113">Start the server by identity</span></span>

## <span data-ttu-id="f13b3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f13b3-114">PARAMETERS</span></span>

### <span data-ttu-id="f13b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f13b3-115">-AsJob</span></span>
<span data-ttu-id="f13b3-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f13b3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f13b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13b3-117">-DefaultProfile</span></span>
<span data-ttu-id="f13b3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f13b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f13b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f13b3-119">-InputObject</span></span>
<span data-ttu-id="f13b3-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f13b3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13b3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f13b3-121">-Name</span></span>
<span data-ttu-id="f13b3-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f13b3-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="f13b3-123">-NoWait</span></span>
<span data-ttu-id="f13b3-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f13b3-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f13b3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f13b3-125">-PassThru</span></span>
<span data-ttu-id="f13b3-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="f13b3-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f13b3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13b3-127">-ResourceGroupName</span></span>
<span data-ttu-id="f13b3-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f13b3-128">The name of the resource group.</span></span>
<span data-ttu-id="f13b3-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f13b3-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f13b3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f13b3-130">-SubscriptionId</span></span>
<span data-ttu-id="f13b3-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f13b3-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f13b3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f13b3-132">-Confirm</span></span>
<span data-ttu-id="f13b3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f13b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13b3-134">-WhatIf</span></span>
<span data-ttu-id="f13b3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f13b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f13b3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f13b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13b3-137">CommonParameters</span></span>
<span data-ttu-id="f13b3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13b3-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f13b3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13b3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f13b3-140">INPUTS</span></span>

### <span data-ttu-id="f13b3-141">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="f13b3-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f13b3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f13b3-142">OUTPUTS</span></span>

### <span data-ttu-id="f13b3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f13b3-143">System.Boolean</span></span>

## <span data-ttu-id="f13b3-144">Note</span><span class="sxs-lookup"><span data-stu-id="f13b3-144">NOTES</span></span>

<span data-ttu-id="f13b3-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f13b3-145">ALIASES</span></span>

<span data-ttu-id="f13b3-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f13b3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f13b3-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f13b3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f13b3-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f13b3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f13b3-149">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f13b3-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f13b3-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f13b3-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="f13b3-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f13b3-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f13b3-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f13b3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f13b3-154">`[KeyName <String>]`: Il nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="f13b3-155">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="f13b3-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f13b3-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f13b3-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f13b3-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f13b3-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="f13b3-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f13b3-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f13b3-159">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="f13b3-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f13b3-160">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f13b3-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f13b3-161">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f13b3-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f13b3-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f13b3-162">RELATED LINKS</span></span>

