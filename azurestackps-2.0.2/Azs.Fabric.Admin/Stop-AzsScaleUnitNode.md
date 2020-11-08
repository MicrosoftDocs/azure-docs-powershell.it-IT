---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030271"
---
# <span data-ttu-id="49081-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="49081-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="49081-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49081-102">SYNOPSIS</span></span>
<span data-ttu-id="49081-103">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="49081-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49081-104">SYNTAX</span></span>

### <span data-ttu-id="49081-105">PowerOff (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49081-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49081-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49081-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49081-107">Arresto</span><span class="sxs-lookup"><span data-stu-id="49081-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="49081-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49081-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49081-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49081-109">DESCRIPTION</span></span>
<span data-ttu-id="49081-110">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="49081-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49081-111">EXAMPLES</span></span>

### <span data-ttu-id="49081-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="49081-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="49081-113">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="49081-114">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="49081-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="49081-115">Spegnere un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-115">Power down a scale unit node.</span></span> <span data-ttu-id="49081-116">Come lavoro.</span><span class="sxs-lookup"><span data-stu-id="49081-116">As a job.</span></span>

## <span data-ttu-id="49081-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49081-117">PARAMETERS</span></span>

### <span data-ttu-id="49081-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49081-118">-AsJob</span></span>
<span data-ttu-id="49081-119">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="49081-119">Run the command as a job</span></span>

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

### <span data-ttu-id="49081-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49081-120">-DefaultProfile</span></span>
<span data-ttu-id="49081-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49081-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49081-122">-Force</span><span class="sxs-lookup"><span data-stu-id="49081-122">-Force</span></span>
<span data-ttu-id="49081-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="49081-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="49081-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49081-124">-InputObject</span></span>
<span data-ttu-id="49081-125">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="49081-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49081-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="49081-126">-Location</span></span>
<span data-ttu-id="49081-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="49081-127">Location of the resource.</span></span>

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

### <span data-ttu-id="49081-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="49081-128">-Name</span></span>
<span data-ttu-id="49081-129">Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="49081-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="49081-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="49081-130">-NoWait</span></span>
<span data-ttu-id="49081-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="49081-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="49081-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49081-132">-PassThru</span></span>
<span data-ttu-id="49081-133">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="49081-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="49081-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49081-134">-ResourceGroupName</span></span>
<span data-ttu-id="49081-135">Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="49081-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49081-136">-SubscriptionId</span></span>
<span data-ttu-id="49081-137">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49081-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49081-138">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="49081-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49081-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49081-139">-Confirm</span></span>
<span data-ttu-id="49081-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49081-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49081-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49081-141">-WhatIf</span></span>
<span data-ttu-id="49081-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49081-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49081-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49081-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49081-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49081-144">CommonParameters</span></span>
<span data-ttu-id="49081-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49081-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49081-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49081-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49081-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49081-147">INPUTS</span></span>

### <span data-ttu-id="49081-148">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="49081-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="49081-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49081-149">OUTPUTS</span></span>

### <span data-ttu-id="49081-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49081-150">System.Boolean</span></span>

## <span data-ttu-id="49081-151">Note</span><span class="sxs-lookup"><span data-stu-id="49081-151">NOTES</span></span>

<span data-ttu-id="49081-152">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="49081-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49081-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49081-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="49081-154">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="49081-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49081-155">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="49081-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="49081-156">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="49081-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="49081-157">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="49081-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="49081-158">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="49081-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="49081-159">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="49081-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="49081-160">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="49081-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="49081-161">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="49081-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49081-162">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="49081-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="49081-163">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="49081-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="49081-164">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="49081-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="49081-165">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="49081-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="49081-166">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="49081-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="49081-167">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="49081-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="49081-168">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="49081-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="49081-169">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49081-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="49081-170">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="49081-171">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="49081-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="49081-172">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="49081-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="49081-173">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="49081-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="49081-174">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="49081-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="49081-175">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49081-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="49081-176">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="49081-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="49081-177">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="49081-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="49081-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49081-178">RELATED LINKS</span></span>
