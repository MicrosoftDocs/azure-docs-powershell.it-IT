---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 1036fb17cb83e28a76e4765b5fc64d703c2e014b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189740"
---
# <span data-ttu-id="ca5df-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca5df-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="ca5df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca5df-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5df-103">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="ca5df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca5df-104">SYNTAX</span></span>

### <span data-ttu-id="ca5df-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca5df-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ca5df-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca5df-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca5df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca5df-107">DESCRIPTION</span></span>
<span data-ttu-id="ca5df-108">Elimina una regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="ca5df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca5df-109">EXAMPLES</span></span>

### <span data-ttu-id="ca5df-110">Esempio 1: rimuovere la regola del firewall MySql per nome</span><span class="sxs-lookup"><span data-stu-id="ca5df-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="ca5df-111">Questo cmdlet rimuove la regola del firewall MySql per nome.</span><span class="sxs-lookup"><span data-stu-id="ca5df-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="ca5df-112">Esempio 2: rimuovere la regola del firewall MySql per identità</span><span class="sxs-lookup"><span data-stu-id="ca5df-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="ca5df-113">Questi cmdlet eliminano la regola del firewall MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="ca5df-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="ca5df-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca5df-114">PARAMETERS</span></span>

### <span data-ttu-id="ca5df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca5df-115">-AsJob</span></span>
<span data-ttu-id="ca5df-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ca5df-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ca5df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5df-117">-DefaultProfile</span></span>
<span data-ttu-id="ca5df-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca5df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca5df-119">-InputObject</span></span>
<span data-ttu-id="ca5df-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ca5df-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5df-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca5df-121">-Name</span></span>
<span data-ttu-id="ca5df-122">Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5df-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ca5df-123">-NoWait</span></span>
<span data-ttu-id="ca5df-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ca5df-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ca5df-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca5df-125">-PassThru</span></span>
<span data-ttu-id="ca5df-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="ca5df-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca5df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5df-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca5df-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca5df-128">The name of the resource group.</span></span>
<span data-ttu-id="ca5df-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca5df-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5df-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ca5df-130">-ServerName</span></span>
<span data-ttu-id="ca5df-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5df-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca5df-132">-SubscriptionId</span></span>
<span data-ttu-id="ca5df-133">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca5df-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5df-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca5df-134">-Confirm</span></span>
<span data-ttu-id="ca5df-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca5df-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca5df-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5df-136">-WhatIf</span></span>
<span data-ttu-id="ca5df-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca5df-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca5df-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca5df-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca5df-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5df-139">CommonParameters</span></span>
<span data-ttu-id="ca5df-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5df-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5df-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca5df-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5df-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca5df-142">INPUTS</span></span>

### <span data-ttu-id="ca5df-143">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ca5df-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ca5df-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca5df-144">OUTPUTS</span></span>

### <span data-ttu-id="ca5df-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca5df-145">System.Boolean</span></span>

## <span data-ttu-id="ca5df-146">Note</span><span class="sxs-lookup"><span data-stu-id="ca5df-146">NOTES</span></span>

<span data-ttu-id="ca5df-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ca5df-147">ALIASES</span></span>

<span data-ttu-id="ca5df-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca5df-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca5df-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ca5df-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca5df-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca5df-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca5df-151">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ca5df-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca5df-152">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ca5df-153">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="ca5df-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ca5df-154">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ca5df-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ca5df-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca5df-156">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="ca5df-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ca5df-157">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca5df-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca5df-158">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="ca5df-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca5df-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ca5df-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ca5df-160">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="ca5df-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ca5df-161">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ca5df-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca5df-162">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca5df-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ca5df-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca5df-163">RELATED LINKS</span></span>

