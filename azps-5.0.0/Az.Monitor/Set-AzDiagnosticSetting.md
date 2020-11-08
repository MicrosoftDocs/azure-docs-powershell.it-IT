---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: eeadf64c83f62a8d245a7ace8f750b34ddc230ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200040"
---
# <span data-ttu-id="925d2-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="925d2-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="925d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="925d2-102">SYNOPSIS</span></span>
<span data-ttu-id="925d2-103">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="925d2-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="925d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="925d2-104">SYNTAX</span></span>

### <span data-ttu-id="925d2-105">OldSetDiagnosticSetting (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="925d2-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="925d2-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="925d2-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="925d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="925d2-107">DESCRIPTION</span></span>
<span data-ttu-id="925d2-108">Il cmdlet **set-AzDiagnosticSetting** Abilita o disabilita ogni categoria di granulosità e log per la particolare risorsa.</span><span class="sxs-lookup"><span data-stu-id="925d2-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="925d2-109">I registri e le metriche sono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="925d2-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="925d2-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="925d2-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="925d2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="925d2-111">EXAMPLES</span></span>

### <span data-ttu-id="925d2-112">Esempio 1: abilitare tutte le metriche e i registri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="925d2-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="925d2-113">Questo comando consente di abilitare tutte le metriche e i registri disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="925d2-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="925d2-114">Esempio 2: disabilitare tutte le metriche e i registri</span><span class="sxs-lookup"><span data-stu-id="925d2-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="925d2-115">Questo comando Disabilita tutte le metriche e i registri disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="925d2-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="925d2-116">Esempio 3: abilitare/disabilitare più categorie di metriche</span><span class="sxs-lookup"><span data-stu-id="925d2-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
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

<span data-ttu-id="925d2-117">Questo comando Disabilita le categorie metriche denominate Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="925d2-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="925d2-118">Tutte le altre categorie restano invariate.</span><span class="sxs-lookup"><span data-stu-id="925d2-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="925d2-119">Esempio 4: abilitare/disabilitare più categorie di log</span><span class="sxs-lookup"><span data-stu-id="925d2-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
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

<span data-ttu-id="925d2-120">Questo comando consente di abilitare Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="925d2-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="925d2-121">Tutte le altre categorie di metriche e registri restano le stesse.</span><span class="sxs-lookup"><span data-stu-id="925d2-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="925d2-122">Esempio 5: abilitare una granulosità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="925d2-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="925d2-123">Questo comando consente di abilitare solo Categoria1, Categoria2 e Time Grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="925d2-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="925d2-124">Tutti gli altri grani e categorie di tempo sono invariati.</span><span class="sxs-lookup"><span data-stu-id="925d2-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="925d2-125">Esempio 6: uso della pipeline</span><span class="sxs-lookup"><span data-stu-id="925d2-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="925d2-126">Questo comando usa la pipeline di PowerShell per impostare (nessuna modifica apportata) un'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="925d2-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="925d2-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="925d2-127">PARAMETERS</span></span>

### <span data-ttu-id="925d2-128">-Categoria</span><span class="sxs-lookup"><span data-stu-id="925d2-128">-Category</span></span>
<span data-ttu-id="925d2-129">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="925d2-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="925d2-130">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="925d2-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="925d2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925d2-131">-DefaultProfile</span></span>
<span data-ttu-id="925d2-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="925d2-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="925d2-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="925d2-133">-Enabled</span></span>
<span data-ttu-id="925d2-134">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="925d2-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="925d2-135">Specificare $True per abilitare la diagnostica o $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="925d2-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="925d2-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="925d2-136">-EnableLog</span></span>
<span data-ttu-id="925d2-137">Valore che indica se i log di diagnostica devono essere abilitati o disabilitati</span><span class="sxs-lookup"><span data-stu-id="925d2-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

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

### <span data-ttu-id="925d2-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="925d2-138">-EnableMetrics</span></span>
<span data-ttu-id="925d2-139">Valore che indica se le metriche di diagnostica devono essere abilitate o disabilitate</span><span class="sxs-lookup"><span data-stu-id="925d2-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

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

### <span data-ttu-id="925d2-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="925d2-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="925d2-141">ID regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="925d2-141">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="925d2-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="925d2-142">-EventHubName</span></span>
<span data-ttu-id="925d2-143">Nome Hub dell'evento</span><span class="sxs-lookup"><span data-stu-id="925d2-143">The event hub name</span></span>

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

### <span data-ttu-id="925d2-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="925d2-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="925d2-145">Contrassegno che indica che l'esportazione in LA deve essere eseguita in una tabella specifica delle risorse, alias</span><span class="sxs-lookup"><span data-stu-id="925d2-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="925d2-146">tabella schema dedicata o fissa, invece della tabella schema dinamico **predefinita** denominata **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="925d2-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="925d2-147">Questo argomento è efficace solo quando viene assegnato anche l'argomento **-workspaceId** .</span><span class="sxs-lookup"><span data-stu-id="925d2-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

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

### <span data-ttu-id="925d2-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="925d2-148">-InputObject</span></span>
<span data-ttu-id="925d2-149">L'oggetto di input (possibile dalla pipeline) Il nome e resourceId verranno estratti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="925d2-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="925d2-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="925d2-150">-MetricCategory</span></span>
<span data-ttu-id="925d2-151">Elenco di categorie metriche.</span><span class="sxs-lookup"><span data-stu-id="925d2-151">The list of metric categories.</span></span> <span data-ttu-id="925d2-152">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="925d2-152">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="925d2-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="925d2-153">-Name</span></span>
<span data-ttu-id="925d2-154">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="925d2-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="925d2-155">Il valore predefinito è **Service**.</span><span class="sxs-lookup"><span data-stu-id="925d2-155">The default value is **service**.</span></span>

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

### <span data-ttu-id="925d2-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="925d2-156">-ResourceId</span></span>
<span data-ttu-id="925d2-157">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="925d2-157">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="925d2-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="925d2-158">-RetentionEnabled</span></span>
<span data-ttu-id="925d2-159">Indica se la conservazione delle informazioni di diagnostica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="925d2-159">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="925d2-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="925d2-160">-RetentionInDays</span></span>
<span data-ttu-id="925d2-161">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="925d2-161">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="925d2-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="925d2-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="925d2-163">ID regola del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="925d2-163">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="925d2-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="925d2-164">-StorageAccountId</span></span>
<span data-ttu-id="925d2-165">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="925d2-165">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="925d2-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="925d2-166">-Timegrain</span></span>
<span data-ttu-id="925d2-167">Specifica i grani temporali da abilitare o disabilitare per le metriche, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="925d2-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="925d2-168">Se non specifichi una granulosità temporale, questo comando funziona in tutti i grani temporali disponibili.</span><span class="sxs-lookup"><span data-stu-id="925d2-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="925d2-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="925d2-169">-WorkspaceId</span></span>
<span data-ttu-id="925d2-170">ID risorsa dell'area di lavoro analisi log per l'invio di registri/metriche a</span><span class="sxs-lookup"><span data-stu-id="925d2-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="925d2-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="925d2-171">-Confirm</span></span>
<span data-ttu-id="925d2-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="925d2-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="925d2-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="925d2-173">-WhatIf</span></span>
<span data-ttu-id="925d2-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="925d2-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="925d2-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="925d2-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="925d2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925d2-176">CommonParameters</span></span>
<span data-ttu-id="925d2-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="925d2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925d2-178">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="925d2-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925d2-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="925d2-179">INPUTS</span></span>

### <span data-ttu-id="925d2-180">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="925d2-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="925d2-181">System. String</span><span class="sxs-lookup"><span data-stu-id="925d2-181">System.String</span></span>

### <span data-ttu-id="925d2-182">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="925d2-182">System.Boolean</span></span>

### <span data-ttu-id="925d2-183">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="925d2-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="925d2-184">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="925d2-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="925d2-185">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="925d2-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="925d2-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="925d2-186">OUTPUTS</span></span>

### <span data-ttu-id="925d2-187">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="925d2-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="925d2-188">Note</span><span class="sxs-lookup"><span data-stu-id="925d2-188">NOTES</span></span>

## <span data-ttu-id="925d2-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="925d2-189">RELATED LINKS</span></span>

<span data-ttu-id="925d2-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="925d2-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
