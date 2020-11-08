---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030160"
---
# <span data-ttu-id="54e2a-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="54e2a-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="54e2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="54e2a-103">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="54e2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54e2a-104">SYNTAX</span></span>

### <span data-ttu-id="54e2a-105">PowerOn (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54e2a-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54e2a-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="54e2a-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54e2a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54e2a-107">DESCRIPTION</span></span>
<span data-ttu-id="54e2a-108">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="54e2a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54e2a-109">EXAMPLES</span></span>

### <span data-ttu-id="54e2a-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="54e2a-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="54e2a-111">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="54e2a-112">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="54e2a-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="54e2a-113">Accendere un nodo di unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-113">Power on a scale unit node.</span></span> <span data-ttu-id="54e2a-114">Come lavoro.</span><span class="sxs-lookup"><span data-stu-id="54e2a-114">As a job.</span></span>

## <span data-ttu-id="54e2a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54e2a-115">PARAMETERS</span></span>

### <span data-ttu-id="54e2a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54e2a-116">-AsJob</span></span>
<span data-ttu-id="54e2a-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="54e2a-117">Run the command as a job</span></span>

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

### <span data-ttu-id="54e2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e2a-118">-DefaultProfile</span></span>
<span data-ttu-id="54e2a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54e2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54e2a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="54e2a-120">-Force</span></span>
<span data-ttu-id="54e2a-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="54e2a-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="54e2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54e2a-122">-InputObject</span></span>
<span data-ttu-id="54e2a-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="54e2a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54e2a-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="54e2a-124">-Location</span></span>
<span data-ttu-id="54e2a-125">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="54e2a-125">Location of the resource.</span></span>

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

### <span data-ttu-id="54e2a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="54e2a-126">-Name</span></span>
<span data-ttu-id="54e2a-127">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-127">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="54e2a-128">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="54e2a-128">-NoWait</span></span>
<span data-ttu-id="54e2a-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="54e2a-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54e2a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54e2a-130">-PassThru</span></span>
<span data-ttu-id="54e2a-131">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="54e2a-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="54e2a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e2a-132">-ResourceGroupName</span></span>
<span data-ttu-id="54e2a-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54e2a-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="54e2a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54e2a-134">-SubscriptionId</span></span>
<span data-ttu-id="54e2a-135">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="54e2a-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="54e2a-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="54e2a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="54e2a-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54e2a-137">-Confirm</span></span>
<span data-ttu-id="54e2a-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54e2a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e2a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e2a-139">-WhatIf</span></span>
<span data-ttu-id="54e2a-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54e2a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e2a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54e2a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e2a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e2a-142">CommonParameters</span></span>
<span data-ttu-id="54e2a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e2a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e2a-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54e2a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e2a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54e2a-145">INPUTS</span></span>

### <span data-ttu-id="54e2a-146">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="54e2a-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="54e2a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54e2a-147">OUTPUTS</span></span>

### <span data-ttu-id="54e2a-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54e2a-148">System.Boolean</span></span>

## <span data-ttu-id="54e2a-149">Note</span><span class="sxs-lookup"><span data-stu-id="54e2a-149">NOTES</span></span>

<span data-ttu-id="54e2a-150">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="54e2a-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54e2a-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54e2a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="54e2a-152">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="54e2a-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54e2a-153">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54e2a-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="54e2a-154">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="54e2a-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="54e2a-155">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="54e2a-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="54e2a-156">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="54e2a-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="54e2a-157">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="54e2a-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="54e2a-158">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="54e2a-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="54e2a-159">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="54e2a-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54e2a-160">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="54e2a-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="54e2a-161">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="54e2a-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="54e2a-162">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="54e2a-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="54e2a-163">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="54e2a-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="54e2a-164">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="54e2a-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="54e2a-165">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="54e2a-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="54e2a-166">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="54e2a-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="54e2a-167">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54e2a-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="54e2a-168">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="54e2a-169">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="54e2a-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="54e2a-170">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="54e2a-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="54e2a-171">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54e2a-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="54e2a-172">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54e2a-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="54e2a-173">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="54e2a-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="54e2a-174">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="54e2a-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="54e2a-175">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="54e2a-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="54e2a-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54e2a-176">RELATED LINKS</span></span>
