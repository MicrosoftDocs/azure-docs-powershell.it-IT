---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030289"
---
# <span data-ttu-id="11e07-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="11e07-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="11e07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11e07-102">SYNOPSIS</span></span>
<span data-ttu-id="11e07-103">Restituisce l'oggetto integrità del servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="11e07-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="11e07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11e07-104">SYNTAX</span></span>

### <span data-ttu-id="11e07-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="11e07-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11e07-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="11e07-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11e07-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11e07-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="11e07-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11e07-108">DESCRIPTION</span></span>
<span data-ttu-id="11e07-109">Restituisce l'oggetto integrità del servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="11e07-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="11e07-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11e07-110">EXAMPLES</span></span>

### <span data-ttu-id="11e07-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="11e07-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="11e07-112">Restituisce un elenco dell'integrità di ogni servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="11e07-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="11e07-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="11e07-114">Restituisce l'integrità di un servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-114">Returns a service's health.</span></span>

## <span data-ttu-id="11e07-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11e07-115">PARAMETERS</span></span>

### <span data-ttu-id="11e07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e07-116">-DefaultProfile</span></span>
<span data-ttu-id="11e07-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11e07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e07-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="11e07-118">-Filter</span></span>
<span data-ttu-id="11e07-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="11e07-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="11e07-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e07-120">-InputObject</span></span>
<span data-ttu-id="11e07-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="11e07-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="11e07-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="11e07-122">-Location</span></span>
<span data-ttu-id="11e07-123">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="11e07-123">Name of the region</span></span>

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

### <span data-ttu-id="11e07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e07-124">-ResourceGroupName</span></span>
<span data-ttu-id="11e07-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11e07-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="11e07-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="11e07-126">-ServiceHealth</span></span>
<span data-ttu-id="11e07-127">Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-127">Service Health name.</span></span>

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

### <span data-ttu-id="11e07-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11e07-128">-SubscriptionId</span></span>
<span data-ttu-id="11e07-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11e07-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="11e07-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="11e07-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e07-131">CommonParameters</span></span>
<span data-ttu-id="11e07-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11e07-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e07-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11e07-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e07-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11e07-134">INPUTS</span></span>

### <span data-ttu-id="11e07-135">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="11e07-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="11e07-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11e07-136">OUTPUTS</span></span>

### <span data-ttu-id="11e07-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="11e07-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="11e07-138">Note</span><span class="sxs-lookup"><span data-stu-id="11e07-138">NOTES</span></span>

<span data-ttu-id="11e07-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="11e07-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11e07-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11e07-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="11e07-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="11e07-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11e07-142">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="11e07-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="11e07-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="11e07-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11e07-144">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="11e07-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="11e07-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="11e07-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="11e07-146">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="11e07-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="11e07-147">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="11e07-148">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="11e07-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="11e07-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="11e07-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="11e07-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="11e07-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11e07-151">RELATED LINKS</span></span>

