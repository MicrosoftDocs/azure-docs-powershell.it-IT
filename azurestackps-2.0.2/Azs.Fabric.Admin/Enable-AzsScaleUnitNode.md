---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030325"
---
# <span data-ttu-id="8df94-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8df94-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8df94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8df94-102">SYNOPSIS</span></span>


## <span data-ttu-id="8df94-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8df94-103">SYNTAX</span></span>

### <span data-ttu-id="8df94-104">Inizio (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8df94-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8df94-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8df94-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8df94-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8df94-106">DESCRIPTION</span></span>


## <span data-ttu-id="8df94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8df94-107">EXAMPLES</span></span>

### <span data-ttu-id="8df94-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="8df94-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="8df94-109">Interrompere la modalità di manutenzione per un nodo unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8df94-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="8df94-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8df94-110">PARAMETERS</span></span>

### <span data-ttu-id="8df94-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8df94-111">-AsJob</span></span>


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

### <span data-ttu-id="8df94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df94-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="8df94-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8df94-113">-Force</span></span>


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

### <span data-ttu-id="8df94-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8df94-114">-InputObject</span></span>
<span data-ttu-id="8df94-115">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8df94-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8df94-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8df94-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8df94-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8df94-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8df94-118">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="8df94-118">-NoWait</span></span>


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

### <span data-ttu-id="8df94-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8df94-119">-PassThru</span></span>


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

### <span data-ttu-id="8df94-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df94-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8df94-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8df94-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8df94-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8df94-122">-Confirm</span></span>
<span data-ttu-id="8df94-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8df94-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df94-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df94-124">-WhatIf</span></span>
<span data-ttu-id="8df94-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df94-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df94-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df94-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df94-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df94-127">CommonParameters</span></span>
<span data-ttu-id="8df94-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df94-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df94-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8df94-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df94-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8df94-130">INPUTS</span></span>

### <span data-ttu-id="8df94-131">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8df94-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8df94-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8df94-132">OUTPUTS</span></span>

### <span data-ttu-id="8df94-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8df94-133">System.Boolean</span></span>



## <span data-ttu-id="8df94-134">Note</span><span class="sxs-lookup"><span data-stu-id="8df94-134">NOTES</span></span>

<span data-ttu-id="8df94-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8df94-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8df94-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8df94-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8df94-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="8df94-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="8df94-138">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8df94-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8df94-139">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="8df94-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8df94-140">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="8df94-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8df94-141">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="8df94-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8df94-142">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="8df94-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8df94-143">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="8df94-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8df94-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="8df94-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8df94-145">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="8df94-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8df94-146">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="8df94-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8df94-147">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8df94-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8df94-148">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="8df94-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8df94-149">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="8df94-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8df94-150">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="8df94-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8df94-151">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="8df94-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8df94-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8df94-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8df94-153">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8df94-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8df94-154">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="8df94-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8df94-155">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="8df94-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8df94-156">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8df94-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8df94-157">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8df94-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8df94-158">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8df94-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8df94-159">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8df94-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="8df94-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8df94-160">RELATED LINKS</span></span>

