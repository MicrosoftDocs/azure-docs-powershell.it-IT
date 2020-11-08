---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 3766211a5ac69c416e2b36dd272dfd140193e848
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032441"
---
# <span data-ttu-id="53826-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="53826-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="53826-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53826-102">SYNOPSIS</span></span>
<span data-ttu-id="53826-103">Elimina la soluzione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="53826-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="53826-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53826-104">SYNTAX</span></span>

### <span data-ttu-id="53826-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53826-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53826-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="53826-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53826-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53826-107">DESCRIPTION</span></span>
<span data-ttu-id="53826-108">Elimina la soluzione nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="53826-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="53826-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53826-109">EXAMPLES</span></span>

### <span data-ttu-id="53826-110">Esempio 1: rimuovere una soluzione di analisi del log di monitoraggio per nome</span><span class="sxs-lookup"><span data-stu-id="53826-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="53826-111">Questo comando rimuove una soluzione di analisi del log di monitoraggio per nome.</span><span class="sxs-lookup"><span data-stu-id="53826-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="53826-112">Esempio 2: rimuovere una soluzione di analisi del log di monitoraggio per oggetto</span><span class="sxs-lookup"><span data-stu-id="53826-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="53826-113">Questo comando rimuove una soluzione di analisi del log di monitoraggio per oggetto.</span><span class="sxs-lookup"><span data-stu-id="53826-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="53826-114">Esempio 3: rimuovere una soluzione di analisi del log di monitoraggio tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="53826-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="53826-115">Questo comando rimuove una soluzione di analisi del log di monitoraggio tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="53826-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="53826-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53826-116">PARAMETERS</span></span>

### <span data-ttu-id="53826-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53826-117">-DefaultProfile</span></span>
<span data-ttu-id="53826-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53826-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53826-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53826-119">-InputObject</span></span>
<span data-ttu-id="53826-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="53826-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53826-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="53826-121">-Name</span></span>
<span data-ttu-id="53826-122">Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="53826-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53826-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53826-123">-PassThru</span></span>
<span data-ttu-id="53826-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="53826-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="53826-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53826-125">-ResourceGroupName</span></span>
<span data-ttu-id="53826-126">Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="53826-126">The name of the resource group to get.</span></span>
<span data-ttu-id="53826-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="53826-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="53826-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53826-128">-SubscriptionId</span></span>
<span data-ttu-id="53826-129">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53826-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="53826-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="53826-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="53826-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53826-131">-Confirm</span></span>
<span data-ttu-id="53826-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53826-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53826-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53826-133">-WhatIf</span></span>
<span data-ttu-id="53826-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53826-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53826-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53826-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53826-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53826-136">CommonParameters</span></span>
<span data-ttu-id="53826-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53826-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53826-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53826-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53826-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53826-139">INPUTS</span></span>

### <span data-ttu-id="53826-140">Microsoft. Azure. PowerShell. Cmdlets. MonitoringSolutions. Models. IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="53826-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="53826-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53826-141">OUTPUTS</span></span>

### <span data-ttu-id="53826-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53826-142">System.Boolean</span></span>

## <span data-ttu-id="53826-143">Note</span><span class="sxs-lookup"><span data-stu-id="53826-143">NOTES</span></span>

<span data-ttu-id="53826-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="53826-144">ALIASES</span></span>

<span data-ttu-id="53826-145">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53826-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53826-146">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="53826-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53826-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53826-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53826-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="53826-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53826-149">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="53826-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53826-150">`[ManagementAssociationName <String>]`: Nome ManagementAssociation utente.</span><span class="sxs-lookup"><span data-stu-id="53826-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="53826-151">`[ManagementConfigurationName <String>]`: Nome configurazione gestione utenti.</span><span class="sxs-lookup"><span data-stu-id="53826-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="53826-152">`[ProviderName <String>]`: Nome provider per la risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="53826-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="53826-153">`[ResourceGroupName <String>]`: Nome del gruppo di risorse da ottenere.</span><span class="sxs-lookup"><span data-stu-id="53826-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="53826-154">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="53826-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="53826-155">`[ResourceName <String>]`: Nome risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="53826-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="53826-156">`[ResourceType <String>]`: Tipo di risorsa per la risorsa padre</span><span class="sxs-lookup"><span data-stu-id="53826-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="53826-157">`[SolutionName <String>]`: Nome soluzione utente.</span><span class="sxs-lookup"><span data-stu-id="53826-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="53826-158">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="53826-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="53826-159">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="53826-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="53826-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53826-160">RELATED LINKS</span></span>

