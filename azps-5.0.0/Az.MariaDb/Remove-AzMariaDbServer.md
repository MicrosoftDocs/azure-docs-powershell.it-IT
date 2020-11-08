---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202104"
---
# <span data-ttu-id="04b7c-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="04b7c-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="04b7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="04b7c-103">Elimina un server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-103">Deletes a server.</span></span>

## <span data-ttu-id="04b7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04b7c-104">SYNTAX</span></span>

### <span data-ttu-id="04b7c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04b7c-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04b7c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04b7c-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04b7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04b7c-107">DESCRIPTION</span></span>
<span data-ttu-id="04b7c-108">Elimina un server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-108">Deletes a server.</span></span>

## <span data-ttu-id="04b7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="04b7c-110">Esempio 1: rimuovere un MariaDB</span><span class="sxs-lookup"><span data-stu-id="04b7c-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="04b7c-111">Questo comando rimuove un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="04b7c-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="04b7c-112">Esempio 2: rimuovere un MariaDB</span><span class="sxs-lookup"><span data-stu-id="04b7c-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="04b7c-113">Questo comando rimuove un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="04b7c-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="04b7c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04b7c-114">PARAMETERS</span></span>

### <span data-ttu-id="04b7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04b7c-115">-AsJob</span></span>
<span data-ttu-id="04b7c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="04b7c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="04b7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b7c-117">-DefaultProfile</span></span>
<span data-ttu-id="04b7c-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04b7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04b7c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04b7c-119">-InputObject</span></span>
<span data-ttu-id="04b7c-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="04b7c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04b7c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="04b7c-121">-Name</span></span>
<span data-ttu-id="04b7c-122">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-122">The name of the server.</span></span>

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

### <span data-ttu-id="04b7c-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="04b7c-123">-NoWait</span></span>
<span data-ttu-id="04b7c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="04b7c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04b7c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04b7c-125">-PassThru</span></span>
<span data-ttu-id="04b7c-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="04b7c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="04b7c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b7c-127">-ResourceGroupName</span></span>
<span data-ttu-id="04b7c-128">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="04b7c-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="04b7c-129">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="04b7c-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="04b7c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04b7c-130">-SubscriptionId</span></span>
<span data-ttu-id="04b7c-131">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="04b7c-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="04b7c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04b7c-132">-Confirm</span></span>
<span data-ttu-id="04b7c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b7c-134">-WhatIf</span></span>
<span data-ttu-id="04b7c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04b7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b7c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04b7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b7c-137">CommonParameters</span></span>
<span data-ttu-id="04b7c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b7c-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04b7c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b7c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04b7c-140">INPUTS</span></span>

### <span data-ttu-id="04b7c-141">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="04b7c-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="04b7c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04b7c-142">OUTPUTS</span></span>

### <span data-ttu-id="04b7c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04b7c-143">System.Boolean</span></span>

## <span data-ttu-id="04b7c-144">Note</span><span class="sxs-lookup"><span data-stu-id="04b7c-144">NOTES</span></span>

<span data-ttu-id="04b7c-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="04b7c-145">ALIASES</span></span>

<span data-ttu-id="04b7c-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04b7c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04b7c-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="04b7c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04b7c-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="04b7c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04b7c-149">INPUTOBJECT <IMariaDbIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="04b7c-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04b7c-150">`[ConfigurationName <String>]`: Nome della configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="04b7c-151">`[DatabaseName <String>]`: Nome del database.</span><span class="sxs-lookup"><span data-stu-id="04b7c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="04b7c-152">`[FirewallRuleName <String>]`: Nome della regola del firewall del server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="04b7c-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="04b7c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04b7c-154">`[LocationName <String>]`: Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="04b7c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="04b7c-155">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="04b7c-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="04b7c-156">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="04b7c-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="04b7c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Nome del criterio di avviso per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="04b7c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="04b7c-158">`[ServerName <String>]`: Nome del server.</span><span class="sxs-lookup"><span data-stu-id="04b7c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="04b7c-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="04b7c-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="04b7c-160">`[VirtualNetworkRuleName <String>]`: Nome della regola di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="04b7c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="04b7c-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04b7c-161">RELATED LINKS</span></span>

