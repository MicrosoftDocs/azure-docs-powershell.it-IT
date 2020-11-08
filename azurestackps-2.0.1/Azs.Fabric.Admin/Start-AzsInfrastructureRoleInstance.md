---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/start-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 922aea432548557857b627696e156c75a8e46157
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023124"
---
# <span data-ttu-id="cdd62-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="cdd62-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="cdd62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdd62-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd62-103">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="cdd62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdd62-104">SYNTAX</span></span>

### <span data-ttu-id="cdd62-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdd62-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cdd62-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdd62-106">PowerOnViaIdentity</span></span>
```
Start-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cdd62-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdd62-107">DESCRIPTION</span></span>
<span data-ttu-id="cdd62-108">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="cdd62-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdd62-109">EXAMPLES</span></span>

### <span data-ttu-id="cdd62-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="cdd62-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="cdd62-111">Alimentazione in un'istanza del ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-111">Power on an infrastructure role instance.</span></span>


## <span data-ttu-id="cdd62-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdd62-112">PARAMETERS</span></span>

### <span data-ttu-id="cdd62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdd62-113">-AsJob</span></span>
<span data-ttu-id="cdd62-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="cdd62-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cdd62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd62-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="cdd62-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cdd62-116">-Force</span></span>
<span data-ttu-id="cdd62-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cdd62-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cdd62-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdd62-118">-InputObject</span></span>
<span data-ttu-id="cdd62-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cdd62-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cdd62-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cdd62-120">-Location</span></span>
<span data-ttu-id="cdd62-121">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cdd62-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cdd62-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdd62-122">-Name</span></span>
<span data-ttu-id="cdd62-123">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cdd62-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="cdd62-124">-NoWait</span></span>
<span data-ttu-id="cdd62-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cdd62-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cdd62-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdd62-126">-PassThru</span></span>
<span data-ttu-id="cdd62-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cdd62-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cdd62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd62-128">-ResourceGroupName</span></span>
<span data-ttu-id="cdd62-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdd62-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cdd62-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdd62-130">-SubscriptionId</span></span>
<span data-ttu-id="cdd62-131">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd62-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdd62-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cdd62-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cdd62-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdd62-133">-Confirm</span></span>
<span data-ttu-id="cdd62-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdd62-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd62-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd62-135">-WhatIf</span></span>
<span data-ttu-id="cdd62-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd62-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd62-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdd62-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd62-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd62-138">CommonParameters</span></span>
<span data-ttu-id="cdd62-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd62-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd62-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd62-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd62-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdd62-141">INPUTS</span></span>

### <span data-ttu-id="cdd62-142">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cdd62-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cdd62-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdd62-143">OUTPUTS</span></span>

### <span data-ttu-id="cdd62-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdd62-144">System.Boolean</span></span>



## <span data-ttu-id="cdd62-145">Note</span><span class="sxs-lookup"><span data-stu-id="cdd62-145">NOTES</span></span>

<span data-ttu-id="cdd62-146">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cdd62-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdd62-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cdd62-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cdd62-148">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cdd62-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdd62-149">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd62-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cdd62-150">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="cdd62-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cdd62-151">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="cdd62-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cdd62-152">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="cdd62-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cdd62-153">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="cdd62-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cdd62-154">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="cdd62-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cdd62-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cdd62-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdd62-156">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cdd62-157">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="cdd62-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cdd62-158">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cdd62-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cdd62-159">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="cdd62-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cdd62-160">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="cdd62-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cdd62-161">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="cdd62-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cdd62-162">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="cdd62-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cdd62-163">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdd62-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cdd62-164">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cdd62-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cdd62-165">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="cdd62-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cdd62-166">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="cdd62-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cdd62-167">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd62-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="cdd62-168">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd62-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cdd62-169">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdd62-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cdd62-170">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cdd62-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cdd62-171">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdd62-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cdd62-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdd62-172">RELATED LINKS</span></span>

