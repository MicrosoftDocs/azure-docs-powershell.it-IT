---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030595"
---
# <span data-ttu-id="cf1ba-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="cf1ba-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="cf1ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1ba-103">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="cf1ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf1ba-104">SYNTAX</span></span>

### <span data-ttu-id="cf1ba-105">Riavvio (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf1ba-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf1ba-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf1ba-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf1ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf1ba-107">DESCRIPTION</span></span>
<span data-ttu-id="cf1ba-108">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="cf1ba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf1ba-109">EXAMPLES</span></span>

### <span data-ttu-id="cf1ba-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="cf1ba-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="cf1ba-111">Riavviare un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="cf1ba-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf1ba-112">PARAMETERS</span></span>

### <span data-ttu-id="cf1ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf1ba-113">-AsJob</span></span>
<span data-ttu-id="cf1ba-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cf1ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1ba-115">-DefaultProfile</span></span>
<span data-ttu-id="cf1ba-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cf1ba-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf1ba-117">-Force</span></span>
<span data-ttu-id="cf1ba-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cf1ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf1ba-119">-InputObject</span></span>
<span data-ttu-id="cf1ba-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf1ba-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cf1ba-121">-Location</span></span>
<span data-ttu-id="cf1ba-122">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-122">Location of the resource.</span></span>

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

### <span data-ttu-id="cf1ba-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf1ba-123">-Name</span></span>
<span data-ttu-id="cf1ba-124">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-124">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="cf1ba-125">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="cf1ba-125">-NoWait</span></span>
<span data-ttu-id="cf1ba-126">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cf1ba-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf1ba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf1ba-127">-PassThru</span></span>
<span data-ttu-id="cf1ba-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cf1ba-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cf1ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="cf1ba-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-130">Name of the resource group.</span></span>

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
### <span data-ttu-id="cf1ba-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf1ba-131">-SubscriptionId</span></span>
<span data-ttu-id="cf1ba-132">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf1ba-133">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf1ba-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf1ba-134">-Confirm</span></span>
<span data-ttu-id="cf1ba-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1ba-136">-WhatIf</span></span>
<span data-ttu-id="cf1ba-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf1ba-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf1ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1ba-139">CommonParameters</span></span>
<span data-ttu-id="cf1ba-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1ba-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf1ba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1ba-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf1ba-142">INPUTS</span></span>

### <span data-ttu-id="cf1ba-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cf1ba-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cf1ba-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf1ba-144">OUTPUTS</span></span>

### <span data-ttu-id="cf1ba-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf1ba-145">System.Boolean</span></span>



## <span data-ttu-id="cf1ba-146">Note</span><span class="sxs-lookup"><span data-stu-id="cf1ba-146">NOTES</span></span>

<span data-ttu-id="cf1ba-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf1ba-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cf1ba-149">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cf1ba-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf1ba-150">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cf1ba-151">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cf1ba-152">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cf1ba-153">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cf1ba-154">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cf1ba-155">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cf1ba-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cf1ba-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf1ba-157">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cf1ba-158">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cf1ba-159">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cf1ba-160">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cf1ba-161">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cf1ba-162">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cf1ba-163">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cf1ba-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cf1ba-165">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cf1ba-166">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cf1ba-167">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cf1ba-168">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cf1ba-169">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cf1ba-170">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf1ba-171">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cf1ba-172">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cf1ba-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cf1ba-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf1ba-173">RELATED LINKS</span></span>

