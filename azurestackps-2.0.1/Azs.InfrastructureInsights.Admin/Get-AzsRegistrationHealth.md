---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023180"
---
# <span data-ttu-id="760bf-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="760bf-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="760bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="760bf-102">SYNOPSIS</span></span>
<span data-ttu-id="760bf-103">Restituisce le informazioni sull'integrità richieste per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="760bf-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="760bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="760bf-104">SYNTAX</span></span>

### <span data-ttu-id="760bf-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="760bf-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="760bf-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="760bf-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="760bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="760bf-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="760bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="760bf-108">DESCRIPTION</span></span>
<span data-ttu-id="760bf-109">Restituisce le informazioni sull'integrità richieste per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="760bf-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="760bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="760bf-110">EXAMPLES</span></span>

### <span data-ttu-id="760bf-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="760bf-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="760bf-112">Restituisce un elenco dell'integrità di ogni risorsa in un servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="760bf-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="760bf-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="760bf-114">Restituisce lo stato di integrità in un oggetto for Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="760bf-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="760bf-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="760bf-115">PARAMETERS</span></span>

### <span data-ttu-id="760bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760bf-116">-DefaultProfile</span></span>
<span data-ttu-id="760bf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="760bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760bf-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="760bf-118">-Filter</span></span>
<span data-ttu-id="760bf-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="760bf-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="760bf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="760bf-120">-InputObject</span></span>
<span data-ttu-id="760bf-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="760bf-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="760bf-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="760bf-122">-Location</span></span>
<span data-ttu-id="760bf-123">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="760bf-123">Name of the region</span></span>

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

### <span data-ttu-id="760bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="760bf-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="760bf-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="760bf-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="760bf-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="760bf-127">ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="760bf-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="760bf-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="760bf-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="760bf-129">ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-129">Service registration ID.</span></span>

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

### <span data-ttu-id="760bf-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="760bf-130">-SubscriptionId</span></span>
<span data-ttu-id="760bf-131">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="760bf-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="760bf-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="760bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760bf-133">CommonParameters</span></span>
<span data-ttu-id="760bf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="760bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760bf-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="760bf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760bf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="760bf-136">INPUTS</span></span>

### <span data-ttu-id="760bf-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="760bf-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="760bf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="760bf-138">OUTPUTS</span></span>

### <span data-ttu-id="760bf-139">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="760bf-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="760bf-140">Note</span><span class="sxs-lookup"><span data-stu-id="760bf-140">NOTES</span></span>

<span data-ttu-id="760bf-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="760bf-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="760bf-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="760bf-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="760bf-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="760bf-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="760bf-144">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="760bf-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="760bf-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="760bf-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="760bf-146">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="760bf-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="760bf-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="760bf-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="760bf-148">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="760bf-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="760bf-149">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="760bf-150">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="760bf-151">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="760bf-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="760bf-152">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="760bf-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="760bf-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="760bf-153">RELATED LINKS</span></span>

