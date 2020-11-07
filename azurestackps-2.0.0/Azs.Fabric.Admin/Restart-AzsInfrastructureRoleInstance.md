---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863989"
---
# <span data-ttu-id="76c8b-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="76c8b-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="76c8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="76c8b-103">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="76c8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76c8b-104">SYNTAX</span></span>

### <span data-ttu-id="76c8b-105">Riavvio (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76c8b-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="76c8b-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76c8b-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="76c8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76c8b-107">DESCRIPTION</span></span>
<span data-ttu-id="76c8b-108">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="76c8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76c8b-109">EXAMPLES</span></span>

### <span data-ttu-id="76c8b-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="76c8b-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="76c8b-111">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="76c8b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76c8b-112">PARAMETERS</span></span>

### <span data-ttu-id="76c8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76c8b-113">-AsJob</span></span>
<span data-ttu-id="76c8b-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="76c8b-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="76c8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c8b-115">-DefaultProfile</span></span>
<span data-ttu-id="76c8b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76c8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="76c8b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="76c8b-117">-Force</span></span>
<span data-ttu-id="76c8b-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="76c8b-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76c8b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76c8b-119">-InputObject</span></span>
<span data-ttu-id="76c8b-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="76c8b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RebootViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="76c8b-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="76c8b-121">-Location</span></span>
<span data-ttu-id="76c8b-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="76c8b-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76c8b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="76c8b-123">-Name</span></span>
<span data-ttu-id="76c8b-124">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76c8b-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="76c8b-125">-NoWait</span></span>
<span data-ttu-id="76c8b-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="76c8b-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="76c8b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76c8b-127">-PassThru</span></span>
<span data-ttu-id="76c8b-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="76c8b-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="76c8b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c8b-129">-ResourceGroupName</span></span>
<span data-ttu-id="76c8b-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76c8b-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```
### <span data-ttu-id="76c8b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76c8b-131">-SubscriptionId</span></span>
<span data-ttu-id="76c8b-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76c8b-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="76c8b-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="76c8b-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="76c8b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76c8b-134">-Confirm</span></span>
<span data-ttu-id="76c8b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76c8b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c8b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c8b-136">-WhatIf</span></span>
<span data-ttu-id="76c8b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76c8b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c8b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76c8b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c8b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c8b-139">CommonParameters</span></span>
<span data-ttu-id="76c8b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c8b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c8b-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c8b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c8b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76c8b-142">INPUTS</span></span>

### <span data-ttu-id="76c8b-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="76c8b-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="76c8b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76c8b-144">OUTPUTS</span></span>

### <span data-ttu-id="76c8b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="76c8b-145">System.Boolean</span></span>



## <span data-ttu-id="76c8b-146">Note</span><span class="sxs-lookup"><span data-stu-id="76c8b-146">NOTES</span></span>

<span data-ttu-id="76c8b-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="76c8b-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76c8b-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76c8b-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="76c8b-149">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="76c8b-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="76c8b-150">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76c8b-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="76c8b-151">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="76c8b-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="76c8b-152">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="76c8b-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="76c8b-153">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="76c8b-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="76c8b-154">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="76c8b-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="76c8b-155">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="76c8b-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="76c8b-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="76c8b-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76c8b-157">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="76c8b-158">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="76c8b-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="76c8b-159">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="76c8b-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="76c8b-160">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="76c8b-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="76c8b-161">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="76c8b-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="76c8b-162">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="76c8b-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="76c8b-163">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="76c8b-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="76c8b-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76c8b-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="76c8b-165">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="76c8b-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="76c8b-166">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="76c8b-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="76c8b-167">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="76c8b-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="76c8b-168">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76c8b-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="76c8b-169">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76c8b-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="76c8b-170">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="76c8b-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="76c8b-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="76c8b-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="76c8b-172">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76c8b-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="76c8b-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76c8b-173">RELATED LINKS</span></span>

