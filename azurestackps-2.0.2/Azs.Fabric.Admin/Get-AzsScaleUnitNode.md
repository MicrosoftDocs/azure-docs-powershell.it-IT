---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030092"
---
# <span data-ttu-id="d9128-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d9128-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d9128-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9128-102">SYNOPSIS</span></span>


## <span data-ttu-id="d9128-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9128-103">SYNTAX</span></span>

### <span data-ttu-id="d9128-104">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9128-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d9128-105">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d9128-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d9128-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d9128-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d9128-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9128-107">DESCRIPTION</span></span>


## <span data-ttu-id="d9128-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9128-108">EXAMPLES</span></span>

### <span data-ttu-id="d9128-109">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d9128-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="d9128-110">Ottenere tutti i nodi delle unità di scala in una posizione.</span><span class="sxs-lookup"><span data-stu-id="d9128-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="d9128-111">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="d9128-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="d9128-112">Ottenere un nodo specifico dell'unità di scala in una posizione assegnata un nome.</span><span class="sxs-lookup"><span data-stu-id="d9128-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="d9128-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9128-113">PARAMETERS</span></span>

### <span data-ttu-id="d9128-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9128-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="d9128-115">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d9128-115">-Filter</span></span>


```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9128-116">-InputObject</span></span>
<span data-ttu-id="d9128-117">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d9128-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d9128-118">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9128-119">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9128-120">-PassThru</span></span>


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

### <span data-ttu-id="d9128-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9128-121">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9128-122">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9128-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9128-123">CommonParameters</span></span>
<span data-ttu-id="d9128-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9128-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9128-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9128-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9128-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9128-126">INPUTS</span></span>

### <span data-ttu-id="d9128-127">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d9128-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="d9128-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9128-128">OUTPUTS</span></span>

### <span data-ttu-id="d9128-129">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d9128-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="d9128-130">Note</span><span class="sxs-lookup"><span data-stu-id="d9128-130">NOTES</span></span>

<span data-ttu-id="d9128-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d9128-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9128-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9128-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d9128-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="d9128-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="d9128-134">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d9128-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="d9128-135">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="d9128-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="d9128-136">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="d9128-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="d9128-137">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="d9128-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="d9128-138">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="d9128-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="d9128-139">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="d9128-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="d9128-140">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d9128-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9128-141">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d9128-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="d9128-142">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d9128-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="d9128-143">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d9128-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d9128-144">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="d9128-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="d9128-145">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="d9128-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="d9128-146">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="d9128-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="d9128-147">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="d9128-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="d9128-148">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9128-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d9128-149">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d9128-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="d9128-150">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="d9128-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="d9128-151">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="d9128-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="d9128-152">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d9128-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="d9128-153">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d9128-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d9128-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d9128-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d9128-155">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d9128-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="d9128-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9128-156">RELATED LINKS</span></span>

