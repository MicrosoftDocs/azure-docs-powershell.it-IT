---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023171"
---
# <span data-ttu-id="cccea-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="cccea-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="cccea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cccea-102">SYNOPSIS</span></span>
<span data-ttu-id="cccea-103">Ottenere una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="cccea-103">Get a quota by name.</span></span>

## <span data-ttu-id="cccea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cccea-104">SYNTAX</span></span>

### <span data-ttu-id="cccea-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cccea-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cccea-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cccea-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cccea-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cccea-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cccea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cccea-108">DESCRIPTION</span></span>
<span data-ttu-id="cccea-109">Elencare tutte le quote.</span><span class="sxs-lookup"><span data-stu-id="cccea-109">List all quotas.</span></span>
<span data-ttu-id="cccea-110">Limitare l'elenco passando un nome o un filtro.</span><span class="sxs-lookup"><span data-stu-id="cccea-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="cccea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cccea-111">EXAMPLES</span></span>

### <span data-ttu-id="cccea-112">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cccea-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="cccea-113">Elenca tutte le quote di rete.</span><span class="sxs-lookup"><span data-stu-id="cccea-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="cccea-114">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cccea-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="cccea-115">Ottiene la quota di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="cccea-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="cccea-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cccea-116">PARAMETERS</span></span>

### <span data-ttu-id="cccea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccea-117">-DefaultProfile</span></span>
<span data-ttu-id="cccea-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cccea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cccea-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="cccea-119">-Filter</span></span>
<span data-ttu-id="cccea-120">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="cccea-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="cccea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccea-121">-InputObject</span></span>
<span data-ttu-id="cccea-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cccea-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cccea-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cccea-123">-Location</span></span>
<span data-ttu-id="cccea-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cccea-124">Location of the resource.</span></span>

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

### <span data-ttu-id="cccea-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cccea-125">-Name</span></span>
<span data-ttu-id="cccea-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cccea-126">Name of the resource.</span></span>

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

### <span data-ttu-id="cccea-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cccea-127">-PassThru</span></span>
<span data-ttu-id="cccea-128">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cccea-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cccea-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cccea-129">-SubscriptionId</span></span>
<span data-ttu-id="cccea-130">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cccea-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cccea-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cccea-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cccea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccea-132">CommonParameters</span></span>
<span data-ttu-id="cccea-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccea-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cccea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccea-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cccea-135">INPUTS</span></span>

### <span data-ttu-id="cccea-136">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cccea-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="cccea-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cccea-137">OUTPUTS</span></span>

### <span data-ttu-id="cccea-138">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="cccea-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="cccea-139">Note</span><span class="sxs-lookup"><span data-stu-id="cccea-139">NOTES</span></span>

<span data-ttu-id="cccea-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cccea-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cccea-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cccea-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cccea-142">INPUTOBJECT <INetworkAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cccea-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cccea-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cccea-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cccea-144">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cccea-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cccea-145">`[ResourceName <String>]`: Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cccea-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="cccea-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cccea-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cccea-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cccea-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cccea-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cccea-148">RELATED LINKS</span></span>

