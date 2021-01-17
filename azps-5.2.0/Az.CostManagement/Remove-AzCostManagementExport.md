---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/remove-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Remove-AzCostManagementExport.md
ms.openlocfilehash: 75c1f01730d4dfe3e9769a430f874887fd2d2090
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336607"
---
# <span data-ttu-id="fc11c-101">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="fc11c-101">Remove-AzCostManagementExport</span></span>

## <span data-ttu-id="fc11c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc11c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc11c-103">Operazione per eliminare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="fc11c-103">The operation to delete a export.</span></span>

## <span data-ttu-id="fc11c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc11c-104">SYNTAX</span></span>

### <span data-ttu-id="fc11c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fc11c-105">Delete (Default)</span></span>
```
Remove-AzCostManagementExport -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fc11c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc11c-106">DeleteViaIdentity</span></span>
```
Remove-AzCostManagementExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fc11c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc11c-107">DESCRIPTION</span></span>
<span data-ttu-id="fc11c-108">Operazione per eliminare un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="fc11c-108">The operation to delete a export.</span></span>

## <span data-ttu-id="fc11c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc11c-109">EXAMPLES</span></span>

### <span data-ttu-id="fc11c-110">Esempio 1: eliminare il AzCostManagementExport per ambito e nome</span><span class="sxs-lookup"><span data-stu-id="fc11c-110">Example 1: Delete the AzCostManagementExport by Scope and Name</span></span>
```powershell
PS C:\> Remove-AzCostManagementExport -Scope 'subscriptions/********' -name 'TestExportDatasetAggregationInfoYouri'


```

<span data-ttu-id="fc11c-111">Eliminare l'AzCostManagementExport per ambito e exportname</span><span class="sxs-lookup"><span data-stu-id="fc11c-111">Delete the AzCostManagementExport By Scope and ExportName</span></span>

### <span data-ttu-id="fc11c-112">Esempio 2: eliminare il AzCostManagementExport per esportare un oggetto</span><span class="sxs-lookup"><span data-stu-id="fc11c-112">Example 2: Delete the AzCostManagementExport by Export Object</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Scope 'subscriptions/*********' -name 'TestExportDatasetAggregationYouori'
Remove-AzCostManagementExport -InputObject $getExport


```

<span data-ttu-id="fc11c-113">Eliminare il AzCostManagementExport da InputObject</span><span class="sxs-lookup"><span data-stu-id="fc11c-113">Delete the AzCostManagementExport By InputObject</span></span>

## <span data-ttu-id="fc11c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc11c-114">PARAMETERS</span></span>

### <span data-ttu-id="fc11c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc11c-115">-DefaultProfile</span></span>
<span data-ttu-id="fc11c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc11c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc11c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc11c-117">-InputObject</span></span>
<span data-ttu-id="fc11c-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="fc11c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc11c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc11c-119">-Name</span></span>
<span data-ttu-id="fc11c-120">Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="fc11c-120">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc11c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc11c-121">-PassThru</span></span>
<span data-ttu-id="fc11c-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="fc11c-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc11c-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="fc11c-123">-Scope</span></span>
<span data-ttu-id="fc11c-124">Questo parametro definisce l'ambito di Costmanagement da diverse prospettive "abbonamento", "ResourceGroup" e "Fornisci servizio".</span><span class="sxs-lookup"><span data-stu-id="fc11c-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc11c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fc11c-125">-Confirm</span></span>
<span data-ttu-id="fc11c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc11c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc11c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc11c-127">-WhatIf</span></span>
<span data-ttu-id="fc11c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc11c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc11c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fc11c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc11c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc11c-130">CommonParameters</span></span>
<span data-ttu-id="fc11c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc11c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc11c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc11c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc11c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc11c-133">INPUTS</span></span>

### <span data-ttu-id="fc11c-134">Microsoft. Azure. PowerShell. Cmdlets. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="fc11c-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="fc11c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc11c-135">OUTPUTS</span></span>

### <span data-ttu-id="fc11c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc11c-136">System.Boolean</span></span>

## <span data-ttu-id="fc11c-137">Note</span><span class="sxs-lookup"><span data-stu-id="fc11c-137">NOTES</span></span>

<span data-ttu-id="fc11c-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fc11c-138">ALIASES</span></span>

<span data-ttu-id="fc11c-139">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc11c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fc11c-140">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="fc11c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc11c-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc11c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fc11c-142">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="fc11c-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fc11c-143">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="fc11c-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="fc11c-144">`[ExportName <String>]`: Esporta nome.</span><span class="sxs-lookup"><span data-stu-id="fc11c-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="fc11c-145">`[ExternalCloudProviderId <String>]`: Può essere "{externalSubscriptionId}" per l'account collegato o "{externalBillingAccountId}" per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="fc11c-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="fc11c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Il tipo di provider cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="fc11c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="fc11c-147">Questo include "externalSubscriptions" per l'account collegato e "externalBillingAccounts" per l'account consolidato.</span><span class="sxs-lookup"><span data-stu-id="fc11c-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="fc11c-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="fc11c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc11c-149">`[Scope <String>]`: L'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fc11c-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="fc11c-150">Questo include "abbonamenti/{subscriptionId}" per l'ambito di sottoscrizione, "abbonamenti/{subscriptionId}/resourceGroups/{resourceGroupName}" per resourceGroup ambito, "providers/Microsoft. Billing/billingAccounts/{billingAccountId}' per l'ambito dell'account di fatturazione,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/repartis/{IDReparto}' per l'ambito Department,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope,' Providers/Microsoft. Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope,' Providers/Microsoft. Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione,' Providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito account di fatturazione esterno è Providers/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito di sottoscrizione esterno.</span><span class="sxs-lookup"><span data-stu-id="fc11c-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="fc11c-151">`[ViewName <String>]`: Nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="fc11c-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="fc11c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc11c-152">RELATED LINKS</span></span>

