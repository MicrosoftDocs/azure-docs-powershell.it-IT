---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexportexecutionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExportExecutionHistory.md
ms.openlocfilehash: 7bb337837f9bd2be532c4eead8d8379b7cf04fe9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336679"
---
# <span data-ttu-id="ad1c2-101">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="ad1c2-101">Get-AzCostManagementExportExecutionHistory</span></span>

## <span data-ttu-id="ad1c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1c2-103">Operazione per ottenere la cronologia di esecuzione di un'esportazione per l'ambito definito e il nome di esportazione.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-103">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="ad1c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-104">SYNTAX</span></span>

### <span data-ttu-id="ad1c2-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad1c2-105">Get (Default)</span></span>
```
Get-AzCostManagementExportExecutionHistory -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad1c2-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad1c2-106">GetViaIdentity</span></span>
```
Get-AzCostManagementExportExecutionHistory -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad1c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="ad1c2-108">Operazione per ottenere la cronologia di esecuzione di un'esportazione per l'ambito definito e il nome di esportazione.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

## <span data-ttu-id="ad1c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="ad1c2-110">Esempio 1: ottenere AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="ad1c2-110">Example 1: Get AzCostManagementExportExecutionHistory</span></span>
```powershell
PS C:\> Get-AzCostManagementExportExecutionHistory -ExportName 'TestExport' -Scope 'subscriptions/**********'

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
```

<span data-ttu-id="ad1c2-111">Ottenere AzCostManagementExportExecutionHistory per exportname e scope</span><span class="sxs-lookup"><span data-stu-id="ad1c2-111">Get AzCostManagementExportExecutionHistory By ExportName and Scope</span></span>

### <span data-ttu-id="ad1c2-112">Esempio 2: ottenere AzCostManagementExportExecutionHistory da InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1c2-112">Example 2: Get AzCostManagementExportExecutionHistory by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Get-AzCostManagementExportExecutionHistory -InputObject $getExport

ExecutionType ProcessingStartTime ProcessingEndTime  Status    FileName
------------- ------------------- -----------------  ------    --------
Scheduled     2020/6/11 12:03:20  2020/6/11 12:03:43 Completed ad-hoc/TestExport/20200601-20200630/TestExport_00000000-0000-0000-0000-000000000000.csv
Scheduled     2020/6/12 12:03:37  2020/6/12 12:03:48 Completed ad-hoc/TestExport/20200601-20200630/
```

<span data-ttu-id="ad1c2-113">Ottenere AzCostManagementExportExecutionHistory da InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1c2-113">Get AzCostManagementExportExecutionHistory By InputObject</span></span>

## <span data-ttu-id="ad1c2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-114">PARAMETERS</span></span>

### <span data-ttu-id="ad1c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1c2-115">-DefaultProfile</span></span>
<span data-ttu-id="ad1c2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad1c2-117">-Exportname</span><span class="sxs-lookup"><span data-stu-id="ad1c2-117">-ExportName</span></span>
<span data-ttu-id="ad1c2-118">Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-118">Export Name.</span></span>

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

### <span data-ttu-id="ad1c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1c2-119">-InputObject</span></span>
<span data-ttu-id="ad1c2-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad1c2-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ad1c2-121">-Scope</span></span>
<span data-ttu-id="ad1c2-122">Questo parametro definisce l'ambito di Costmanagement da diverse prospettive "abbonamento", "ResourceGroup" e "Fornisci servizio".</span><span class="sxs-lookup"><span data-stu-id="ad1c2-122">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="ad1c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1c2-123">CommonParameters</span></span>
<span data-ttu-id="ad1c2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1c2-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad1c2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1c2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-126">INPUTS</span></span>

### <span data-ttu-id="ad1c2-127">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="ad1c2-127">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="ad1c2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad1c2-128">OUTPUTS</span></span>

### <span data-ttu-id="ad1c2-129">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. IExportExecution</span><span class="sxs-lookup"><span data-stu-id="ad1c2-129">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExportExecution</span></span>

## <span data-ttu-id="ad1c2-130">Note</span><span class="sxs-lookup"><span data-stu-id="ad1c2-130">NOTES</span></span>

<span data-ttu-id="ad1c2-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ad1c2-131">ALIASES</span></span>

<span data-ttu-id="ad1c2-132">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-132">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad1c2-133">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-133">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad1c2-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad1c2-135">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ad1c2-135">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad1c2-136">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="ad1c2-136">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="ad1c2-137">`[ExportName <String>]`: Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-137">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="ad1c2-138">`[ExternalCloudProviderId <String>]`: Può essere "{externalSubscriptionId}" per l'account collegato o "{externalBillingAccountId}" per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-138">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="ad1c2-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Il tipo di provider cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-139">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="ad1c2-140">Questo include "externalSubscriptions" per l'account collegato e "externalBillingAccounts" per l'account consolidato.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-140">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="ad1c2-141">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ad1c2-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad1c2-142">`[Scope <String>]`: L'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-142">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="ad1c2-143">Questo include "abbonamenti/{subscriptionId}" per l'ambito di sottoscrizione, "abbonamenti/{subscriptionId}/resourceGroups/{resourceGroupName}" per resourceGroup ambito, "providers/Microsoft. Billing/billingAccounts/{billingAccountId}' per l'ambito dell'account di fatturazione,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/repartis/{IDReparto}' per l'ambito Department,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope,' Providers/Microsoft. Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione,' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito account di fatturazione esterno è Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito di sottoscrizione esterno.</span><span class="sxs-lookup"><span data-stu-id="ad1c2-143">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="ad1c2-144">`[ViewName <String>]`: Nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="ad1c2-144">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="ad1c2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad1c2-145">RELATED LINKS</span></span>

