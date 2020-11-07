---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 7c33c351b7daea7b39fd614a8d842a4ed8be7f2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678744"
---
# <span data-ttu-id="6ad97-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6ad97-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="6ad97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ad97-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad97-103">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ad97-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="6ad97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ad97-104">SYNTAX</span></span>

### <span data-ttu-id="6ad97-105">OldSetDiagnosticSetting (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ad97-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad97-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6ad97-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad97-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ad97-107">DESCRIPTION</span></span>
<span data-ttu-id="6ad97-108">Il cmdlet **set-AzDiagnosticSetting** Abilita o disabilita ogni categoria di granulosità e log per la particolare risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ad97-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="6ad97-109">I registri e le metriche sono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6ad97-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="6ad97-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ad97-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6ad97-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ad97-111">EXAMPLES</span></span>

### <span data-ttu-id="6ad97-112">Esempio 1: abilitare tutte le metriche e i registri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="6ad97-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="6ad97-113">Questo comando consente di abilitare tutte le metriche e i registri disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="6ad97-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="6ad97-114">Esempio 2: disabilitare tutte le metriche e i registri</span><span class="sxs-lookup"><span data-stu-id="6ad97-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="6ad97-115">Questo comando Disabilita tutte le metriche e i registri disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="6ad97-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="6ad97-116">Esempio 3: abilitare/disabilitare più categorie di metriche</span><span class="sxs-lookup"><span data-stu-id="6ad97-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="6ad97-117">Questo comando Disabilita le metriche cateories chiamate Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="6ad97-117">This command disables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="6ad97-118">Tutte le altre categorie restano invariate.</span><span class="sxs-lookup"><span data-stu-id="6ad97-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="6ad97-119">Esempio 4: abilitare/disabilitare più categorie di log</span><span class="sxs-lookup"><span data-stu-id="6ad97-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="6ad97-120">Questo comando consente di abilitare Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="6ad97-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="6ad97-121">Tutte le altre categorie di metriche e registri restano le stesse.</span><span class="sxs-lookup"><span data-stu-id="6ad97-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="6ad97-122">Esempio 4: abilitare una granulosità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="6ad97-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="6ad97-123">Questo comando consente di abilitare solo Categoria1, Categoria2 e Time Grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="6ad97-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="6ad97-124">Tutti gli altri grani e categorie di tempo sono invariati.</span><span class="sxs-lookup"><span data-stu-id="6ad97-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="6ad97-125">Esempio 5: uso della pipeline</span><span class="sxs-lookup"><span data-stu-id="6ad97-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="6ad97-126">Questo comando usa la pipeline di PowerShell per impostare (non apportare modifiche) un'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="6ad97-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="6ad97-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ad97-127">PARAMETERS</span></span>

### <span data-ttu-id="6ad97-128">-Categoria</span><span class="sxs-lookup"><span data-stu-id="6ad97-128">-Category</span></span>
<span data-ttu-id="6ad97-129">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="6ad97-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="6ad97-130">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="6ad97-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad97-131">-DefaultProfile</span></span>
<span data-ttu-id="6ad97-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ad97-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="6ad97-133">-Enabled</span></span>
<span data-ttu-id="6ad97-134">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="6ad97-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="6ad97-135">Specificare $True per abilitare la diagnostica o $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="6ad97-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="6ad97-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="6ad97-137">ID regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="6ad97-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="6ad97-138">-EventHubName</span></span>
<span data-ttu-id="6ad97-139">Nome Hub dell'evento</span><span class="sxs-lookup"><span data-stu-id="6ad97-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ad97-140">-InputObject</span></span>
<span data-ttu-id="6ad97-141">L'oggetto di input (possibile dalla pipeline) Il nome e resourceId verranno estratti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6ad97-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="6ad97-142">-MetricCategory</span></span>
<span data-ttu-id="6ad97-143">Elenco di categorie metriche.</span><span class="sxs-lookup"><span data-stu-id="6ad97-143">The list of metric categories.</span></span> <span data-ttu-id="6ad97-144">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="6ad97-144">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ad97-145">-Name</span></span>
<span data-ttu-id="6ad97-146">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="6ad97-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="6ad97-147">Il valore predefinito è **Service**.</span><span class="sxs-lookup"><span data-stu-id="6ad97-147">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad97-148">-ResourceId</span></span>
<span data-ttu-id="6ad97-149">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ad97-149">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="6ad97-150">-RetentionEnabled</span></span>
<span data-ttu-id="6ad97-151">Indica se la conservazione delle informazioni di diagnostica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="6ad97-151">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6ad97-152">-RetentionInDays</span></span>
<span data-ttu-id="6ad97-153">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="6ad97-153">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="6ad97-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="6ad97-155">ID regola del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="6ad97-155">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6ad97-156">-StorageAccountId</span></span>
<span data-ttu-id="6ad97-157">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="6ad97-157">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="6ad97-158">-Timegrain</span></span>
<span data-ttu-id="6ad97-159">Specifica i grani temporali da abilitare o disabilitare per le metriche, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="6ad97-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="6ad97-160">Se non specifichi una granulosità temporale, questo comando funziona in tutti i grani temporali disponibili.</span><span class="sxs-lookup"><span data-stu-id="6ad97-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="6ad97-161">-WorkspaceId</span></span>
<span data-ttu-id="6ad97-162">ID dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6ad97-162">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad97-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ad97-163">-Confirm</span></span>
<span data-ttu-id="6ad97-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ad97-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad97-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad97-165">-WhatIf</span></span>
<span data-ttu-id="6ad97-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ad97-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ad97-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ad97-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad97-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad97-168">CommonParameters</span></span>
<span data-ttu-id="6ad97-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ad97-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad97-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad97-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad97-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ad97-171">INPUTS</span></span>

### <span data-ttu-id="6ad97-172">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6ad97-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="6ad97-173">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad97-173">System.String</span></span>

### <span data-ttu-id="6ad97-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ad97-174">System.Boolean</span></span>

### <span data-ttu-id="6ad97-175">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ad97-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ad97-176">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ad97-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6ad97-177">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6ad97-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6ad97-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ad97-178">OUTPUTS</span></span>

### <span data-ttu-id="6ad97-179">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6ad97-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="6ad97-180">Note</span><span class="sxs-lookup"><span data-stu-id="6ad97-180">NOTES</span></span>

## <span data-ttu-id="6ad97-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ad97-181">RELATED LINKS</span></span>

<span data-ttu-id="6ad97-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="6ad97-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
