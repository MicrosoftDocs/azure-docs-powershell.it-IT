---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030578"
---
# <span data-ttu-id="d6715-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="d6715-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="d6715-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6715-102">SYNOPSIS</span></span>
<span data-ttu-id="d6715-103">Ottenere una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="d6715-103">Get a quota by name.</span></span>

## <span data-ttu-id="d6715-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6715-104">SYNTAX</span></span>

### <span data-ttu-id="d6715-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6715-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d6715-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d6715-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d6715-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6715-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d6715-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6715-108">DESCRIPTION</span></span>
<span data-ttu-id="d6715-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="d6715-109">List all quotas.</span></span>
<span data-ttu-id="d6715-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="d6715-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="d6715-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6715-111">EXAMPLES</span></span>

### <span data-ttu-id="d6715-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6715-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="d6715-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="d6715-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="d6715-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6715-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="d6715-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="d6715-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="d6715-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6715-116">PARAMETERS</span></span>

### <span data-ttu-id="d6715-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6715-117">-DefaultProfile</span></span>
<span data-ttu-id="d6715-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6715-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6715-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d6715-119">-Filter</span></span>
<span data-ttu-id="d6715-120">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d6715-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="d6715-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6715-121">-InputObject</span></span>
<span data-ttu-id="d6715-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d6715-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d6715-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d6715-123">-Location</span></span>
<span data-ttu-id="d6715-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6715-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6715-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6715-125">-Name</span></span>
<span data-ttu-id="d6715-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6715-126">Name of the resource.</span></span>

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

### <span data-ttu-id="d6715-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6715-127">-PassThru</span></span>
<span data-ttu-id="d6715-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="d6715-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d6715-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6715-129">-SubscriptionId</span></span>
<span data-ttu-id="d6715-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6715-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6715-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d6715-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6715-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6715-132">CommonParameters</span></span>
<span data-ttu-id="d6715-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6715-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6715-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6715-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6715-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6715-135">INPUTS</span></span>

### <span data-ttu-id="d6715-136">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d6715-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="d6715-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6715-137">OUTPUTS</span></span>

### <span data-ttu-id="d6715-138">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="d6715-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="d6715-139">Note</span><span class="sxs-lookup"><span data-stu-id="d6715-139">NOTES</span></span>

<span data-ttu-id="d6715-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d6715-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6715-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6715-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d6715-142">INPUTOBJECT <INetworkAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d6715-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6715-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d6715-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6715-144">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6715-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d6715-145">`[ResourceName <String>]`: Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d6715-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="d6715-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6715-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d6715-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d6715-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d6715-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6715-148">RELATED LINKS</span></span>

