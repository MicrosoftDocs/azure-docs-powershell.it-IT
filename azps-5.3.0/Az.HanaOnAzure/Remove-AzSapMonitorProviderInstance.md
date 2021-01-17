---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386872"
---
# <span data-ttu-id="c966f-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="c966f-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="c966f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c966f-102">SYNOPSIS</span></span>
<span data-ttu-id="c966f-103">Elimina un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="c966f-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="c966f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c966f-104">SYNTAX</span></span>

### <span data-ttu-id="c966f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c966f-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c966f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c966f-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c966f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c966f-107">DESCRIPTION</span></span>
<span data-ttu-id="c966f-108">Elimina un'istanza del provider per l'abbonamento, il gruppo di risorse, il nome SapMonitor e il nome della risorsa specificati.</span><span class="sxs-lookup"><span data-stu-id="c966f-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="c966f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c966f-109">EXAMPLES</span></span>

### <span data-ttu-id="c966f-110">Esempio 1: rimuovere l'istanza di SAP monitor per nome</span><span class="sxs-lookup"><span data-stu-id="c966f-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="c966f-111">Questo comando rimuove l'istanza di SAP monitor per nome.</span><span class="sxs-lookup"><span data-stu-id="c966f-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="c966f-112">Esempio 2: rimuovere l'istanza di SAP monitor by Object</span><span class="sxs-lookup"><span data-stu-id="c966f-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="c966f-113">Questo comando rimuove l'istanza di SAP monitor by Object.</span><span class="sxs-lookup"><span data-stu-id="c966f-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="c966f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c966f-114">PARAMETERS</span></span>

### <span data-ttu-id="c966f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c966f-115">-AsJob</span></span>
<span data-ttu-id="c966f-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c966f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c966f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c966f-117">-DefaultProfile</span></span>
<span data-ttu-id="c966f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c966f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c966f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c966f-119">-InputObject</span></span>
<span data-ttu-id="c966f-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c966f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c966f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c966f-121">-Name</span></span>
<span data-ttu-id="c966f-122">Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="c966f-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c966f-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c966f-123">-NoWait</span></span>
<span data-ttu-id="c966f-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c966f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c966f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c966f-125">-PassThru</span></span>
<span data-ttu-id="c966f-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="c966f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c966f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c966f-127">-ResourceGroupName</span></span>
<span data-ttu-id="c966f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c966f-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="c966f-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="c966f-129">-SapMonitorName</span></span>
<span data-ttu-id="c966f-130">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="c966f-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="c966f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c966f-131">-SubscriptionId</span></span>
<span data-ttu-id="c966f-132">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c966f-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c966f-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c966f-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c966f-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c966f-134">-Confirm</span></span>
<span data-ttu-id="c966f-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c966f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c966f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c966f-136">-WhatIf</span></span>
<span data-ttu-id="c966f-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c966f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c966f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c966f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c966f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c966f-139">CommonParameters</span></span>
<span data-ttu-id="c966f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c966f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c966f-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c966f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c966f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c966f-142">INPUTS</span></span>

### <span data-ttu-id="c966f-143">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="c966f-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="c966f-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c966f-144">OUTPUTS</span></span>

### <span data-ttu-id="c966f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c966f-145">System.Boolean</span></span>

## <span data-ttu-id="c966f-146">Note</span><span class="sxs-lookup"><span data-stu-id="c966f-146">NOTES</span></span>

<span data-ttu-id="c966f-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c966f-147">ALIASES</span></span>

<span data-ttu-id="c966f-148">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c966f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c966f-149">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c966f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c966f-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c966f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c966f-151">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c966f-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c966f-152">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c966f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c966f-153">`[Location <String>]`: La posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="c966f-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="c966f-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="c966f-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="c966f-155">`[ProviderInstanceName <String>]`: Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="c966f-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="c966f-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c966f-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c966f-157">`[ResourceName <String>]`: Il nome della risorsa identità.</span><span class="sxs-lookup"><span data-stu-id="c966f-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="c966f-158">`[SapMonitorName <String>]`: Nome della risorsa di monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="c966f-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="c966f-159">`[Scope <String>]`: L'ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c966f-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="c966f-160">Risorsa padre estesa da identità gestite.</span><span class="sxs-lookup"><span data-stu-id="c966f-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="c966f-161">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c966f-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c966f-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c966f-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c966f-163">`[VaultName <String>]`: Nome del Vault</span><span class="sxs-lookup"><span data-stu-id="c966f-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="c966f-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c966f-164">RELATED LINKS</span></span>

