---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203729"
---
# <span data-ttu-id="15409-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15409-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="15409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15409-102">SYNOPSIS</span></span>
<span data-ttu-id="15409-103">Crea una configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="15409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15409-104">SYNTAX</span></span>

### <span data-ttu-id="15409-105">ByIntegrationAccountAndParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15409-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="15409-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="15409-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="15409-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="15409-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="15409-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="15409-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="15409-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15409-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="15409-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15409-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15409-114">DESCRIPTION</span></span>
<span data-ttu-id="15409-115">Il cmdlet **Get-AzIntegrationAccountBatchConfiguration crea** una nuova configurazione batch in un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="15409-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15409-116">EXAMPLES</span></span>

### <span data-ttu-id="15409-117">Esempio 1: Creare una nuova configurazione batch usando un file locale</span><span class="sxs-lookup"><span data-stu-id="15409-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="15409-118">Crea una nuova configurazione batch usando il file locale che si trova nel percorso del file contenuto in "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="15409-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="15409-119">Esempio 2: Creare una nuova configurazione batch usando una stringa JSON</span><span class="sxs-lookup"><span data-stu-id="15409-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="15409-120">Crea una nuova configurazione batch usando la stringa JSON contenuta in "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="15409-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="15409-121">Esempio 3: Creare una nuova configurazione batch usando parametri</span><span class="sxs-lookup"><span data-stu-id="15409-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="15409-122">Crea una nuova configurazione batch fornendo manualmente tutti i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="15409-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="15409-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15409-123">PARAMETERS</span></span>

### <span data-ttu-id="15409-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="15409-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="15409-125">Definizione di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="15409-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="15409-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="15409-127">Percorso del file di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="15409-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="15409-128">-BatchGroupName</span></span>
<span data-ttu-id="15409-129">Nome del gruppo di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="15409-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="15409-130">-BatchSize</span></span>
<span data-ttu-id="15409-131">Dimensioni del batch di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="15409-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15409-132">-DefaultProfile</span></span>
<span data-ttu-id="15409-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15409-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15409-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="15409-134">-MessageCount</span></span>
<span data-ttu-id="15409-135">Numero di messaggi di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="15409-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="15409-136">-Metadata</span></span>
<span data-ttu-id="15409-137">Metadati di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="15409-138">-Name</span><span class="sxs-lookup"><span data-stu-id="15409-138">-Name</span></span>
<span data-ttu-id="15409-139">Nome di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15409-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="15409-140">-ParentName</span></span>
<span data-ttu-id="15409-141">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-141">The integration account name.</span></span>

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

### <span data-ttu-id="15409-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="15409-142">-ParentObject</span></span>
<span data-ttu-id="15409-143">Oggetto account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15409-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="15409-144">-ParentResourceId</span></span>
<span data-ttu-id="15409-145">ID risorsa di configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="15409-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15409-146">-ResourceGroupName</span></span>
<span data-ttu-id="15409-147">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15409-147">The resource group name.</span></span>

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

### <span data-ttu-id="15409-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="15409-148">-ScheduleFrequency</span></span>
<span data-ttu-id="15409-149">Frequenza della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="15409-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="15409-150">-ScheduleInterval</span></span>
<span data-ttu-id="15409-151">Intervallo di pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="15409-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="15409-152">-ScheduleStartTime</span></span>
<span data-ttu-id="15409-153">Ora di inizio della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="15409-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="15409-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="15409-155">Fuso orario della pianificazione della configurazione batch dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="15409-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="15409-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15409-156">-Confirm</span></span>
<span data-ttu-id="15409-157">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15409-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15409-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15409-158">-WhatIf</span></span>
<span data-ttu-id="15409-159">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15409-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15409-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15409-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15409-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15409-161">CommonParameters</span></span>
<span data-ttu-id="15409-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15409-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15409-163">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15409-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15409-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="15409-164">INPUTS</span></span>

### <span data-ttu-id="15409-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15409-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="15409-166">System.String</span><span class="sxs-lookup"><span data-stu-id="15409-166">System.String</span></span>

## <span data-ttu-id="15409-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15409-167">OUTPUTS</span></span>

### <span data-ttu-id="15409-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="15409-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="15409-169">NOTE</span><span class="sxs-lookup"><span data-stu-id="15409-169">NOTES</span></span>

## <span data-ttu-id="15409-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15409-170">RELATED LINKS</span></span>
