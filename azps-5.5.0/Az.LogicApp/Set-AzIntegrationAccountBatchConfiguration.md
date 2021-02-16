---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194199"
---
# <span data-ttu-id="e12ef-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e12ef-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e12ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e12ef-103">Modifica una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="e12ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e12ef-104">SYNTAX</span></span>

### <span data-ttu-id="e12ef-105">ByIntegrationAccountAndParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e12ef-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="e12ef-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e12ef-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="e12ef-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e12ef-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="e12ef-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="e12ef-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e12ef-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e12ef-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="e12ef-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e12ef-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e12ef-114">DESCRIPTION</span></span>
<span data-ttu-id="e12ef-115">Il cmdlet **Set-AzIntegrationAccountBatchConfiguration** modifica una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="e12ef-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e12ef-116">EXAMPLES</span></span>

### <span data-ttu-id="e12ef-117">Esempio 1: Modificare una configurazione batch usando un file locale</span><span class="sxs-lookup"><span data-stu-id="e12ef-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e12ef-118">Modificare una configurazione batch denominata "sampleBatchConfig" usando il file locale che si trova nel percorso del file contenuto in "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="e12ef-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="e12ef-119">Esempio 2: Modificare una configurazione batch usando una stringa JSON</span><span class="sxs-lookup"><span data-stu-id="e12ef-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e12ef-120">Modificare una configurazione batch denominata "sampleBatchConfig" usando una stringa JSON contenuta in "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="e12ef-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="e12ef-121">Esempio 3: Modificare una configurazione batch usando parametri</span><span class="sxs-lookup"><span data-stu-id="e12ef-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e12ef-122">Modificare una configurazione batch denominata "sampleBatchConfig" fornendo manualmente tutti i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="e12ef-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="e12ef-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12ef-123">PARAMETERS</span></span>

### <span data-ttu-id="e12ef-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="e12ef-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="e12ef-125">Definizione di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="e12ef-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="e12ef-127">Percorso del file di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="e12ef-128">-BatchGroupName</span></span>
<span data-ttu-id="e12ef-129">Nome del gruppo di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="e12ef-130">-BatchSize</span></span>
<span data-ttu-id="e12ef-131">Dimensioni del batch di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12ef-132">-DefaultProfile</span></span>
<span data-ttu-id="e12ef-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e12ef-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e12ef-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e12ef-134">-InputObject</span></span>
<span data-ttu-id="e12ef-135">Configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e12ef-136">-MessageCount</span></span>
<span data-ttu-id="e12ef-137">Numero di messaggi di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e12ef-138">-Metadata</span></span>
<span data-ttu-id="e12ef-139">Metadati di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-140">-Name</span><span class="sxs-lookup"><span data-stu-id="e12ef-140">-Name</span></span>
<span data-ttu-id="e12ef-141">Nome di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e12ef-142">-ParentName</span></span>
<span data-ttu-id="e12ef-143">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e12ef-144">-ResourceGroupName</span></span>
<span data-ttu-id="e12ef-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e12ef-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e12ef-146">-ResourceId</span></span>
<span data-ttu-id="e12ef-147">ID risorsa di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="e12ef-148">-ScheduleFrequency</span></span>
<span data-ttu-id="e12ef-149">Frequenza della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="e12ef-150">-ScheduleInterval</span></span>
<span data-ttu-id="e12ef-151">Intervallo di pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="e12ef-152">-ScheduleStartTime</span></span>
<span data-ttu-id="e12ef-153">Ora di inizio della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="e12ef-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="e12ef-155">Fuso orario della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e12ef-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e12ef-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e12ef-156">-Confirm</span></span>
<span data-ttu-id="e12ef-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e12ef-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e12ef-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e12ef-158">-WhatIf</span></span>
<span data-ttu-id="e12ef-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e12ef-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e12ef-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e12ef-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e12ef-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12ef-161">CommonParameters</span></span>
<span data-ttu-id="e12ef-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12ef-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12ef-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e12ef-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12ef-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="e12ef-164">INPUTS</span></span>

### <span data-ttu-id="e12ef-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e12ef-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="e12ef-166">System.String</span><span class="sxs-lookup"><span data-stu-id="e12ef-166">System.String</span></span>

## <span data-ttu-id="e12ef-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e12ef-167">OUTPUTS</span></span>

### <span data-ttu-id="e12ef-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e12ef-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e12ef-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="e12ef-169">NOTES</span></span>

## <span data-ttu-id="e12ef-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e12ef-170">RELATED LINKS</span></span>
