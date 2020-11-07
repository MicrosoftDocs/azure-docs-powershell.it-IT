---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863934"
---
# <span data-ttu-id="cb310-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="cb310-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="cb310-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb310-102">SYNOPSIS</span></span>
<span data-ttu-id="cb310-103">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cb310-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="cb310-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb310-104">SYNTAX</span></span>

### <span data-ttu-id="cb310-105">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb310-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb310-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb310-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb310-107">Arresto</span><span class="sxs-lookup"><span data-stu-id="cb310-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb310-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb310-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb310-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb310-109">DESCRIPTION</span></span>
<span data-ttu-id="cb310-110">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cb310-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="cb310-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb310-111">EXAMPLES</span></span>

### <span data-ttu-id="cb310-112">Esempio 1: {{add title here}}</span><span class="sxs-lookup"><span data-stu-id="cb310-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="cb310-113">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cb310-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="cb310-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb310-114">PARAMETERS</span></span>

### <span data-ttu-id="cb310-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb310-115">-AsJob</span></span>
<span data-ttu-id="cb310-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cb310-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cb310-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb310-117">-DefaultProfile</span></span>
<span data-ttu-id="cb310-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb310-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb310-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cb310-119">-Force</span></span>
<span data-ttu-id="cb310-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cb310-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cb310-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb310-121">-InputObject</span></span>
<span data-ttu-id="cb310-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cb310-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cb310-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cb310-123">-Location</span></span>
<span data-ttu-id="cb310-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb310-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb310-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb310-125">-Name</span></span>
<span data-ttu-id="cb310-126">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cb310-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb310-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="cb310-127">-NoWait</span></span>
<span data-ttu-id="cb310-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cb310-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb310-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb310-129">-PassThru</span></span>
<span data-ttu-id="cb310-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cb310-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb310-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb310-131">-ResourceGroupName</span></span>
<span data-ttu-id="cb310-132">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cb310-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb310-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb310-133">-SubscriptionId</span></span>
<span data-ttu-id="cb310-134">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb310-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb310-135">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cb310-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cb310-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb310-136">-Confirm</span></span>
<span data-ttu-id="cb310-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb310-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb310-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb310-138">-WhatIf</span></span>
<span data-ttu-id="cb310-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb310-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb310-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb310-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb310-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb310-141">CommonParameters</span></span>
<span data-ttu-id="cb310-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb310-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb310-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb310-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb310-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb310-144">INPUTS</span></span>

### <span data-ttu-id="cb310-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cb310-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cb310-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb310-146">OUTPUTS</span></span>

### <span data-ttu-id="cb310-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb310-147">System.Boolean</span></span>



## <span data-ttu-id="cb310-148">Note</span><span class="sxs-lookup"><span data-stu-id="cb310-148">NOTES</span></span>

<span data-ttu-id="cb310-149">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cb310-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb310-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cb310-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cb310-151">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cb310-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb310-152">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb310-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cb310-153">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="cb310-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cb310-154">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="cb310-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cb310-155">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="cb310-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cb310-156">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="cb310-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cb310-157">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="cb310-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cb310-158">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cb310-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb310-159">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cb310-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cb310-160">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cb310-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cb310-161">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb310-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cb310-162">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="cb310-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cb310-163">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="cb310-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cb310-164">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="cb310-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cb310-165">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="cb310-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cb310-166">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb310-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cb310-167">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cb310-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cb310-168">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cb310-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cb310-169">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="cb310-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cb310-170">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb310-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cb310-171">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb310-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cb310-172">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cb310-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb310-173">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cb310-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cb310-174">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cb310-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cb310-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb310-175">RELATED LINKS</span></span>

