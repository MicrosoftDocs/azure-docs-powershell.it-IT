---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023246"
---
# <span data-ttu-id="1eb74-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="1eb74-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="1eb74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1eb74-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb74-103">Restituisce lo stato di integrità richiesto di un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="1eb74-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="1eb74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eb74-104">SYNTAX</span></span>

### <span data-ttu-id="1eb74-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1eb74-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1eb74-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1eb74-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1eb74-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="1eb74-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1eb74-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eb74-108">DESCRIPTION</span></span>
<span data-ttu-id="1eb74-109">Restituisce lo stato di integrità richiesto di un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="1eb74-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="1eb74-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eb74-110">EXAMPLES</span></span>

### <span data-ttu-id="1eb74-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="1eb74-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="1eb74-112">Restituisce un elenco di stato di integrità dell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="1eb74-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="1eb74-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1eb74-113">PARAMETERS</span></span>

### <span data-ttu-id="1eb74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb74-114">-DefaultProfile</span></span>
<span data-ttu-id="1eb74-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eb74-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1eb74-116">-Filter</span></span>
<span data-ttu-id="1eb74-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="1eb74-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="1eb74-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eb74-118">-InputObject</span></span>
<span data-ttu-id="1eb74-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1eb74-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1eb74-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1eb74-120">-Location</span></span>
<span data-ttu-id="1eb74-121">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="1eb74-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1eb74-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb74-122">-ResourceGroupName</span></span>
<span data-ttu-id="1eb74-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1eb74-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1eb74-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1eb74-124">-SubscriptionId</span></span>
<span data-ttu-id="1eb74-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb74-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1eb74-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1eb74-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1eb74-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb74-127">CommonParameters</span></span>
<span data-ttu-id="1eb74-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb74-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb74-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eb74-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb74-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1eb74-130">INPUTS</span></span>

### <span data-ttu-id="1eb74-131">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1eb74-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="1eb74-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eb74-132">OUTPUTS</span></span>

### <span data-ttu-id="1eb74-133">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="1eb74-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="1eb74-134">Note</span><span class="sxs-lookup"><span data-stu-id="1eb74-134">NOTES</span></span>

<span data-ttu-id="1eb74-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1eb74-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1eb74-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1eb74-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1eb74-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1eb74-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1eb74-138">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="1eb74-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="1eb74-139">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1eb74-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1eb74-140">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="1eb74-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="1eb74-141">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1eb74-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1eb74-142">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="1eb74-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="1eb74-143">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="1eb74-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="1eb74-144">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="1eb74-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="1eb74-145">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb74-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1eb74-146">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1eb74-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1eb74-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eb74-147">RELATED LINKS</span></span>

