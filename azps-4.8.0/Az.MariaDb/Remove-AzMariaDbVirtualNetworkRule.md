---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033015"
---
# <span data-ttu-id="c65c3-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c65c3-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="c65c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c65c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c65c3-103">Elimina la regola di rete virtuale con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="c65c3-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="c65c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c65c3-104">SYNTAX</span></span>

### <span data-ttu-id="c65c3-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c65c3-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c65c3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c65c3-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c65c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c65c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c65c3-108">Elimina la regola di rete virtuale con il nome indicato.</span><span class="sxs-lookup"><span data-stu-id="c65c3-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="c65c3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c65c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c65c3-110">Esempio 1: rimuovere una regola di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c65c3-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="c65c3-111">Questo comando rimuove una regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c65c3-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="c65c3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c65c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c65c3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c65c3-113">-AsJob</span></span>
<span data-ttu-id="c65c3-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c65c3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c65c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65c3-115">-DefaultProfile</span></span>
<span data-ttu-id="c65c3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c65c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65c3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65c3-117">-InputObject</span></span>
<span data-ttu-id="c65c3-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c65c3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c65c3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c65c3-119">-Name</span></span>
<span data-ttu-id="c65c3-120">Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c65c3-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c65c3-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c65c3-121">-NoWait</span></span>
<span data-ttu-id="c65c3-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c65c3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c65c3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c65c3-123">-PassThru</span></span>
<span data-ttu-id="c65c3-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="c65c3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c65c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c65c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="c65c3-126">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c65c3-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c65c3-127">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c65c3-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c65c3-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c65c3-128">-ServerName</span></span>
<span data-ttu-id="c65c3-129">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="c65c3-129">The name of the server.</span></span>

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

### <span data-ttu-id="c65c3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c65c3-130">-SubscriptionId</span></span>
<span data-ttu-id="c65c3-131">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c65c3-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c65c3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c65c3-132">-Confirm</span></span>
<span data-ttu-id="c65c3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c65c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c65c3-134">-WhatIf</span></span>
<span data-ttu-id="c65c3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c65c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c65c3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c65c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65c3-137">CommonParameters</span></span>
<span data-ttu-id="c65c3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65c3-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c65c3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65c3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c65c3-140">INPUTS</span></span>

### <span data-ttu-id="c65c3-141">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="c65c3-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="c65c3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c65c3-142">OUTPUTS</span></span>

### <span data-ttu-id="c65c3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c65c3-143">System.Boolean</span></span>

## <span data-ttu-id="c65c3-144">Note</span><span class="sxs-lookup"><span data-stu-id="c65c3-144">NOTES</span></span>

<span data-ttu-id="c65c3-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c65c3-145">ALIASES</span></span>

<span data-ttu-id="c65c3-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c65c3-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c65c3-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c65c3-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c65c3-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c65c3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c65c3-149">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c65c3-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c65c3-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="c65c3-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c65c3-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="c65c3-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c65c3-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="c65c3-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c65c3-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c65c3-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c65c3-154">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="c65c3-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c65c3-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c65c3-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c65c3-156">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="c65c3-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c65c3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c65c3-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c65c3-158">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="c65c3-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c65c3-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="c65c3-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="c65c3-160">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c65c3-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c65c3-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c65c3-161">RELATED LINKS</span></span>

