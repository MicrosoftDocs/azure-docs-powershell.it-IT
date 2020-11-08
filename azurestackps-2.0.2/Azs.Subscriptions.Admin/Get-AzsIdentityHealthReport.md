---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030579"
---
# <span data-ttu-id="6de0c-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="6de0c-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="6de0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6de0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6de0c-103">Controlla l'integrità delle identità</span><span class="sxs-lookup"><span data-stu-id="6de0c-103">Checks the identity health</span></span>

## <span data-ttu-id="6de0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6de0c-104">SYNTAX</span></span>

### <span data-ttu-id="6de0c-105">Controllo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6de0c-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6de0c-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6de0c-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6de0c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6de0c-107">DESCRIPTION</span></span>
<span data-ttu-id="6de0c-108">Controlla l'integrità delle identità</span><span class="sxs-lookup"><span data-stu-id="6de0c-108">Checks the identity health</span></span>

## <span data-ttu-id="6de0c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6de0c-109">EXAMPLES</span></span>

### <span data-ttu-id="6de0c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6de0c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="6de0c-111">Ottenere lo stato dell'integrità delle identità.</span><span class="sxs-lookup"><span data-stu-id="6de0c-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="6de0c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6de0c-112">PARAMETERS</span></span>

### <span data-ttu-id="6de0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de0c-113">-DefaultProfile</span></span>
<span data-ttu-id="6de0c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6de0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de0c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6de0c-115">-InputObject</span></span>
<span data-ttu-id="6de0c-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6de0c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6de0c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6de0c-117">-SubscriptionId</span></span>
<span data-ttu-id="6de0c-118">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6de0c-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6de0c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6de0c-119">-Confirm</span></span>
<span data-ttu-id="6de0c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de0c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6de0c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de0c-121">-WhatIf</span></span>
<span data-ttu-id="6de0c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de0c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de0c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6de0c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6de0c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de0c-124">CommonParameters</span></span>
<span data-ttu-id="6de0c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de0c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de0c-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6de0c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de0c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6de0c-127">INPUTS</span></span>

### <span data-ttu-id="6de0c-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6de0c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="6de0c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6de0c-129">OUTPUTS</span></span>

### <span data-ttu-id="6de0c-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="6de0c-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="6de0c-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6de0c-131">ALIASES</span></span>

## <span data-ttu-id="6de0c-132">Note</span><span class="sxs-lookup"><span data-stu-id="6de0c-132">NOTES</span></span>

<span data-ttu-id="6de0c-133">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6de0c-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6de0c-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6de0c-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6de0c-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="6de0c-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6de0c-136">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="6de0c-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="6de0c-137">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="6de0c-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="6de0c-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="6de0c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6de0c-139">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="6de0c-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="6de0c-140">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="6de0c-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="6de0c-141">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="6de0c-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="6de0c-142">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="6de0c-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="6de0c-143">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="6de0c-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="6de0c-144">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="6de0c-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="6de0c-145">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="6de0c-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="6de0c-146">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="6de0c-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="6de0c-147">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6de0c-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="6de0c-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="6de0c-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6de0c-149">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6de0c-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="6de0c-150">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="6de0c-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="6de0c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6de0c-151">RELATED LINKS</span></span>

