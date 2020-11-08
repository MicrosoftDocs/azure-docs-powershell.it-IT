---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurerole
schema: 2.0.0
ms.openlocfilehash: dcd4f9da702425808e3e2565a7b668930ff7aa32
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023242"
---
# <span data-ttu-id="eecff-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="eecff-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="eecff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eecff-102">SYNOPSIS</span></span>
<span data-ttu-id="eecff-103">Restituisce la descrizione del ruolo dell'infrastruttura richiesto.</span><span class="sxs-lookup"><span data-stu-id="eecff-103">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="eecff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eecff-104">SYNTAX</span></span>

### <span data-ttu-id="eecff-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eecff-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="eecff-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="eecff-106">Get</span></span>
```
Get-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="eecff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eecff-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRole -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="eecff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eecff-108">DESCRIPTION</span></span>
<span data-ttu-id="eecff-109">Restituisce la descrizione del ruolo dell'infrastruttura richiesto.</span><span class="sxs-lookup"><span data-stu-id="eecff-109">Returns the requested infrastructure role description.</span></span>

## <span data-ttu-id="eecff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eecff-110">EXAMPLES</span></span>

### <span data-ttu-id="eecff-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="eecff-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole

A list of all infrastructure roles.
```

<span data-ttu-id="eecff-112">Ottenere un elenco di tutti i ruoli dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eecff-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="eecff-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="eecff-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRole -Name "Active Directory Federation Services"

An infrastructure role based on the name.
```

<span data-ttu-id="eecff-114">Ottenere un ruolo di infrastruttura basato sul nome.</span><span class="sxs-lookup"><span data-stu-id="eecff-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="eecff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eecff-115">PARAMETERS</span></span>

### <span data-ttu-id="eecff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eecff-116">-DefaultProfile</span></span>
<span data-ttu-id="eecff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eecff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eecff-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="eecff-118">-Filter</span></span>
<span data-ttu-id="eecff-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="eecff-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="eecff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eecff-120">-InputObject</span></span>
<span data-ttu-id="eecff-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="eecff-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eecff-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="eecff-122">-Location</span></span>
<span data-ttu-id="eecff-123">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eecff-123">Location of the resource.</span></span>

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

### <span data-ttu-id="eecff-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eecff-124">-Name</span></span>
<span data-ttu-id="eecff-125">Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eecff-125">Infrastructure role name.</span></span>

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

### <span data-ttu-id="eecff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eecff-126">-PassThru</span></span>
<span data-ttu-id="eecff-127">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="eecff-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="eecff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eecff-128">-ResourceGroupName</span></span>
<span data-ttu-id="eecff-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eecff-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="eecff-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eecff-130">-SubscriptionId</span></span>
<span data-ttu-id="eecff-131">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eecff-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eecff-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="eecff-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eecff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eecff-133">CommonParameters</span></span>
<span data-ttu-id="eecff-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eecff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eecff-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eecff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eecff-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eecff-136">INPUTS</span></span>

### <span data-ttu-id="eecff-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="eecff-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="eecff-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eecff-138">OUTPUTS</span></span>

### <span data-ttu-id="eecff-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IInfraRole</span><span class="sxs-lookup"><span data-stu-id="eecff-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRole</span></span>



## <span data-ttu-id="eecff-140">Note</span><span class="sxs-lookup"><span data-stu-id="eecff-140">NOTES</span></span>

<span data-ttu-id="eecff-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="eecff-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eecff-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eecff-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eecff-143">INPUTOBJECT <IFabricAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="eecff-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eecff-144">`[Drive <String>]`: Nome dell'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eecff-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="eecff-145">`[EdgeGateway <String>]`: Nome del gateway Edge.</span><span class="sxs-lookup"><span data-stu-id="eecff-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="eecff-146">`[EdgeGatewayPool <String>]`: Nome del pool di gateway perimetrale.</span><span class="sxs-lookup"><span data-stu-id="eecff-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="eecff-147">`[FabricLocation <String>]`: Posizione tessuto.</span><span class="sxs-lookup"><span data-stu-id="eecff-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="eecff-148">`[FileShare <String>]`: Nome condivisione file tessuto.</span><span class="sxs-lookup"><span data-stu-id="eecff-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="eecff-149">`[IPPool <String>]`: Nome pool IP.</span><span class="sxs-lookup"><span data-stu-id="eecff-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="eecff-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="eecff-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eecff-151">`[InfraRole <String>]`: Nome ruolo infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eecff-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="eecff-152">`[InfraRoleInstance <String>]`: Nome dell'istanza di un ruolo dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="eecff-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="eecff-153">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="eecff-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="eecff-154">`[LogicalNetwork <String>]`: Nome della rete logica.</span><span class="sxs-lookup"><span data-stu-id="eecff-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="eecff-155">`[LogicalSubnet <String>]`: Nome della subnet logica.</span><span class="sxs-lookup"><span data-stu-id="eecff-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="eecff-156">`[MacAddressPool <String>]`: Nome del pool di indirizzi MAC.</span><span class="sxs-lookup"><span data-stu-id="eecff-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="eecff-157">`[Operation <String>]`: Identificatore operazione.</span><span class="sxs-lookup"><span data-stu-id="eecff-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="eecff-158">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eecff-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="eecff-159">`[ScaleUnit <String>]`: Nome delle unità di scala.</span><span class="sxs-lookup"><span data-stu-id="eecff-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="eecff-160">`[ScaleUnitNode <String>]`: Nome del nodo dell'unità di scala.</span><span class="sxs-lookup"><span data-stu-id="eecff-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="eecff-161">`[SlbMuxInstance <String>]`: Nome di un'istanza di SLB MUX.</span><span class="sxs-lookup"><span data-stu-id="eecff-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="eecff-162">`[StoragePool <String>]`: Nome del pool di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eecff-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="eecff-163">`[StorageSubSystem <String>]`: Nome del sistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eecff-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="eecff-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eecff-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eecff-165">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="eecff-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="eecff-166">`[Volume <String>]`: Nome del volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="eecff-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="eecff-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eecff-167">RELATED LINKS</span></span>

