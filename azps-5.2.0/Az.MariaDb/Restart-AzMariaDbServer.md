---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326729"
---
# <span data-ttu-id="38da4-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="38da4-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="38da4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38da4-102">SYNOPSIS</span></span>
<span data-ttu-id="38da4-103">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="38da4-103">Restarts a server.</span></span>

## <span data-ttu-id="38da4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38da4-104">SYNTAX</span></span>

### <span data-ttu-id="38da4-105">Nomeserver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38da4-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="38da4-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="38da4-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38da4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38da4-107">DESCRIPTION</span></span>
<span data-ttu-id="38da4-108">Riavvia un server.</span><span class="sxs-lookup"><span data-stu-id="38da4-108">Restarts a server.</span></span>

## <span data-ttu-id="38da4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38da4-109">EXAMPLES</span></span>

### <span data-ttu-id="38da4-110">Esempio 1: riavviare un MariaDB</span><span class="sxs-lookup"><span data-stu-id="38da4-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="38da4-111">Questo comando Riavvia un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="38da4-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="38da4-112">Esempio 2: riavviare un MariaDB</span><span class="sxs-lookup"><span data-stu-id="38da4-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="38da4-113">Questo comando Riavvia un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="38da4-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="38da4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38da4-114">PARAMETERS</span></span>

### <span data-ttu-id="38da4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38da4-115">-AsJob</span></span>
<span data-ttu-id="38da4-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="38da4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="38da4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38da4-117">-DefaultProfile</span></span>
<span data-ttu-id="38da4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38da4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38da4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38da4-119">-InputObject</span></span>
<span data-ttu-id="38da4-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="38da4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38da4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="38da4-121">-Name</span></span>
<span data-ttu-id="38da4-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="38da4-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38da4-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="38da4-123">-NoWait</span></span>
<span data-ttu-id="38da4-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="38da4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38da4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38da4-125">-PassThru</span></span>
<span data-ttu-id="38da4-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="38da4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="38da4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38da4-127">-ResourceGroupName</span></span>
<span data-ttu-id="38da4-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="38da4-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="38da4-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="38da4-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38da4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38da4-130">-SubscriptionId</span></span>
<span data-ttu-id="38da4-131">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="38da4-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38da4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38da4-132">-Confirm</span></span>
<span data-ttu-id="38da4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38da4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38da4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38da4-134">-WhatIf</span></span>
<span data-ttu-id="38da4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38da4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38da4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38da4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38da4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38da4-137">CommonParameters</span></span>
<span data-ttu-id="38da4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38da4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38da4-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38da4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38da4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38da4-140">INPUTS</span></span>

### <span data-ttu-id="38da4-141">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="38da4-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="38da4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38da4-142">OUTPUTS</span></span>

### <span data-ttu-id="38da4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38da4-143">System.Boolean</span></span>

## <span data-ttu-id="38da4-144">Note</span><span class="sxs-lookup"><span data-stu-id="38da4-144">NOTES</span></span>

<span data-ttu-id="38da4-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="38da4-145">ALIASES</span></span>

<span data-ttu-id="38da4-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38da4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38da4-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="38da4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38da4-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38da4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38da4-149">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="38da4-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38da4-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="38da4-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="38da4-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="38da4-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="38da4-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="38da4-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="38da4-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="38da4-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38da4-154">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="38da4-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="38da4-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="38da4-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="38da4-156">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="38da4-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="38da4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="38da4-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="38da4-158">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="38da4-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="38da4-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="38da4-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="38da4-160">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="38da4-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="38da4-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38da4-161">RELATED LINKS</span></span>

