---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 5a9594c4261e3de99090d875e07997668fadea57
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398972"
---
# <span data-ttu-id="5ca02-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5ca02-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="5ca02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca02-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca02-103">Imposta le impostazioni di log e metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ca02-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="5ca02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ca02-104">SYNTAX</span></span>

### <span data-ttu-id="5ca02-105">OldSetDiagnosticSetting (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5ca02-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca02-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5ca02-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca02-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ca02-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca02-108">Il cmdlet **Set-AzDiagnosticSetting** abilita o disabilita ogni grana temporale e categoria di log per la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="5ca02-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="5ca02-109">I log e le metriche vengono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="5ca02-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="5ca02-110">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ca02-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5ca02-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ca02-111">EXAMPLES</span></span>

### <span data-ttu-id="5ca02-112">Esempio 1: Abilitare tutte le metriche e i log per una risorsa</span><span class="sxs-lookup"><span data-stu-id="5ca02-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="5ca02-113">Questo comando abilita tutte le metriche e i log disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="5ca02-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="5ca02-114">Esempio 2: Disabilitare tutte le metriche e i log</span><span class="sxs-lookup"><span data-stu-id="5ca02-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="5ca02-115">Questo comando disabilita tutte le metriche e i log disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="5ca02-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="5ca02-116">Esempio 3: Abilitare/disabilitare più categorie di metriche</span><span class="sxs-lookup"><span data-stu-id="5ca02-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="5ca02-117">Questo comando disabilita le categorie di metriche denominate Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="5ca02-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="5ca02-118">Tutte le altre categorie rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="5ca02-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="5ca02-119">Esempio 4: Abilitare/disabilitare più categorie di log</span><span class="sxs-lookup"><span data-stu-id="5ca02-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="5ca02-120">Questo comando abilita Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="5ca02-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="5ca02-121">Tutte le altre metriche e le categorie di log rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="5ca02-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="5ca02-122">Esempio 4: Abilitare le granularità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="5ca02-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="5ca02-123">Questo comando abilita solo Categoria1, Categoria2 e Grana temporale PT1M.</span><span class="sxs-lookup"><span data-stu-id="5ca02-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="5ca02-124">Tutti gli altri grani e categorie rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="5ca02-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="5ca02-125">Esempio 5: Uso della pipeline</span><span class="sxs-lookup"><span data-stu-id="5ca02-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="5ca02-126">Questo comando usa la pipeline di PowerShell per impostare (senza alcuna modifica) un'impostazione diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5ca02-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="5ca02-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ca02-127">PARAMETERS</span></span>

### <span data-ttu-id="5ca02-128">-Categoria</span><span class="sxs-lookup"><span data-stu-id="5ca02-128">-Category</span></span>
<span data-ttu-id="5ca02-129">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Abilitato.*</span><span class="sxs-lookup"><span data-stu-id="5ca02-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="5ca02-130">Se non viene specificata alcuna categoria, questo comando opera su tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="5ca02-130">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="5ca02-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca02-131">-DefaultProfile</span></span>
<span data-ttu-id="5ca02-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5ca02-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ca02-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5ca02-133">-Enabled</span></span>
<span data-ttu-id="5ca02-134">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5ca02-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="5ca02-135">Specificare $True per abilitare la diagnostica oppure specificare $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5ca02-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="5ca02-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="5ca02-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="5ca02-137">ID regola di autorizzazione hub eventi</span><span class="sxs-lookup"><span data-stu-id="5ca02-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="5ca02-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="5ca02-138">-EventHubName</span></span>
<span data-ttu-id="5ca02-139">Nome dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="5ca02-139">The event hub name</span></span>

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

### <span data-ttu-id="5ca02-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="5ca02-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="5ca02-141">Flag che indica che l'esportazione in La deve essere eseguita in una tabella specifica della risorsa, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="5ca02-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="5ca02-142">dedicato o tabella dello schema fissa,  a differenza della tabella dello schema dinamico predefinita denominata **AzureDiagnostics.**</span><span class="sxs-lookup"><span data-stu-id="5ca02-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="5ca02-143">Questo argomento è valido solo quando viene specificato anche **l'argomento -workspaceId.**</span><span class="sxs-lookup"><span data-stu-id="5ca02-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca02-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ca02-144">-InputObject</span></span>
<span data-ttu-id="5ca02-145">Oggetto di input (possibile dalla pipeline). Il nome e resourceId verranno estratti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ca02-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="5ca02-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="5ca02-146">-MetricCategory</span></span>
<span data-ttu-id="5ca02-147">Elenco delle categorie metriche.</span><span class="sxs-lookup"><span data-stu-id="5ca02-147">The list of metric categories.</span></span>
<span data-ttu-id="5ca02-148">Se non viene specificata alcuna categoria, questo comando opera su tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="5ca02-148">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="5ca02-149">-Name</span><span class="sxs-lookup"><span data-stu-id="5ca02-149">-Name</span></span>
<span data-ttu-id="5ca02-150">Nome dell'impostazione diagnostica.</span><span class="sxs-lookup"><span data-stu-id="5ca02-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="5ca02-151">Il valore predefinito è **servizio.**</span><span class="sxs-lookup"><span data-stu-id="5ca02-151">The default value is **service**.</span></span>

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

### <span data-ttu-id="5ca02-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca02-152">-ResourceId</span></span>
<span data-ttu-id="5ca02-153">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5ca02-153">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="5ca02-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="5ca02-154">-RetentionEnabled</span></span>
<span data-ttu-id="5ca02-155">Indica se la conservazione delle informazioni diagnostiche è abilitata.</span><span class="sxs-lookup"><span data-stu-id="5ca02-155">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="5ca02-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5ca02-156">-RetentionInDays</span></span>
<span data-ttu-id="5ca02-157">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="5ca02-157">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="5ca02-158">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="5ca02-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="5ca02-159">ID regola bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="5ca02-159">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="5ca02-160">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5ca02-160">-StorageAccountId</span></span>
<span data-ttu-id="5ca02-161">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="5ca02-161">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="5ca02-162">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="5ca02-162">-Timegrain</span></span>
<span data-ttu-id="5ca02-163">Specifica i grani tempo da abilitare o disabilitare per le metriche, in base al valore di *Abilitato.*</span><span class="sxs-lookup"><span data-stu-id="5ca02-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="5ca02-164">Se non si specificano le granularità per l'ora, questo comando viene eseguito in tutte le grane disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ca02-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="5ca02-165">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5ca02-165">-WorkspaceId</span></span>
<span data-ttu-id="5ca02-166">ID della risorsa dell'area di lavoro Analisi log a cui inviare log/metriche</span><span class="sxs-lookup"><span data-stu-id="5ca02-166">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="5ca02-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ca02-167">-Confirm</span></span>
<span data-ttu-id="5ca02-168">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca02-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca02-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca02-169">-WhatIf</span></span>
<span data-ttu-id="5ca02-170">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ca02-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ca02-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ca02-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca02-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca02-172">CommonParameters</span></span>
<span data-ttu-id="5ca02-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca02-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca02-174">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ca02-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca02-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ca02-175">INPUTS</span></span>

### <span data-ttu-id="5ca02-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="5ca02-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="5ca02-177">System.String</span><span class="sxs-lookup"><span data-stu-id="5ca02-177">System.String</span></span>

### <span data-ttu-id="5ca02-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ca02-178">System.Boolean</span></span>

### <span data-ttu-id="5ca02-179">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ca02-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5ca02-180">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ca02-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5ca02-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ca02-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5ca02-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ca02-182">OUTPUTS</span></span>

### <span data-ttu-id="5ca02-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="5ca02-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="5ca02-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ca02-184">NOTES</span></span>

## <span data-ttu-id="5ca02-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ca02-185">RELATED LINKS</span></span>

<span data-ttu-id="5ca02-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="5ca02-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
