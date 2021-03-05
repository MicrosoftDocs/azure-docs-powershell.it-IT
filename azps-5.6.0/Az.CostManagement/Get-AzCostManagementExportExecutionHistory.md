---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 602797e32e5d29e3dd4ff2b6ade75ff8055efd0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009677"
---
# <span data-ttu-id="5c288-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="5c288-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="5c288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c288-102">SYNOPSIS</span></span>
<span data-ttu-id="5c288-103">Operazione per ottenere la cronologia di esecuzione di un'esportazione per l'ambito definito e il nome dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="5c288-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="5c288-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c288-104">SYNTAX</span></span>

### <span data-ttu-id="5c288-105">Ottieni (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c288-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c288-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c288-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c288-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c288-107">DESCRIPTION</span></span>
<span data-ttu-id="5c288-108">Operazione per ottenere la cronologia di esecuzione di un'esportazione per l'ambito definito e il nome dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="5c288-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="5c288-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c288-109">EXAMPLES</span></span>

### <span data-ttu-id="5c288-110">Esempio 1: Ottenere AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="5c288-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="5c288-111">Ottenere AzCostManagementExportExecutionHistory per ExportName e Scope</span><span class="sxs-lookup"><span data-stu-id="5c288-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="5c288-112">Esempio 2: Ottenere AzCostManagementExportExecutionHistory da InputObject</span><span class="sxs-lookup"><span data-stu-id="5c288-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="5c288-113">Ottenere AzCostManagementExportExecutionHistory per InputObject</span><span class="sxs-lookup"><span data-stu-id="5c288-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="5c288-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c288-114">PARAMETERS</span></span>

### <span data-ttu-id="5c288-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c288-115">-DefaultProfile</span></span>
<span data-ttu-id="5c288-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c288-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c288-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="5c288-117">-ExportName</span></span>
<span data-ttu-id="5c288-118">Nome esportazione.</span><span class="sxs-lookup"><span data-stu-id="5c288-118">Export Name.</span></span>

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

### <span data-ttu-id="5c288-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c288-119">-InputObject</span></span>
<span data-ttu-id="5c288-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5c288-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5c288-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="5c288-121">-Scope</span></span>
<span data-ttu-id="5c288-122">Questo parametro definisce l'ambito di costmanagement da prospettive diverse, "Sottoscrizione", "GruppoSociezione" e "Fornire servizio".</span><span class="sxs-lookup"><span data-stu-id="5c288-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="5c288-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c288-123">CommonParameters</span></span>
<span data-ttu-id="5c288-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c288-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c288-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c288-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c288-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c288-126">INPUTS</span></span>

### <span data-ttu-id="5c288-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="5c288-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="5c288-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c288-128">OUTPUTS</span></span>

### <span data-ttu-id="5c288-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span><span class="sxs-lookup"><span data-stu-id="5c288-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="5c288-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c288-130">NOTES</span></span>

<span data-ttu-id="5c288-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5c288-131">ALIASES</span></span>

<span data-ttu-id="5c288-132">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="5c288-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c288-133">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5c288-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c288-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c288-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c288-135">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="5c288-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c288-136">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="5c288-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="5c288-137">`[ExportName <String>]`: consente di esportare il nome.</span><span class="sxs-lookup"><span data-stu-id="5c288-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="5c288-138">`[ExternalCloudProviderId <String>]`: può essere '{externalSubscriptionId}' per l'account collegato o '{externalBillingAccountId}' per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="5c288-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="5c288-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: tipo di provider di cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="5c288-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="5c288-140">Sono incluse le 'externalSubscriptions' per gli account collegati e 'externalBillingAccounts' per gli account consolidati.</span><span class="sxs-lookup"><span data-stu-id="5c288-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="5c288-141">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="5c288-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c288-142">`[Scope <String>]`: l'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="5c288-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="5c288-143">Ciò include 'subscriptions/{subscriptionId}' per l'ambito della sottoscrizione, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' per l'ambito resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' per l'ambito Account di fatturazione, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' per l'ambito Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' per ambito EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' per l'ambito BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' per l'ambito InvoiceSection, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito Account di fatturazione esterna e 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito Sottoscrizione esterna.</span><span class="sxs-lookup"><span data-stu-id="5c288-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="5c288-144">`[ViewName <String>]`: nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="5c288-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="5c288-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c288-145">RELATED LINKS</span></span>

