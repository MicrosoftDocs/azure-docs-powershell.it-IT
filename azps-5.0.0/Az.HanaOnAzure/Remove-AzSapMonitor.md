---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193299"
---
# <span data-ttu-id="f36a2-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="f36a2-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="f36a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f36a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f36a2-103">Elimina un monitor SAP con l'abbonamento, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="f36a2-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="f36a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f36a2-104">SYNTAX</span></span>

### <span data-ttu-id="f36a2-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f36a2-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f36a2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f36a2-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f36a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f36a2-107">DESCRIPTION</span></span>
<span data-ttu-id="f36a2-108">Elimina un monitor SAP con l'abbonamento, il gruppo di risorse e il nome del monitor specificati.</span><span class="sxs-lookup"><span data-stu-id="f36a2-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="f36a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f36a2-109">EXAMPLES</span></span>

### <span data-ttu-id="f36a2-110">Esempio 1: rimuovere un monitor SAP per nome</span><span class="sxs-lookup"><span data-stu-id="f36a2-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="f36a2-111">Questo comando rimuove un monitor SAP per nome.</span><span class="sxs-lookup"><span data-stu-id="f36a2-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="f36a2-112">Esempio 2: rimuovere un monitor SAP per oggetto</span><span class="sxs-lookup"><span data-stu-id="f36a2-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="f36a2-113">Questo comando rimuove un monitor SAP per oggetto.</span><span class="sxs-lookup"><span data-stu-id="f36a2-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="f36a2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f36a2-114">PARAMETERS</span></span>

### <span data-ttu-id="f36a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f36a2-115">-AsJob</span></span>
<span data-ttu-id="f36a2-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f36a2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f36a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36a2-117">-DefaultProfile</span></span>
<span data-ttu-id="f36a2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f36a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f36a2-119">-InputObject</span></span>
<span data-ttu-id="f36a2-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f36a2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f36a2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f36a2-121">-Name</span></span>
<span data-ttu-id="f36a2-122">Nome della risorsa monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="f36a2-122">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f36a2-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="f36a2-123">-NoWait</span></span>
<span data-ttu-id="f36a2-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f36a2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f36a2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f36a2-125">-PassThru</span></span>
<span data-ttu-id="f36a2-126">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="f36a2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f36a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="f36a2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f36a2-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="f36a2-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f36a2-129">-SubscriptionId</span></span>
<span data-ttu-id="f36a2-130">ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f36a2-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f36a2-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f36a2-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f36a2-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f36a2-132">-Confirm</span></span>
<span data-ttu-id="f36a2-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f36a2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f36a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36a2-134">-WhatIf</span></span>
<span data-ttu-id="f36a2-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f36a2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36a2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f36a2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f36a2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36a2-137">CommonParameters</span></span>
<span data-ttu-id="f36a2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f36a2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36a2-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f36a2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36a2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f36a2-140">INPUTS</span></span>

### <span data-ttu-id="f36a2-141">Microsoft. Azure. PowerShell. Cmdlets. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="f36a2-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f36a2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f36a2-142">OUTPUTS</span></span>

### <span data-ttu-id="f36a2-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f36a2-143">System.Boolean</span></span>

## <span data-ttu-id="f36a2-144">Note</span><span class="sxs-lookup"><span data-stu-id="f36a2-144">NOTES</span></span>

<span data-ttu-id="f36a2-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f36a2-145">ALIASES</span></span>

<span data-ttu-id="f36a2-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f36a2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f36a2-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f36a2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f36a2-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f36a2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f36a2-149">INPUTOBJECT <IHanaOnAzureIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f36a2-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f36a2-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f36a2-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f36a2-151">`[Location <String>]`: La posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="f36a2-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f36a2-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Nome dell'operazione</span><span class="sxs-lookup"><span data-stu-id="f36a2-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f36a2-153">`[ProviderInstanceName <String>]`: Nome dell'istanza del provider.</span><span class="sxs-lookup"><span data-stu-id="f36a2-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f36a2-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f36a2-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f36a2-155">`[ResourceName <String>]`: Il nome della risorsa identità.</span><span class="sxs-lookup"><span data-stu-id="f36a2-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f36a2-156">`[SapMonitorName <String>]`: Nome della risorsa di monitoraggio SAP.</span><span class="sxs-lookup"><span data-stu-id="f36a2-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f36a2-157">`[Scope <String>]`: L'ambito del provider di risorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f36a2-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f36a2-158">Risorsa padre estesa da identità gestite.</span><span class="sxs-lookup"><span data-stu-id="f36a2-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f36a2-159">`[SubscriptionId <String>]`: ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f36a2-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f36a2-160">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f36a2-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f36a2-161">`[VaultName <String>]`: Nome del Vault</span><span class="sxs-lookup"><span data-stu-id="f36a2-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f36a2-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f36a2-162">RELATED LINKS</span></span>
