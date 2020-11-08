---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030175"
---
# <span data-ttu-id="859f3-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="859f3-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="859f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="859f3-102">SYNOPSIS</span></span>
<span data-ttu-id="859f3-103">Scala un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="859f3-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="859f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="859f3-104">SYNTAX</span></span>

### <span data-ttu-id="859f3-105">ScaleExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="859f3-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="859f3-106">Scala</span><span class="sxs-lookup"><span data-stu-id="859f3-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="859f3-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="859f3-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="859f3-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="859f3-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="859f3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="859f3-109">DESCRIPTION</span></span>
<span data-ttu-id="859f3-110">Scala un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="859f3-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="859f3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="859f3-111">EXAMPLES</span></span>

### <span data-ttu-id="859f3-112">Esempio 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="859f3-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="859f3-113">Aggiungere un nuovo nodo unità di scala al cluster di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="859f3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="859f3-114">PARAMETERS</span></span>

### <span data-ttu-id="859f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="859f3-115">-AsJob</span></span>
<span data-ttu-id="859f3-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="859f3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="859f3-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="859f3-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="859f3-118">Il contrassegno indica se l'operazione deve attendere lo spazio di archiviazione per confluire prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="859f3-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859f3-119">-DefaultProfile</span></span>
<span data-ttu-id="859f3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="859f3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="859f3-121">-InputObject</span></span>
<span data-ttu-id="859f3-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="859f3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="859f3-123">-Location</span></span>
<span data-ttu-id="859f3-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="859f3-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="859f3-125">-BmciPv4Address</span></span> 
<span data-ttu-id="859f3-126">Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="859f3-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="859f3-127">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="859f3-127">-ComputerName</span></span> 
<span data-ttu-id="859f3-128">Nome computer della macchina fisica.</span><span class="sxs-lookup"><span data-stu-id="859f3-128">Computer name of the physical machine.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="859f3-129">-NoWait</span></span>
<span data-ttu-id="859f3-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="859f3-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="859f3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="859f3-131">-PassThru</span></span>
<span data-ttu-id="859f3-132">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="859f3-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="859f3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859f3-133">-ResourceGroupName</span></span>
<span data-ttu-id="859f3-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="859f3-134">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="859f3-135">-ScaleUnit</span></span>
<span data-ttu-id="859f3-136">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-136">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="859f3-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="859f3-138">Elenco di dati di input che consente di aggiungere un set di nodi di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="859f3-139">Per costruire, vedere la sezione Note per le proprietà di SCALEUNITNODEPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="859f3-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="859f3-140">-SubscriptionId</span></span>
<span data-ttu-id="859f3-141">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="859f3-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="859f3-142">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="859f3-142">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="859f3-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="859f3-143">-Confirm</span></span>
<span data-ttu-id="859f3-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="859f3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859f3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859f3-145">-WhatIf</span></span>
<span data-ttu-id="859f3-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="859f3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="859f3-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="859f3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859f3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859f3-148">CommonParameters</span></span>
<span data-ttu-id="859f3-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859f3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859f3-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="859f3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859f3-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="859f3-151">INPUTS</span></span>

### <span data-ttu-id="859f3-152">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="859f3-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="859f3-153">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="859f3-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="859f3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="859f3-154">OUTPUTS</span></span>

### <span data-ttu-id="859f3-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="859f3-155">System.Boolean</span></span>

## <span data-ttu-id="859f3-156">Note</span><span class="sxs-lookup"><span data-stu-id="859f3-156">NOTES</span></span>

<span data-ttu-id="859f3-157">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="859f3-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="859f3-158">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="859f3-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="859f3-159">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="859f3-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="859f3-160">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="859f3-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="859f3-161">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="859f3-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="859f3-162">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="859f3-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="859f3-163">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="859f3-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="859f3-164">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="859f3-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="859f3-165">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="859f3-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="859f3-166">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="859f3-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="859f3-167">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="859f3-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="859f3-168">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="859f3-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="859f3-169">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="859f3-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="859f3-170">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="859f3-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="859f3-171">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="859f3-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="859f3-172">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="859f3-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="859f3-173">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="859f3-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="859f3-174">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="859f3-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="859f3-175">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="859f3-176">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="859f3-177">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="859f3-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="859f3-178">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="859f3-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="859f3-179">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="859f3-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="859f3-180">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="859f3-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="859f3-181">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="859f3-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="859f3-182">NODELIST <IScaleOutScaleUnitParameters [] >: elenco dei nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="859f3-183">`[BmciPv4Address <String>]`: Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="859f3-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="859f3-184">`[ComputerName <String>]`: Nome computer della macchina fisica.</span><span class="sxs-lookup"><span data-stu-id="859f3-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="859f3-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : elenco di dati di input che consente di aggiungere un set di nodi di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="859f3-186">`[AwaitStorageConvergence <Boolean?>]`: Contrassegno indica se l'operazione deve attendere lo spazio di archiviazione per confluire prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="859f3-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="859f3-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Elenco dei nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="859f3-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="859f3-188">`[BmciPv4Address <String>]`: Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="859f3-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="859f3-189">`[ComputerName <String>]`: Nome computer della macchina fisica.</span><span class="sxs-lookup"><span data-stu-id="859f3-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="859f3-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="859f3-190">RELATED LINKS</span></span>
