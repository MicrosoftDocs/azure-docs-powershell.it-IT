---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: f318fcf3592c0b865684df57230f73a5f22ce024
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996812"
---
# <span data-ttu-id="64b98-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="64b98-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="64b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b98-102">SYNOPSIS</span></span>
<span data-ttu-id="64b98-103">Operazione per ottenere l'esportazione per l'ambito definito in base al nome dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="64b98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64b98-104">SYNTAX</span></span>

### <span data-ttu-id="64b98-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64b98-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="64b98-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="64b98-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="64b98-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64b98-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="64b98-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="64b98-108">DESCRIPTION</span></span>
<span data-ttu-id="64b98-109">Operazione per ottenere l'esportazione per l'ambito definito in base al nome dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="64b98-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64b98-110">EXAMPLES</span></span>

### <span data-ttu-id="64b98-111">Esempio 1: Ottenere tutti i tipi di AzCostManagementExports in base all'ambito</span><span class="sxs-lookup"><span data-stu-id="64b98-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="64b98-112">Ottenere tutti i tipi di AzCostManagementExports in base all'ambito</span><span class="sxs-lookup"><span data-stu-id="64b98-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="64b98-113">Esempio 2: Ottenere AzCostManagementExport per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="64b98-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="64b98-114">Ottenere AzCostManagementExport per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="64b98-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="64b98-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64b98-115">PARAMETERS</span></span>

### <span data-ttu-id="64b98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b98-116">-DefaultProfile</span></span>
<span data-ttu-id="64b98-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64b98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b98-118">-Expand</span><span class="sxs-lookup"><span data-stu-id="64b98-118">-Expand</span></span>
<span data-ttu-id="64b98-119">Può essere usato per espandere le proprietà all'interno di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="64b98-120">Attualmente è supportato solo "runHistory" e restituisce informazioni per le ultime 10 esecuzioni dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="64b98-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64b98-121">-InputObject</span></span>
<span data-ttu-id="64b98-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64b98-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-123">-Name</span><span class="sxs-lookup"><span data-stu-id="64b98-123">-Name</span></span>
<span data-ttu-id="64b98-124">Nome esportazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-124">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b98-125">-Scope</span><span class="sxs-lookup"><span data-stu-id="64b98-125">-Scope</span></span>
<span data-ttu-id="64b98-126">Questo parametro definisce l'ambito di costmanagement da prospettive diverse, "Sottoscrizione", "GruppoSociezione" e "Fornire servizio".</span><span class="sxs-lookup"><span data-stu-id="64b98-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="64b98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b98-127">CommonParameters</span></span>
<span data-ttu-id="64b98-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b98-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="64b98-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b98-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="64b98-130">INPUTS</span></span>

### <span data-ttu-id="64b98-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="64b98-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="64b98-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64b98-132">OUTPUTS</span></span>

### <span data-ttu-id="64b98-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="64b98-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="64b98-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="64b98-134">NOTES</span></span>

<span data-ttu-id="64b98-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="64b98-135">ALIASES</span></span>

<span data-ttu-id="64b98-136">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="64b98-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64b98-137">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="64b98-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64b98-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64b98-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64b98-139">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="64b98-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64b98-140">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="64b98-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="64b98-141">`[ExportName <String>]`: consente di esportare il nome.</span><span class="sxs-lookup"><span data-stu-id="64b98-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="64b98-142">`[ExternalCloudProviderId <String>]`: può essere '{externalSubscriptionId}' per l'account collegato o '{externalBillingAccountId}' per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="64b98-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="64b98-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: tipo di provider di cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="64b98-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="64b98-144">Sono incluse le 'externalSubscriptions' per gli account collegati e 'externalBillingAccounts' per gli account consolidati.</span><span class="sxs-lookup"><span data-stu-id="64b98-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="64b98-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="64b98-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64b98-146">`[Scope <String>]`: l'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="64b98-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="64b98-147">Ciò include 'subscriptions/{subscriptionId}' per l'ambito della sottoscrizione, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' per l'ambito resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' per l'ambito Account di fatturazione, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' per l'ambito Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' per ambito EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' per l'ambito BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' per l'ambito InvoiceSection, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito Account di fatturazione esterna e 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito Sottoscrizione esterna.</span><span class="sxs-lookup"><span data-stu-id="64b98-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="64b98-148">`[ViewName <String>]`: nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="64b98-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="64b98-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64b98-149">RELATED LINKS</span></span>

