---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/get-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Get-AzCostManagementExport.md
ms.openlocfilehash: 269a58e57510f6b0945218645ec079b21b606e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336691"
---
# <span data-ttu-id="38b1c-101">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="38b1c-101">Get-AzCostManagementExport</span></span>

## <span data-ttu-id="38b1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="38b1c-103">Operazione per ottenere l'esportazione per l'ambito definito in base al nome di esportazione.</span><span class="sxs-lookup"><span data-stu-id="38b1c-103">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="38b1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38b1c-104">SYNTAX</span></span>

### <span data-ttu-id="38b1c-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38b1c-105">List (Default)</span></span>
```
Get-AzCostManagementExport -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="38b1c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="38b1c-106">Get</span></span>
```
Get-AzCostManagementExport -Name <String> -Scope <String> [-Expand <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="38b1c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="38b1c-107">GetViaIdentity</span></span>
```
Get-AzCostManagementExport -InputObject <ICostManagementIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="38b1c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38b1c-108">DESCRIPTION</span></span>
<span data-ttu-id="38b1c-109">Operazione per ottenere l'esportazione per l'ambito definito in base al nome di esportazione.</span><span class="sxs-lookup"><span data-stu-id="38b1c-109">The operation to get the export for the defined scope by export name.</span></span>

## <span data-ttu-id="38b1c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38b1c-110">EXAMPLES</span></span>

### <span data-ttu-id="38b1c-111">Esempio 1: ottenere tutti i AzCostManagementExports per ambito</span><span class="sxs-lookup"><span data-stu-id="38b1c-111">Example 1: Get all AzCostManagementExports by scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Scope 'subscriptions/**********'

ETag              Name                               Type
----              ----                               ----
"************" TestExport                         Microsoft.CostManagement/exports
"************" TestExport1                        Microsoft.CostManagement/exports
"************" TestExport2                        Microsoft.CostManagement/exports
```

<span data-ttu-id="38b1c-112">Ottenere tutti i AzCostManagementExports per ambito</span><span class="sxs-lookup"><span data-stu-id="38b1c-112">Get all AzCostManagementExports by Scope</span></span>

### <span data-ttu-id="38b1c-113">Esempio 2: ottenere AzCostManagementExport per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="38b1c-113">Example 2: Get AzCostManagementExport by Name and scope</span></span>
```powershell
PS C:\> Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'

ETag              Name       Type
----              ----       ----
"************" TestExport Microsoft.CostManagement/exports
```

<span data-ttu-id="38b1c-114">Ottenere AzCostManagementExport per nome e ambito</span><span class="sxs-lookup"><span data-stu-id="38b1c-114">Get AzCostManagementExport by Name and scope</span></span>

## <span data-ttu-id="38b1c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38b1c-115">PARAMETERS</span></span>

### <span data-ttu-id="38b1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b1c-116">-DefaultProfile</span></span>
<span data-ttu-id="38b1c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38b1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b1c-118">-Espandi</span><span class="sxs-lookup"><span data-stu-id="38b1c-118">-Expand</span></span>
<span data-ttu-id="38b1c-119">Può essere usato per espandere le proprietà all'interno di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="38b1c-119">May be used to expand the properties within an export.</span></span>
<span data-ttu-id="38b1c-120">Attualmente è supportato solo "runHistory" e restituirà informazioni per le ultime 10 esecuzioni dell'esportazione.</span><span class="sxs-lookup"><span data-stu-id="38b1c-120">Currently only 'runHistory' is supported and will return information for the last 10 executions of the export.</span></span>

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

### <span data-ttu-id="38b1c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b1c-121">-InputObject</span></span>
<span data-ttu-id="38b1c-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="38b1c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="38b1c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="38b1c-123">-Name</span></span>
<span data-ttu-id="38b1c-124">Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="38b1c-124">Export Name.</span></span>

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

### <span data-ttu-id="38b1c-125">-Ambito</span><span class="sxs-lookup"><span data-stu-id="38b1c-125">-Scope</span></span>
<span data-ttu-id="38b1c-126">Questo parametro definisce l'ambito di Costmanagement da diverse prospettive "abbonamento", "ResourceGroup" e "Fornisci servizio".</span><span class="sxs-lookup"><span data-stu-id="38b1c-126">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="38b1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b1c-127">CommonParameters</span></span>
<span data-ttu-id="38b1c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b1c-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38b1c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b1c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38b1c-130">INPUTS</span></span>

### <span data-ttu-id="38b1c-131">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="38b1c-131">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="38b1c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38b1c-132">OUTPUTS</span></span>

### <span data-ttu-id="38b1c-133">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="38b1c-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="38b1c-134">Note</span><span class="sxs-lookup"><span data-stu-id="38b1c-134">NOTES</span></span>

<span data-ttu-id="38b1c-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="38b1c-135">ALIASES</span></span>

<span data-ttu-id="38b1c-136">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38b1c-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38b1c-137">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="38b1c-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38b1c-138">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38b1c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38b1c-139">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="38b1c-139">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="38b1c-140">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="38b1c-140">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="38b1c-141">`[ExportName <String>]`: Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="38b1c-141">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="38b1c-142">`[ExternalCloudProviderId <String>]`: Può essere "{externalSubscriptionId}" per l'account collegato o "{externalBillingAccountId}" per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="38b1c-142">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="38b1c-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Il tipo di provider cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="38b1c-143">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="38b1c-144">Questo include "externalSubscriptions" per l'account collegato e "externalBillingAccounts" per l'account consolidato.</span><span class="sxs-lookup"><span data-stu-id="38b1c-144">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="38b1c-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="38b1c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="38b1c-146">`[Scope <String>]`: L'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="38b1c-146">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="38b1c-147">Questo include "abbonamenti/{subscriptionId}" per l'ambito di sottoscrizione, "abbonamenti/{subscriptionId}/resourceGroups/{resourceGroupName}" per resourceGroup ambito, "providers/Microsoft. Billing/billingAccounts/{billingAccountId}' per l'ambito dell'account di fatturazione,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/repartis/{IDReparto}' per l'ambito Department,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope,' Providers/Microsoft. Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione,' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito account di fatturazione esterno è Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito di sottoscrizione esterno.</span><span class="sxs-lookup"><span data-stu-id="38b1c-147">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="38b1c-148">`[ViewName <String>]`: Nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="38b1c-148">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="38b1c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38b1c-149">RELATED LINKS</span></span>

