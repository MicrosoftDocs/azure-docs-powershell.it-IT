---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023263"
---
# <span data-ttu-id="0e2a9-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="0e2a9-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="0e2a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2a9-103">Restituisci il sottosistema di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="0e2a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e2a9-104">SYNTAX</span></span>

### <span data-ttu-id="0e2a9-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e2a9-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0e2a9-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="0e2a9-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0e2a9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0e2a9-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0e2a9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e2a9-108">DESCRIPTION</span></span>
<span data-ttu-id="0e2a9-109">Restituisci il sottosistema di archiviazione richiesto.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="0e2a9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e2a9-110">EXAMPLES</span></span>

### <span data-ttu-id="0e2a9-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="0e2a9-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="0e2a9-112">Ottenere tutti i sottosistemi di archiviazione da un'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="0e2a9-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="0e2a9-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="0e2a9-114">Ottenere un sottosistema di archiviazione assegnato un nome e un'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="0e2a9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e2a9-115">PARAMETERS</span></span>

### <span data-ttu-id="0e2a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2a9-116">-DefaultProfile</span></span>
<span data-ttu-id="0e2a9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e2a9-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="0e2a9-118">-Filter</span></span>
<span data-ttu-id="0e2a9-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="0e2a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e2a9-120">-InputObject</span></span>
<span data-ttu-id="0e2a9-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0e2a9-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0e2a9-122">-Location</span></span>
<span data-ttu-id="0e2a9-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-123">Location of the resource.</span></span>

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

### <span data-ttu-id="0e2a9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e2a9-124">-Name</span></span>
<span data-ttu-id="0e2a9-125">Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="0e2a9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e2a9-126">-PassThru</span></span>
<span data-ttu-id="0e2a9-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="0e2a9-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0e2a9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2a9-128">-ResourceGroupName</span></span>
<span data-ttu-id="0e2a9-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="0e2a9-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0e2a9-130">-ScaleUnit</span></span>
<span data-ttu-id="0e2a9-131">Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-131">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0e2a9-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="0e2a9-132">-Skip</span></span>
<span data-ttu-id="0e2a9-133">Parametro OData skip.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="0e2a9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e2a9-134">-SubscriptionId</span></span>
<span data-ttu-id="0e2a9-135">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0e2a9-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0e2a9-137">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="0e2a9-137">-Top</span></span>
<span data-ttu-id="0e2a9-138">Parametro OData superiore.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-138">OData top parameter.</span></span>

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

### <span data-ttu-id="0e2a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2a9-139">CommonParameters</span></span>
<span data-ttu-id="0e2a9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2a9-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e2a9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2a9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e2a9-142">INPUTS</span></span>

### <span data-ttu-id="0e2a9-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0e2a9-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="0e2a9-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e2a9-144">OUTPUTS</span></span>

### <span data-ttu-id="0e2a9-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="0e2a9-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="0e2a9-146">Note</span><span class="sxs-lookup"><span data-stu-id="0e2a9-146">NOTES</span></span>

<span data-ttu-id="0e2a9-147">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e2a9-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0e2a9-149">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0e2a9-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0e2a9-150">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="0e2a9-151">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="0e2a9-152">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="0e2a9-153">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="0e2a9-154">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="0e2a9-155">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="0e2a9-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="0e2a9-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0e2a9-157">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="0e2a9-158">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="0e2a9-159">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0e2a9-160">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="0e2a9-161">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="0e2a9-162">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="0e2a9-163">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="0e2a9-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0e2a9-165">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="0e2a9-166">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="0e2a9-167">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="0e2a9-168">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="0e2a9-169">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0e2a9-170">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0e2a9-171">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e2a9-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="0e2a9-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e2a9-172">RELATED LINKS</span></span>

