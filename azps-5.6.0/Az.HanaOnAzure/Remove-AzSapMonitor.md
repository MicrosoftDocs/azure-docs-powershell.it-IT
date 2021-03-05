---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: e06cfbb595f9302bf4c7d90846e5a847a24f9322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013342"
---
# <span data-ttu-id="c16fe-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="c16fe-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="c16fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c16fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c16fe-103">Elimina un monitor SAP con la sottoscrizione, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="c16fe-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="c16fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c16fe-104">SYNTAX</span></span>

### <span data-ttu-id="c16fe-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c16fe-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c16fe-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c16fe-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c16fe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c16fe-107">DESCRIPTION</span></span>
<span data-ttu-id="c16fe-108">Elimina un monitor SAP con la sottoscrizione, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="c16fe-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="c16fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c16fe-109">EXAMPLES</span></span>

### <span data-ttu-id="c16fe-110">Esempio 1: Rimuovere un monitor SAP in base al nome</span><span class="sxs-lookup"><span data-stu-id="c16fe-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="c16fe-111">Questo comando rimuove un monitor SAP in base al nome.</span><span class="sxs-lookup"><span data-stu-id="c16fe-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="c16fe-112">Esempio 2: Rimuovere un monitor SAP per oggetto</span><span class="sxs-lookup"><span data-stu-id="c16fe-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="c16fe-113">Questo comando rimuove un monitor SAP per oggetto.</span><span class="sxs-lookup"><span data-stu-id="c16fe-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="c16fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c16fe-114">PARAMETERS</span></span>

### <span data-ttu-id="c16fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c16fe-115">-AsJob</span></span>
<span data-ttu-id="c16fe-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c16fe-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c16fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16fe-117">-DefaultProfile</span></span>
<span data-ttu-id="c16fe-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c16fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c16fe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c16fe-119">-InputObject</span></span>
<span data-ttu-id="c16fe-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c16fe-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c16fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c16fe-121">-Name</span></span>
<span data-ttu-id="c16fe-122">Nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="c16fe-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c16fe-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c16fe-123">-NoWait</span></span>
<span data-ttu-id="c16fe-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c16fe-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c16fe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c16fe-125">-PassThru</span></span>
<span data-ttu-id="c16fe-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c16fe-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c16fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c16fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="c16fe-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c16fe-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="c16fe-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c16fe-129">-SubscriptionId</span></span>
<span data-ttu-id="c16fe-130">ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c16fe-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c16fe-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c16fe-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c16fe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c16fe-132">-Confirm</span></span>
<span data-ttu-id="c16fe-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c16fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c16fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16fe-134">-WhatIf</span></span>
<span data-ttu-id="c16fe-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c16fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c16fe-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c16fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c16fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16fe-137">CommonParameters</span></span>
<span data-ttu-id="c16fe-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c16fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16fe-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c16fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16fe-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="c16fe-140">INPUTS</span></span>

### <span data-ttu-id="c16fe-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="c16fe-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="c16fe-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c16fe-142">OUTPUTS</span></span>

### <span data-ttu-id="c16fe-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c16fe-143">System.Boolean</span></span>

## <span data-ttu-id="c16fe-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="c16fe-144">NOTES</span></span>

<span data-ttu-id="c16fe-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c16fe-145">ALIASES</span></span>

<span data-ttu-id="c16fe-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="c16fe-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c16fe-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c16fe-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c16fe-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c16fe-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c16fe-149">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c16fe-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c16fe-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="c16fe-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c16fe-151">`[Location <String>]`: posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="c16fe-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="c16fe-152">`[OperationKind <AccessPolicyUpdateKind?>]`: nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="c16fe-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="c16fe-153">`[ProviderInstanceName <String>]`: nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="c16fe-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="c16fe-154">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c16fe-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c16fe-155">`[ResourceName <String>]`: nome della risorsa di identità.</span><span class="sxs-lookup"><span data-stu-id="c16fe-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="c16fe-156">`[SapMonitorName <String>]`: nome della risorsa monitor SAP.</span><span class="sxs-lookup"><span data-stu-id="c16fe-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="c16fe-157">`[Scope <String>]`: ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c16fe-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="c16fe-158">Risorsa padre estesa da Identità gestite.</span><span class="sxs-lookup"><span data-stu-id="c16fe-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="c16fe-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c16fe-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c16fe-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c16fe-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c16fe-161">`[VaultName <String>]`: nome del vault</span><span class="sxs-lookup"><span data-stu-id="c16fe-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="c16fe-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c16fe-162">RELATED LINKS</span></span>

