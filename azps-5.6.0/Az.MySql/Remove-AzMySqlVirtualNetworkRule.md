---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 57411a223e96a6aa88c7270e6f23f73f0977e495
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954573"
---
# <span data-ttu-id="39aef-101">Remove-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="39aef-101">Remove-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="39aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39aef-102">SYNOPSIS</span></span>
<span data-ttu-id="39aef-103">Elimina la regola della rete virtuale con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="39aef-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="39aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39aef-104">SYNTAX</span></span>

### <span data-ttu-id="39aef-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39aef-105">Delete (Default)</span></span>
```
Remove-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="39aef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39aef-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39aef-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39aef-107">DESCRIPTION</span></span>
<span data-ttu-id="39aef-108">Elimina la regola della rete virtuale con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="39aef-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="39aef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39aef-109">EXAMPLES</span></span>

### <span data-ttu-id="39aef-110">Esempio 1: Rimuovere la regola di rete virtuale del server MySql in base al nome</span><span class="sxs-lookup"><span data-stu-id="39aef-110">Example 1: Remove MySql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest-ServerName mysql-test

```

<span data-ttu-id="39aef-111">Questo cmdlet rimuove la regola di rete virtuale del server MySql in base al nome.</span><span class="sxs-lookup"><span data-stu-id="39aef-111">This cmdlet removes MySql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="39aef-112">Esempio 2: Rimuovere la regola di rete virtuale del server MySql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="39aef-112">Example 2: Remove MySql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Remove-AzMySqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="39aef-113">Questi cmdlet rimuovono la regola di rete virtuale del server MySql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="39aef-113">These cmdlets remove MySql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="39aef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39aef-114">PARAMETERS</span></span>

### <span data-ttu-id="39aef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39aef-115">-AsJob</span></span>
<span data-ttu-id="39aef-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="39aef-116">Run the command as a job</span></span>

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

### <span data-ttu-id="39aef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39aef-117">-DefaultProfile</span></span>
<span data-ttu-id="39aef-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39aef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39aef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39aef-119">-InputObject</span></span>
<span data-ttu-id="39aef-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="39aef-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39aef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39aef-121">-Name</span></span>
<span data-ttu-id="39aef-122">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39aef-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39aef-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39aef-123">-NoWait</span></span>
<span data-ttu-id="39aef-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="39aef-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39aef-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39aef-125">-PassThru</span></span>
<span data-ttu-id="39aef-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="39aef-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39aef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39aef-127">-ResourceGroupName</span></span>
<span data-ttu-id="39aef-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39aef-128">The name of the resource group.</span></span>
<span data-ttu-id="39aef-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39aef-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="39aef-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="39aef-130">-ServerName</span></span>
<span data-ttu-id="39aef-131">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="39aef-131">The name of the server.</span></span>

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

### <span data-ttu-id="39aef-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39aef-132">-SubscriptionId</span></span>
<span data-ttu-id="39aef-133">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39aef-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="39aef-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39aef-134">-Confirm</span></span>
<span data-ttu-id="39aef-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39aef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39aef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39aef-136">-WhatIf</span></span>
<span data-ttu-id="39aef-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39aef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39aef-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39aef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39aef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39aef-139">CommonParameters</span></span>
<span data-ttu-id="39aef-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39aef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39aef-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39aef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39aef-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="39aef-142">INPUTS</span></span>

### <span data-ttu-id="39aef-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="39aef-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="39aef-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39aef-144">OUTPUTS</span></span>

### <span data-ttu-id="39aef-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39aef-145">System.Boolean</span></span>

## <span data-ttu-id="39aef-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="39aef-146">NOTES</span></span>

<span data-ttu-id="39aef-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="39aef-147">ALIASES</span></span>

<span data-ttu-id="39aef-148">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="39aef-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39aef-149">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="39aef-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39aef-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39aef-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39aef-151">INPUTOBJECT <IMySqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="39aef-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39aef-152">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="39aef-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="39aef-153">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="39aef-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="39aef-154">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="39aef-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="39aef-155">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="39aef-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39aef-156">`[KeyName <String>]`: nome della chiave del server.</span><span class="sxs-lookup"><span data-stu-id="39aef-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="39aef-157">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="39aef-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="39aef-158">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39aef-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39aef-159">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="39aef-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="39aef-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="39aef-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="39aef-161">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="39aef-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="39aef-162">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="39aef-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="39aef-163">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39aef-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="39aef-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39aef-164">RELATED LINKS</span></span>

