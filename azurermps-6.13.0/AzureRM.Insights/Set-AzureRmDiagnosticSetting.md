---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: ee7d753ac81a55bf563742f87de7e195c89fb644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688420"
---
# <span data-ttu-id="e018e-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e018e-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="e018e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e018e-102">SYNOPSIS</span></span>
<span data-ttu-id="e018e-103">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e018e-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e018e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e018e-104">SYNTAX</span></span>

### <span data-ttu-id="e018e-105">OldSetDiagnosticSetting (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e018e-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e018e-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e018e-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e018e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e018e-107">DESCRIPTION</span></span>
<span data-ttu-id="e018e-108">Il cmdlet **set-AzureRmDiagnosticSetting** Abilita o disabilita ogni categoria di granulosità e log per la particolare risorsa.</span><span class="sxs-lookup"><span data-stu-id="e018e-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="e018e-109">I registri e le metriche sono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="e018e-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="e018e-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e018e-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e018e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e018e-111">EXAMPLES</span></span>

### <span data-ttu-id="e018e-112">Esempio 1: abilitare tutte le metriche e i registri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="e018e-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="e018e-113">Questo comando consente di abilitare tutte le metriche e i registri disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="e018e-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="e018e-114">Esempio 2: disabilitare tutte le metriche e i registri</span><span class="sxs-lookup"><span data-stu-id="e018e-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="e018e-115">Questo comando Disabilita tutte le metriche e i registri disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="e018e-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="e018e-116">Esempio 3: abilitare/disabilitare più categorie di metriche</span><span class="sxs-lookup"><span data-stu-id="e018e-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="e018e-117">Questo comando consente di abilitare le metriche cateories chiamate Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="e018e-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="e018e-118">Tutte le altre categorie restano invariate.</span><span class="sxs-lookup"><span data-stu-id="e018e-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="e018e-119">Esempio 4: abilitare/disabilitare più categorie di log</span><span class="sxs-lookup"><span data-stu-id="e018e-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="e018e-120">Questo comando consente di abilitare Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="e018e-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="e018e-121">Tutte le altre categorie di metriche e registri restano le stesse.</span><span class="sxs-lookup"><span data-stu-id="e018e-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="e018e-122">Esempio 4: abilitare una granulosità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="e018e-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="e018e-123">Questo comando consente di abilitare solo Categoria1, Categoria2 e Time Grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="e018e-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="e018e-124">Tutti gli altri grani e categorie di tempo sono invariati.</span><span class="sxs-lookup"><span data-stu-id="e018e-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="e018e-125">Esempio 5: uso della pipeline</span><span class="sxs-lookup"><span data-stu-id="e018e-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="e018e-126">Questo comando usa la pipeline di PowerShell per impostare (non apportare modifiche) un'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e018e-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="e018e-127">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e018e-127">PARAMETERS</span></span>

### <span data-ttu-id="e018e-128">-Categorie</span><span class="sxs-lookup"><span data-stu-id="e018e-128">-Categories</span></span>
<span data-ttu-id="e018e-129">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="e018e-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="e018e-130">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="e018e-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e018e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e018e-131">-DefaultProfile</span></span>
<span data-ttu-id="e018e-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e018e-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e018e-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e018e-133">-Enabled</span></span>
<span data-ttu-id="e018e-134">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e018e-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="e018e-135">Specificare $True per abilitare la diagnostica o $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e018e-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="e018e-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="e018e-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="e018e-137">ID regola di autorizzazione Hub eventi</span><span class="sxs-lookup"><span data-stu-id="e018e-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="e018e-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e018e-138">-EventHubName</span></span>
<span data-ttu-id="e018e-139">Nome Hub dell'evento</span><span class="sxs-lookup"><span data-stu-id="e018e-139">The event hub name</span></span>

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

### <span data-ttu-id="e018e-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e018e-140">-InputObject</span></span>
<span data-ttu-id="e018e-141">L'oggetto di input (possibile dalla pipeline) Il nome e resourceId verranno estratti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e018e-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="e018e-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="e018e-142">-MetricCategory</span></span>
<span data-ttu-id="e018e-143">Elenco di categorie metriche.</span><span class="sxs-lookup"><span data-stu-id="e018e-143">The list of metric categories.</span></span> <span data-ttu-id="e018e-144">Se non è specificata alcuna categoria, questo comando funziona in tutte le categorie supportate.</span><span class="sxs-lookup"><span data-stu-id="e018e-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="e018e-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="e018e-145">-Name</span></span>
<span data-ttu-id="e018e-146">Nome dell'impostazione di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="e018e-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="e018e-147">Il valore predefinito è **Service**.</span><span class="sxs-lookup"><span data-stu-id="e018e-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="e018e-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e018e-148">-ResourceId</span></span>
<span data-ttu-id="e018e-149">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e018e-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="e018e-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="e018e-150">-RetentionEnabled</span></span>
<span data-ttu-id="e018e-151">Indica se la conservazione delle informazioni di diagnostica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e018e-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="e018e-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e018e-152">-RetentionInDays</span></span>
<span data-ttu-id="e018e-153">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="e018e-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="e018e-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="e018e-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="e018e-155">ID regola del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="e018e-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="e018e-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e018e-156">-StorageAccountId</span></span>
<span data-ttu-id="e018e-157">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="e018e-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="e018e-158">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="e018e-158">-Timegrains</span></span>
<span data-ttu-id="e018e-159">Specifica i grani temporali da abilitare o disabilitare per le metriche, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="e018e-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="e018e-160">Se non specifichi una granulosità temporale, questo comando funziona in tutti i grani temporali disponibili.</span><span class="sxs-lookup"><span data-stu-id="e018e-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e018e-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="e018e-161">-WorkspaceId</span></span>
<span data-ttu-id="e018e-162">ID dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="e018e-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="e018e-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e018e-163">-Confirm</span></span>
<span data-ttu-id="e018e-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e018e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e018e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e018e-165">-WhatIf</span></span>
<span data-ttu-id="e018e-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e018e-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e018e-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e018e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e018e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e018e-168">CommonParameters</span></span>
<span data-ttu-id="e018e-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e018e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e018e-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e018e-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e018e-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e018e-171">INPUTS</span></span>

### <span data-ttu-id="e018e-172">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="e018e-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="e018e-173">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e018e-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e018e-174">System. String</span><span class="sxs-lookup"><span data-stu-id="e018e-174">System.String</span></span>

### <span data-ttu-id="e018e-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e018e-175">System.Boolean</span></span>

### <span data-ttu-id="e018e-176">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e018e-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e018e-177">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e018e-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e018e-178">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e018e-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e018e-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e018e-179">OUTPUTS</span></span>

### <span data-ttu-id="e018e-180">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="e018e-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="e018e-181">Note</span><span class="sxs-lookup"><span data-stu-id="e018e-181">NOTES</span></span>

## <span data-ttu-id="e018e-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e018e-182">RELATED LINKS</span></span>

<span data-ttu-id="e018e-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="e018e-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
