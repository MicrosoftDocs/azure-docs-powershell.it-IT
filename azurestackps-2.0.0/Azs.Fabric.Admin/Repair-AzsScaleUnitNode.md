---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861742"
---
# <span data-ttu-id="44ce0-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="44ce0-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="44ce0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="44ce0-103">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="44ce0-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="44ce0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44ce0-104">SYNTAX</span></span>

### <span data-ttu-id="44ce0-105">RepairExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44ce0-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44ce0-106">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="44ce0-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44ce0-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44ce0-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44ce0-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="44ce0-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44ce0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44ce0-109">DESCRIPTION</span></span>
<span data-ttu-id="44ce0-110">Ripristina un nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="44ce0-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="44ce0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44ce0-111">EXAMPLES</span></span>

### <span data-ttu-id="44ce0-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="44ce0-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="44ce0-113">Ripristinare un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="44ce0-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="44ce0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44ce0-114">PARAMETERS</span></span>

### <span data-ttu-id="44ce0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44ce0-115">-AsJob</span></span>
<span data-ttu-id="44ce0-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="44ce0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="44ce0-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="44ce0-117">-BareMetalNode</span></span>
<span data-ttu-id="44ce0-118">Descrizione di un nodo metallico bare usato per l'operazione di scalabilità su un cluster.</span><span class="sxs-lookup"><span data-stu-id="44ce0-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="44ce0-119">Per costruire, vedere la sezione Note per le proprietà di BAREMETALNODE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="44ce0-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="44ce0-120">-BiosVersion</span></span>
<span data-ttu-id="44ce0-121">Versione del BIOS del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="44ce0-122">-BmciPv4Address</span></span>
<span data-ttu-id="44ce0-123">Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-124">-Clustername</span><span class="sxs-lookup"><span data-stu-id="44ce0-124">-ClusterName</span></span>
<span data-ttu-id="44ce0-125">Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="44ce0-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-126">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="44ce0-126">-ComputerName</span></span>
<span data-ttu-id="44ce0-127">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="44ce0-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ce0-128">-DefaultProfile</span></span>
<span data-ttu-id="44ce0-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44ce0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ce0-130">-Force</span><span class="sxs-lookup"><span data-stu-id="44ce0-130">-Force</span></span>
<span data-ttu-id="44ce0-131">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="44ce0-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="44ce0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ce0-132">-InputObject</span></span>
<span data-ttu-id="44ce0-133">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="44ce0-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="44ce0-134">-Location</span></span>
<span data-ttu-id="44ce0-135">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="44ce0-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-136">-MacAddress</span><span class="sxs-lookup"><span data-stu-id="44ce0-136">-MacAddress</span></span>
<span data-ttu-id="44ce0-137">Nome dell'indirizzo MAC del nodo bare metal.</span><span class="sxs-lookup"><span data-stu-id="44ce0-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-138">-Modello</span><span class="sxs-lookup"><span data-stu-id="44ce0-138">-Model</span></span>
<span data-ttu-id="44ce0-139">Modello del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="44ce0-140">-Name</span></span>
<span data-ttu-id="44ce0-141">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="44ce0-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-142">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="44ce0-142">-NoWait</span></span>
<span data-ttu-id="44ce0-143">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="44ce0-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44ce0-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44ce0-144">-PassThru</span></span>
<span data-ttu-id="44ce0-145">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="44ce0-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44ce0-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ce0-146">-ResourceGroupName</span></span>
<span data-ttu-id="44ce0-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44ce0-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-148">-NumeroSerie</span><span class="sxs-lookup"><span data-stu-id="44ce0-148">-SerialNumber</span></span>
<span data-ttu-id="44ce0-149">Numero seriale del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44ce0-150">-SubscriptionId</span></span>
<span data-ttu-id="44ce0-151">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44ce0-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="44ce0-152">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="44ce0-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="44ce0-153">-Vendor</span></span>
<span data-ttu-id="44ce0-154">Fornitore del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44ce0-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44ce0-155">-Confirm</span></span>
<span data-ttu-id="44ce0-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ce0-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ce0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ce0-157">-WhatIf</span></span>
<span data-ttu-id="44ce0-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ce0-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ce0-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ce0-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ce0-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ce0-160">CommonParameters</span></span>
<span data-ttu-id="44ce0-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ce0-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ce0-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44ce0-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ce0-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44ce0-163">INPUTS</span></span>

### <span data-ttu-id="44ce0-164">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="44ce0-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="44ce0-165">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="44ce0-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="44ce0-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44ce0-166">OUTPUTS</span></span>

### <span data-ttu-id="44ce0-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44ce0-167">System.Boolean</span></span>



## <span data-ttu-id="44ce0-168">Note</span><span class="sxs-lookup"><span data-stu-id="44ce0-168">NOTES</span></span>

<span data-ttu-id="44ce0-169">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="44ce0-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44ce0-170">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44ce0-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="44ce0-171">BAREMETALNODE <IBareMetalNodeDescription> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="44ce0-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="44ce0-172">`[BiosVersion <String>]`: Versione BIOS del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="44ce0-173">`[BmciPv4Address <String>]`: Indirizzo BMC del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="44ce0-174">`[ClusterName <String>]`: Nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="44ce0-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="44ce0-175">`[ComputerName <String>]`: Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="44ce0-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="44ce0-176">`[MacAddress <String>]`: Nome dell'indirizzo MAC del nodo bare metal.</span><span class="sxs-lookup"><span data-stu-id="44ce0-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="44ce0-177">`[Model <String>]`: Modello del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="44ce0-178">`[SerialNumber <String>]`: Numero seriale del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="44ce0-179">`[Vendor <String>]`: Vendor del computer fisico.</span><span class="sxs-lookup"><span data-stu-id="44ce0-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="44ce0-180">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="44ce0-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44ce0-181">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44ce0-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="44ce0-182">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="44ce0-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="44ce0-183">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="44ce0-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="44ce0-184">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="44ce0-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="44ce0-185">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="44ce0-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="44ce0-186">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="44ce0-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="44ce0-187">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="44ce0-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44ce0-188">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="44ce0-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="44ce0-189">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="44ce0-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="44ce0-190">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="44ce0-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="44ce0-191">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="44ce0-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="44ce0-192">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="44ce0-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="44ce0-193">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="44ce0-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="44ce0-194">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="44ce0-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="44ce0-195">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44ce0-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="44ce0-196">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="44ce0-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="44ce0-197">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="44ce0-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="44ce0-198">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="44ce0-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="44ce0-199">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44ce0-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="44ce0-200">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44ce0-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="44ce0-201">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44ce0-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="44ce0-202">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="44ce0-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="44ce0-203">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="44ce0-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="44ce0-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44ce0-204">RELATED LINKS</span></span>

