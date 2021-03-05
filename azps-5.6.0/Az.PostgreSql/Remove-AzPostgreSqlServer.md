---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlServer.md
ms.openlocfilehash: 9e5cf3c317b2da3ab82073e56272556355deaa79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974701"
---
# <span data-ttu-id="80f84-101">Remove-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="80f84-101">Remove-AzPostgreSqlServer</span></span>

## <span data-ttu-id="80f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f84-102">SYNOPSIS</span></span>
<span data-ttu-id="80f84-103">Elimina un server.</span><span class="sxs-lookup"><span data-stu-id="80f84-103">Deletes a server.</span></span>

## <span data-ttu-id="80f84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80f84-104">SYNTAX</span></span>

### <span data-ttu-id="80f84-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80f84-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80f84-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80f84-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80f84-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="80f84-107">DESCRIPTION</span></span>
<span data-ttu-id="80f84-108">Elimina un server.</span><span class="sxs-lookup"><span data-stu-id="80f84-108">Deletes a server.</span></span>

## <span data-ttu-id="80f84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80f84-109">EXAMPLES</span></span>

### <span data-ttu-id="80f84-110">Esempio 1: Rimuovere il server PostgreSql in base a resourceGroup e al nome del server</span><span class="sxs-lookup"><span data-stu-id="80f84-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="80f84-111">Questo cmdlet rimuove il server PostgreSql in base a resourceGroup e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="80f84-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="80f84-112">Esempio 2: Rimuovere il server PostgreSql in base all'identità</span><span class="sxs-lookup"><span data-stu-id="80f84-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer"
PS C:\> Remove-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="80f84-113">Questi cmdlet rimuovono il server PostgreSql in base all'identità.</span><span class="sxs-lookup"><span data-stu-id="80f84-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="80f84-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80f84-114">PARAMETERS</span></span>

### <span data-ttu-id="80f84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80f84-115">-AsJob</span></span>
<span data-ttu-id="80f84-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="80f84-116">Run the command as a job</span></span>

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

### <span data-ttu-id="80f84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f84-117">-DefaultProfile</span></span>
<span data-ttu-id="80f84-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80f84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80f84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80f84-119">-InputObject</span></span>
<span data-ttu-id="80f84-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="80f84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80f84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80f84-121">-Name</span></span>
<span data-ttu-id="80f84-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="80f84-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80f84-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80f84-123">-NoWait</span></span>
<span data-ttu-id="80f84-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="80f84-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="80f84-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80f84-125">-PassThru</span></span>
<span data-ttu-id="80f84-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="80f84-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="80f84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80f84-127">-ResourceGroupName</span></span>
<span data-ttu-id="80f84-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80f84-128">The name of the resource group.</span></span>
<span data-ttu-id="80f84-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="80f84-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="80f84-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80f84-130">-SubscriptionId</span></span>
<span data-ttu-id="80f84-131">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80f84-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="80f84-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80f84-132">-Confirm</span></span>
<span data-ttu-id="80f84-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80f84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80f84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80f84-134">-WhatIf</span></span>
<span data-ttu-id="80f84-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80f84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80f84-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80f84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80f84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f84-137">CommonParameters</span></span>
<span data-ttu-id="80f84-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f84-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80f84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f84-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="80f84-140">INPUTS</span></span>

### <span data-ttu-id="80f84-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="80f84-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="80f84-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80f84-142">OUTPUTS</span></span>

### <span data-ttu-id="80f84-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80f84-143">System.Boolean</span></span>

## <span data-ttu-id="80f84-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="80f84-144">NOTES</span></span>

<span data-ttu-id="80f84-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="80f84-145">ALIASES</span></span>

<span data-ttu-id="80f84-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="80f84-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80f84-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="80f84-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80f84-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80f84-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80f84-149">INPUTOBJECT <IPostgreSqlIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="80f84-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80f84-150">`[ConfigurationName <String>]`: nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="80f84-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="80f84-151">`[DatabaseName <String>]`: nome del database.</span><span class="sxs-lookup"><span data-stu-id="80f84-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="80f84-152">`[FirewallRuleName <String>]`: nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="80f84-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="80f84-153">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="80f84-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80f84-154">`[LocationName <String>]`: nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="80f84-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="80f84-155">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80f84-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="80f84-156">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="80f84-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="80f84-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: nome del criterio di avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="80f84-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="80f84-158">`[ServerName <String>]`: nome del server.</span><span class="sxs-lookup"><span data-stu-id="80f84-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="80f84-159">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="80f84-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="80f84-160">`[VirtualNetworkRuleName <String>]`: nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="80f84-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="80f84-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80f84-161">RELATED LINKS</span></span>

