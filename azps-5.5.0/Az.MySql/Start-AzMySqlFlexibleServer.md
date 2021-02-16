---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: bdda5653a3b7f612fc96d3522bffe15e92649bbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180031"
---
# <span data-ttu-id="99d1a-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="99d1a-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="99d1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="99d1a-103">Avvia un server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-103">Starts a server.</span></span>

## <span data-ttu-id="99d1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99d1a-104">SYNTAX</span></span>

### <span data-ttu-id="99d1a-105">Start (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99d1a-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99d1a-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="99d1a-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99d1a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99d1a-107">DESCRIPTION</span></span>
<span data-ttu-id="99d1a-108">Avvia un server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-108">Starts a server.</span></span>

## <span data-ttu-id="99d1a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99d1a-109">EXAMPLES</span></span>

### <span data-ttu-id="99d1a-110">Esempio 1: Avviare il server in base al nome della risorsa</span><span class="sxs-lookup"><span data-stu-id="99d1a-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="99d1a-111">Avviare il server in base al nome</span><span class="sxs-lookup"><span data-stu-id="99d1a-111">Start the server by name</span></span>

### <span data-ttu-id="99d1a-112">Esempio 2: Avviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="99d1a-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="99d1a-113">Avviare il server in base all'identità</span><span class="sxs-lookup"><span data-stu-id="99d1a-113">Start the server by identity</span></span>

## <span data-ttu-id="99d1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99d1a-114">PARAMETERS</span></span>

### <span data-ttu-id="99d1a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99d1a-115">-AsJob</span></span>
<span data-ttu-id="99d1a-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="99d1a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="99d1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d1a-117">-DefaultProfile</span></span>
<span data-ttu-id="99d1a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99d1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99d1a-119">-InputObject</span></span>
<span data-ttu-id="99d1a-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="99d1a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99d1a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="99d1a-121">-Name</span></span>
<span data-ttu-id="99d1a-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-122">The name of the server.</span></span>

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

### <span data-ttu-id="99d1a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99d1a-123">-NoWait</span></span>
<span data-ttu-id="99d1a-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="99d1a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="99d1a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99d1a-125">-PassThru</span></span>
<span data-ttu-id="99d1a-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="99d1a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="99d1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="99d1a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99d1a-128">The name of the resource group.</span></span>
<span data-ttu-id="99d1a-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="99d1a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="99d1a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99d1a-130">-SubscriptionId</span></span>
<span data-ttu-id="99d1a-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="99d1a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="99d1a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99d1a-132">-Confirm</span></span>
<span data-ttu-id="99d1a-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d1a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d1a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d1a-134">-WhatIf</span></span>
<span data-ttu-id="99d1a-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99d1a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d1a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99d1a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d1a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d1a-137">CommonParameters</span></span>
<span data-ttu-id="99d1a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d1a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d1a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99d1a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d1a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="99d1a-140">INPUTS</span></span>

### <span data-ttu-id="99d1a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="99d1a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="99d1a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99d1a-142">OUTPUTS</span></span>

### <span data-ttu-id="99d1a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99d1a-143">System.Boolean</span></span>

## <span data-ttu-id="99d1a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="99d1a-144">NOTES</span></span>

<span data-ttu-id="99d1a-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="99d1a-145">ALIASES</span></span>

<span data-ttu-id="99d1a-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="99d1a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99d1a-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="99d1a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99d1a-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99d1a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99d1a-149">INPUTOBJECT <IMySqlIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="99d1a-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="99d1a-150">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="99d1a-151">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="99d1a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="99d1a-152">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="99d1a-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="99d1a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="99d1a-154">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="99d1a-155">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="99d1a-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="99d1a-156">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99d1a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="99d1a-157">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="99d1a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="99d1a-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="99d1a-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="99d1a-159">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="99d1a-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="99d1a-160">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="99d1a-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="99d1a-161">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="99d1a-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="99d1a-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99d1a-162">RELATED LINKS</span></span>

