---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/powershell/module/az.costmanagement/invoke-azcostmanagementexecuteexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementExecuteExport.md
ms.openlocfilehash: ef26f52068794349b785c8c067ead33b1ee3284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983598"
---
# <span data-ttu-id="f0b4c-101">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="f0b4c-101">Invoke-AzCostManagementExecuteExport</span></span>

## <span data-ttu-id="f0b4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b4c-103">Operazione per l'esecuzione di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-103">The operation to execute an export.</span></span>

## <span data-ttu-id="f0b4c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0b4c-104">SYNTAX</span></span>

### <span data-ttu-id="f0b4c-105">Esegui (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0b4c-105">Execute (Default)</span></span>
```
Invoke-AzCostManagementExecuteExport -ExportName <String> -Scope <String> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f0b4c-106">ExecuteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f0b4c-106">ExecuteViaIdentity</span></span>
```
Invoke-AzCostManagementExecuteExport -InputObject <ICostManagementIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f0b4c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b4c-108">Operazione per l'esecuzione di un'esportazione.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-108">The operation to execute an export.</span></span>

## <span data-ttu-id="f0b4c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b4c-110">Esempio 1: Richiamare l'esportazione tramite ExportName e Scope</span><span class="sxs-lookup"><span data-stu-id="f0b4c-110">Example 1: Invoke Export by ExportName and Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementExecuteExport -ExportName 'TestExport' -Scope 'subscriptions/**********'

```

<span data-ttu-id="f0b4c-111">Invoke Export by ExportName and Scope</span><span class="sxs-lookup"><span data-stu-id="f0b4c-111">Invoke Export by ExportName and Scope</span></span>

### <span data-ttu-id="f0b4c-112">Esempio 2: Richiamare l'esportazione tramite InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b4c-112">Example 2: Invoke Export by InputObject</span></span>
```powershell
PS C:\> $getExport = Get-AzCostManagementExport -Name 'TestExport' -Scope 'subscriptions/**********'
Invoke-AzCostManagementExecuteExport -InputObject $getExport

```

<span data-ttu-id="f0b4c-113">Richiamare l'esportazione tramite InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b4c-113">Invoke Export by InputObject</span></span>

## <span data-ttu-id="f0b4c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0b4c-114">PARAMETERS</span></span>

### <span data-ttu-id="f0b4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b4c-115">-DefaultProfile</span></span>
<span data-ttu-id="f0b4c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0b4c-117">-ExportName</span><span class="sxs-lookup"><span data-stu-id="f0b4c-117">-ExportName</span></span>
<span data-ttu-id="f0b4c-118">Nome esportazione.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-118">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b4c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0b4c-119">-InputObject</span></span>
<span data-ttu-id="f0b4c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: ExecuteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0b4c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0b4c-121">-PassThru</span></span>
<span data-ttu-id="f0b4c-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="f0b4c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f0b4c-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="f0b4c-123">-Scope</span></span>
<span data-ttu-id="f0b4c-124">Questo parametro definisce l'ambito di costmanagement da prospettive diverse, "Sottoscrizione", "GruppoSociezione" e "Fornire servizio".</span><span class="sxs-lookup"><span data-stu-id="f0b4c-124">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: Execute
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b4c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0b4c-125">-Confirm</span></span>
<span data-ttu-id="f0b4c-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b4c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b4c-127">-WhatIf</span></span>
<span data-ttu-id="f0b4c-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b4c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b4c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b4c-130">CommonParameters</span></span>
<span data-ttu-id="f0b4c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b4c-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b4c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0b4c-133">INPUTS</span></span>

### <span data-ttu-id="f0b4c-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="f0b4c-134">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="f0b4c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0b4c-135">OUTPUTS</span></span>

### <span data-ttu-id="f0b4c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0b4c-136">System.Boolean</span></span>

## <span data-ttu-id="f0b4c-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0b4c-137">NOTES</span></span>

<span data-ttu-id="f0b4c-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f0b4c-138">ALIASES</span></span>

<span data-ttu-id="f0b4c-139">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f0b4c-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f0b4c-140">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f0b4c-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f0b4c-142">INPUTOBJECT <ICostManagementIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f0b4c-142">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f0b4c-143">`[AlertId <String>]`: ID avviso</span><span class="sxs-lookup"><span data-stu-id="f0b4c-143">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="f0b4c-144">`[ExportName <String>]`: consente di esportare il nome.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-144">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="f0b4c-145">`[ExternalCloudProviderId <String>]`: può essere '{externalSubscriptionId}' per l'account collegato o '{externalBillingAccountId}' per l'account consolidato usato con le operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-145">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="f0b4c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: tipo di provider di cloud esterno associato alle operazioni di dimensione/query.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-146">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="f0b4c-147">Sono incluse le 'externalSubscriptions' per gli account collegati e 'externalBillingAccounts' per gli account consolidati.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-147">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="f0b4c-148">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f0b4c-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f0b4c-149">`[Scope <String>]`: l'ambito associato alle operazioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-149">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="f0b4c-150">Ciò include 'subscriptions/{subscriptionId}' per l'ambito della sottoscrizione, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' per l'ambito resourceGroup, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' per l'ambito Account di fatturazione, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' per l'ambito Department, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' per ambito EnrollmentAccount, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' per l'ambito BillingProfile, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' per l'ambito InvoiceSection, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' per l'ambito del gruppo di gestione, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' per l'ambito Account di fatturazione esterna e 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' per l'ambito Sottoscrizione esterna.</span><span class="sxs-lookup"><span data-stu-id="f0b4c-150">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="f0b4c-151">`[ViewName <String>]`: nome visualizzazione</span><span class="sxs-lookup"><span data-stu-id="f0b4c-151">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="f0b4c-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0b4c-152">RELATED LINKS</span></span>

