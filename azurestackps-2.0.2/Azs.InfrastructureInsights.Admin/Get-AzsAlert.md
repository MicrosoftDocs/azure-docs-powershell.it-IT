---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030170"
---
# <span data-ttu-id="d4c15-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="d4c15-101">Get-AzsAlert</span></span>

## <span data-ttu-id="d4c15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4c15-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c15-103">Restituisce l'avviso richiesto.</span><span class="sxs-lookup"><span data-stu-id="d4c15-103">Returns the requested alert.</span></span>

## <span data-ttu-id="d4c15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4c15-104">SYNTAX</span></span>

### <span data-ttu-id="d4c15-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4c15-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4c15-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="d4c15-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4c15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4c15-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4c15-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c15-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c15-109">Restituisce l'avviso richiesto.</span><span class="sxs-lookup"><span data-stu-id="d4c15-109">Returns the requested alert.</span></span>

## <span data-ttu-id="d4c15-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4c15-110">EXAMPLES</span></span>

### <span data-ttu-id="d4c15-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d4c15-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="d4c15-112">Ottenere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="d4c15-112">Get an alert by Name.</span></span>

### <span data-ttu-id="d4c15-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="d4c15-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="d4c15-114">Ottenere tutti gli avvisi attivi e visualizzare il loro errore e il loro titolo.</span><span class="sxs-lookup"><span data-stu-id="d4c15-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="d4c15-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4c15-115">PARAMETERS</span></span>

### <span data-ttu-id="d4c15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c15-116">-DefaultProfile</span></span>
<span data-ttu-id="d4c15-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c15-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="d4c15-118">-Filter</span></span>
<span data-ttu-id="d4c15-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="d4c15-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d4c15-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4c15-120">-InputObject</span></span>
<span data-ttu-id="d4c15-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d4c15-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4c15-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d4c15-122">-Location</span></span>
<span data-ttu-id="d4c15-123">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="d4c15-123">Name of the region</span></span>

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

### <span data-ttu-id="d4c15-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4c15-124">-Name</span></span>
<span data-ttu-id="d4c15-125">Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="d4c15-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d4c15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c15-126">-ResourceGroupName</span></span>
<span data-ttu-id="d4c15-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4c15-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4c15-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4c15-128">-SubscriptionId</span></span>
<span data-ttu-id="d4c15-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c15-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d4c15-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d4c15-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d4c15-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c15-131">CommonParameters</span></span>
<span data-ttu-id="d4c15-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c15-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c15-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4c15-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c15-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4c15-134">INPUTS</span></span>

### <span data-ttu-id="d4c15-135">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d4c15-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="d4c15-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4c15-136">OUTPUTS</span></span>

### <span data-ttu-id="d4c15-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="d4c15-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="d4c15-138">Note</span><span class="sxs-lookup"><span data-stu-id="d4c15-138">NOTES</span></span>

<span data-ttu-id="d4c15-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="d4c15-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4c15-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4c15-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d4c15-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="d4c15-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4c15-142">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="d4c15-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="d4c15-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="d4c15-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4c15-144">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="d4c15-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="d4c15-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4c15-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d4c15-146">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="d4c15-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="d4c15-147">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="d4c15-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="d4c15-148">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="d4c15-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="d4c15-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c15-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d4c15-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="d4c15-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d4c15-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4c15-151">RELATED LINKS</span></span>

