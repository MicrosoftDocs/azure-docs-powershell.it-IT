---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 07751ba4228faa578e4181ec481eef6e5b033126
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030586"
---
# <span data-ttu-id="66731-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="66731-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="66731-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66731-102">SYNOPSIS</span></span>
<span data-ttu-id="66731-103">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="66731-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66731-104">SYNTAX</span></span>

### <span data-ttu-id="66731-105">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66731-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="66731-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="66731-106">PowerOffViaIdentity</span></span>
```
Stop-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="66731-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66731-107">DESCRIPTION</span></span>
<span data-ttu-id="66731-108">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="66731-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66731-109">EXAMPLES</span></span>

### <span data-ttu-id="66731-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="66731-110">Example 1:</span></span> 
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="66731-111">Spegnere un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="66731-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66731-112">PARAMETERS</span></span>

### <span data-ttu-id="66731-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66731-113">-AsJob</span></span>
<span data-ttu-id="66731-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="66731-114">Run the command as a job</span></span>

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

### <span data-ttu-id="66731-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66731-115">-DefaultProfile</span></span>
<span data-ttu-id="66731-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66731-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66731-117">-Force</span><span class="sxs-lookup"><span data-stu-id="66731-117">-Force</span></span>
<span data-ttu-id="66731-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="66731-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="66731-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66731-119">-InputObject</span></span>
<span data-ttu-id="66731-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="66731-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="66731-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="66731-121">-Location</span></span>
<span data-ttu-id="66731-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="66731-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66731-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="66731-123">-Name</span></span>
<span data-ttu-id="66731-124">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66731-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="66731-125">-NoWait</span></span>
<span data-ttu-id="66731-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="66731-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="66731-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66731-127">-PassThru</span></span>
<span data-ttu-id="66731-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="66731-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="66731-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66731-129">-ResourceGroupName</span></span>
<span data-ttu-id="66731-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66731-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66731-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="66731-131">-SubscriptionId</span></span>
<span data-ttu-id="66731-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66731-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="66731-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="66731-133">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="66731-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66731-134">-Confirm</span></span>
<span data-ttu-id="66731-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66731-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66731-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66731-136">-WhatIf</span></span>
<span data-ttu-id="66731-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66731-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66731-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66731-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66731-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66731-139">CommonParameters</span></span>
<span data-ttu-id="66731-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66731-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66731-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66731-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66731-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66731-142">INPUTS</span></span>

### <span data-ttu-id="66731-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="66731-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="66731-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66731-144">OUTPUTS</span></span>

### <span data-ttu-id="66731-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66731-145">System.Boolean</span></span>



## <span data-ttu-id="66731-146">Note</span><span class="sxs-lookup"><span data-stu-id="66731-146">NOTES</span></span>

<span data-ttu-id="66731-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="66731-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="66731-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="66731-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="66731-149">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="66731-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="66731-150">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="66731-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="66731-151">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="66731-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="66731-152">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="66731-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="66731-153">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="66731-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="66731-154">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="66731-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="66731-155">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="66731-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="66731-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="66731-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="66731-157">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="66731-158">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="66731-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="66731-159">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="66731-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="66731-160">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="66731-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="66731-161">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="66731-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="66731-162">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="66731-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="66731-163">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="66731-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="66731-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="66731-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="66731-165">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="66731-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="66731-166">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="66731-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="66731-167">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="66731-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="66731-168">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="66731-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="66731-169">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="66731-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="66731-170">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="66731-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="66731-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="66731-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="66731-172">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="66731-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="66731-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66731-173">RELATED LINKS</span></span>

