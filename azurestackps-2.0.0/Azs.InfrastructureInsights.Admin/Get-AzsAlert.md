---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863922"
---
# <span data-ttu-id="bdbda-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="bdbda-101">Get-AzsAlert</span></span>

## <span data-ttu-id="bdbda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdbda-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbda-103">Restituisce l'avviso richiesto.</span><span class="sxs-lookup"><span data-stu-id="bdbda-103">Returns the requested alert.</span></span>

## <span data-ttu-id="bdbda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdbda-104">SYNTAX</span></span>

### <span data-ttu-id="bdbda-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdbda-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdbda-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bdbda-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdbda-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbda-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdbda-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdbda-108">DESCRIPTION</span></span>
<span data-ttu-id="bdbda-109">Restituisce l'avviso richiesto.</span><span class="sxs-lookup"><span data-stu-id="bdbda-109">Returns the requested alert.</span></span>

## <span data-ttu-id="bdbda-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdbda-110">EXAMPLES</span></span>

### <span data-ttu-id="bdbda-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="bdbda-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="bdbda-112">Ottenere un avviso per nome.</span><span class="sxs-lookup"><span data-stu-id="bdbda-112">Get an alert by Name.</span></span>

### <span data-ttu-id="bdbda-113">Esempio 2:</span><span class="sxs-lookup"><span data-stu-id="bdbda-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="bdbda-114">Ottenere tutti gli avvisi attivi e visualizzare il loro errore e il loro titolo.</span><span class="sxs-lookup"><span data-stu-id="bdbda-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="bdbda-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdbda-115">PARAMETERS</span></span>

### <span data-ttu-id="bdbda-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbda-116">-DefaultProfile</span></span>
<span data-ttu-id="bdbda-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbda-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdbda-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bdbda-118">-Filter</span></span>
<span data-ttu-id="bdbda-119">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="bdbda-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="bdbda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdbda-120">-InputObject</span></span>
<span data-ttu-id="bdbda-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="bdbda-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdbda-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bdbda-122">-Location</span></span>
<span data-ttu-id="bdbda-123">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="bdbda-123">Name of the region</span></span>

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

### <span data-ttu-id="bdbda-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdbda-124">-Name</span></span>
<span data-ttu-id="bdbda-125">Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="bdbda-125">Name of the alert.</span></span>

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

### <span data-ttu-id="bdbda-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbda-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdbda-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bdbda-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="bdbda-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdbda-128">-SubscriptionId</span></span>
<span data-ttu-id="bdbda-129">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbda-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bdbda-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bdbda-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bdbda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbda-131">CommonParameters</span></span>
<span data-ttu-id="bdbda-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdbda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbda-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdbda-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbda-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdbda-134">INPUTS</span></span>

### <span data-ttu-id="bdbda-135">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="bdbda-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="bdbda-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdbda-136">OUTPUTS</span></span>

### <span data-ttu-id="bdbda-137">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="bdbda-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="bdbda-138">Note</span><span class="sxs-lookup"><span data-stu-id="bdbda-138">NOTES</span></span>

<span data-ttu-id="bdbda-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="bdbda-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdbda-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bdbda-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="bdbda-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="bdbda-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdbda-142">`[AlertName <String>]`: Nome dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="bdbda-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="bdbda-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="bdbda-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdbda-144">`[Location <String>]`: Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="bdbda-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="bdbda-145">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bdbda-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bdbda-146">`[ResourceRegistrationId <String>]`: ID registrazione risorse.</span><span class="sxs-lookup"><span data-stu-id="bdbda-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="bdbda-147">`[ServiceHealth <String>]`: Nome integrità servizio.</span><span class="sxs-lookup"><span data-stu-id="bdbda-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="bdbda-148">`[ServiceRegistrationId <String>]`: ID registrazione servizio.</span><span class="sxs-lookup"><span data-stu-id="bdbda-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="bdbda-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbda-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bdbda-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="bdbda-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bdbda-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdbda-151">RELATED LINKS</span></span>

