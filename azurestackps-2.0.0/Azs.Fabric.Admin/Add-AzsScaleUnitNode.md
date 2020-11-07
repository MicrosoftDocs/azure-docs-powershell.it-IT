---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863998"
---
# <span data-ttu-id="835a7-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="835a7-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="835a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="835a7-102">SYNOPSIS</span></span>
<span data-ttu-id="835a7-103">Scala un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="835a7-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="835a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="835a7-104">SYNTAX</span></span>

### <span data-ttu-id="835a7-105">ScaleExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="835a7-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="835a7-106">Scala</span><span class="sxs-lookup"><span data-stu-id="835a7-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="835a7-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="835a7-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="835a7-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="835a7-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="835a7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="835a7-109">DESCRIPTION</span></span>
<span data-ttu-id="835a7-110">Scala un'unità di misura.</span><span class="sxs-lookup"><span data-stu-id="835a7-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="835a7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="835a7-111">EXAMPLES</span></span>

### <span data-ttu-id="835a7-112">Esempio 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="835a7-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="835a7-113">Aggiungere un nuovo nodo unità di scala al cluster di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="835a7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="835a7-114">PARAMETERS</span></span>

### <span data-ttu-id="835a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="835a7-115">-AsJob</span></span>
<span data-ttu-id="835a7-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="835a7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="835a7-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="835a7-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="835a7-118">Il contrassegno indica se l'operazione deve attendere lo spazio di archiviazione per confluire prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="835a7-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="835a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835a7-119">-DefaultProfile</span></span>
<span data-ttu-id="835a7-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="835a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="835a7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="835a7-121">-InputObject</span></span>
<span data-ttu-id="835a7-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="835a7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="835a7-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="835a7-123">-Location</span></span>
<span data-ttu-id="835a7-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="835a7-124">Location of the resource.</span></span>

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

### <span data-ttu-id="835a7-125">-NodeList</span><span class="sxs-lookup"><span data-stu-id="835a7-125">-NodeList</span></span>
<span data-ttu-id="835a7-126">Elenco di nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="835a7-127">Per creare una tabella hash, vedere la sezione Note per le proprietà dei NODELIST.</span><span class="sxs-lookup"><span data-stu-id="835a7-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="835a7-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="835a7-128">-NoWait</span></span>
<span data-ttu-id="835a7-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="835a7-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="835a7-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="835a7-130">-PassThru</span></span>
<span data-ttu-id="835a7-131">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="835a7-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="835a7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835a7-132">-ResourceGroupName</span></span>
<span data-ttu-id="835a7-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="835a7-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="835a7-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="835a7-134">-ScaleUnit</span></span>
<span data-ttu-id="835a7-135">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-135">Name of the scale units.</span></span>

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

### <span data-ttu-id="835a7-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="835a7-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="835a7-137">Elenco di dati di input che consente di aggiungere un set di nodi di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="835a7-138">Per costruire, vedere la sezione Note per le proprietà di SCALEUNITNODEPARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="835a7-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="835a7-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="835a7-139">-SubscriptionId</span></span>
<span data-ttu-id="835a7-140">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="835a7-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="835a7-141">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="835a7-141">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="835a7-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="835a7-142">-Confirm</span></span>
<span data-ttu-id="835a7-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="835a7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="835a7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="835a7-144">-WhatIf</span></span>
<span data-ttu-id="835a7-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="835a7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="835a7-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="835a7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="835a7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835a7-147">CommonParameters</span></span>
<span data-ttu-id="835a7-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835a7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835a7-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="835a7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835a7-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="835a7-150">INPUTS</span></span>

### <span data-ttu-id="835a7-151">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="835a7-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="835a7-152">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="835a7-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="835a7-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="835a7-153">OUTPUTS</span></span>

### <span data-ttu-id="835a7-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="835a7-154">System.Boolean</span></span>



## <span data-ttu-id="835a7-155">Note</span><span class="sxs-lookup"><span data-stu-id="835a7-155">NOTES</span></span>

<span data-ttu-id="835a7-156">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="835a7-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="835a7-157">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="835a7-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="835a7-158">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="835a7-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="835a7-159">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="835a7-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="835a7-160">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="835a7-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="835a7-161">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="835a7-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="835a7-162">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="835a7-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="835a7-163">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="835a7-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="835a7-164">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="835a7-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="835a7-165">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="835a7-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="835a7-166">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="835a7-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="835a7-167">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="835a7-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="835a7-168">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="835a7-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="835a7-169">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="835a7-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="835a7-170">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="835a7-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="835a7-171">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="835a7-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="835a7-172">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="835a7-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="835a7-173">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="835a7-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="835a7-174">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="835a7-175">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="835a7-176">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="835a7-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="835a7-177">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="835a7-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="835a7-178">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="835a7-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="835a7-179">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="835a7-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="835a7-180">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="835a7-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="835a7-181">NODELIST <IScaleOutScaleUnitParameters [] >: elenco dei nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="835a7-182">`[BmciPv4Address <String>]`: Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="835a7-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="835a7-183">`[ComputerName <String>]`: Nome computer della macchina fisica.</span><span class="sxs-lookup"><span data-stu-id="835a7-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="835a7-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : elenco di dati di input che consente di aggiungere un set di nodi di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="835a7-185">`[AwaitStorageConvergence <Boolean?>]`: Contrassegno indica se l'operazione deve attendere lo spazio di archiviazione per confluire prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="835a7-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="835a7-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Elenco dei nodi nell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="835a7-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="835a7-187">`[BmciPv4Address <String>]`: Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="835a7-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="835a7-188">`[ComputerName <String>]`: Nome computer della macchina fisica.</span><span class="sxs-lookup"><span data-stu-id="835a7-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="835a7-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="835a7-189">RELATED LINKS</span></span>

