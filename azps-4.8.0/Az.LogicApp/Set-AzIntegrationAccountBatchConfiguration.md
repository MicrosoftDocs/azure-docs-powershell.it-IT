---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189635"
---
# <span data-ttu-id="b12a5-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b12a5-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b12a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b12a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b12a5-103">Modifica la configurazione batch di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="b12a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b12a5-104">SYNTAX</span></span>

### <span data-ttu-id="b12a5-105">ByIntegrationAccountAndParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b12a5-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="b12a5-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="b12a5-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="b12a5-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="b12a5-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="b12a5-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="b12a5-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="b12a5-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b12a5-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="b12a5-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b12a5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b12a5-114">DESCRIPTION</span></span>
<span data-ttu-id="b12a5-115">Il cmdlet **set-AzIntegrationAccountBatchConfiguration** modifica la configurazione batch di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="b12a5-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b12a5-116">EXAMPLES</span></span>

### <span data-ttu-id="b12a5-117">Esempio 1: modificare una configurazione batch usando un file locale</span><span class="sxs-lookup"><span data-stu-id="b12a5-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b12a5-118">Modificare una configurazione batch denominata "sampleBatchConfig" usando il file locale che si trova nel percorso del file contenuto in "$batchConfigurationFilePath".</span><span class="sxs-lookup"><span data-stu-id="b12a5-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="b12a5-119">Esempio 2: modificare una configurazione batch tramite una stringa JSON</span><span class="sxs-lookup"><span data-stu-id="b12a5-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b12a5-120">Modificare una configurazione batch denominata "sampleBatchConfig" usando la stringa JSON contenuta in "$batchConfigurationContent".</span><span class="sxs-lookup"><span data-stu-id="b12a5-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="b12a5-121">Esempio 3: modificare una configurazione batch usando i parametri</span><span class="sxs-lookup"><span data-stu-id="b12a5-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="b12a5-122">Modificare una configurazione batch denominata "sampleBatchConfig" fornendo manualmente tutti i parametri necessari.</span><span class="sxs-lookup"><span data-stu-id="b12a5-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="b12a5-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b12a5-123">PARAMETERS</span></span>

### <span data-ttu-id="b12a5-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="b12a5-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="b12a5-125">Definizione della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="b12a5-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="b12a5-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="b12a5-127">Percorso del file di configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="b12a5-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="b12a5-128">-BatchGroupName</span></span>
<span data-ttu-id="b12a5-129">Nome del gruppo Configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="b12a5-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b12a5-130">-BatchSize</span></span>
<span data-ttu-id="b12a5-131">Dimensione batch configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="b12a5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12a5-132">-DefaultProfile</span></span>
<span data-ttu-id="b12a5-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b12a5-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b12a5-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b12a5-134">-InputObject</span></span>
<span data-ttu-id="b12a5-135">Configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="b12a5-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="b12a5-136">-MessageCount</span></span>
<span data-ttu-id="b12a5-137">Conteggio messaggi configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="b12a5-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b12a5-138">-Metadata</span></span>
<span data-ttu-id="b12a5-139">Metadati della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="b12a5-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="b12a5-140">-Name</span></span>
<span data-ttu-id="b12a5-141">Nome della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="b12a5-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="b12a5-142">-ParentName</span></span>
<span data-ttu-id="b12a5-143">Nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-143">The integration account name.</span></span>

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

### <span data-ttu-id="b12a5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b12a5-144">-ResourceGroupName</span></span>
<span data-ttu-id="b12a5-145">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b12a5-145">The resource group name.</span></span>

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

### <span data-ttu-id="b12a5-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b12a5-146">-ResourceId</span></span>
<span data-ttu-id="b12a5-147">ID risorsa configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="b12a5-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="b12a5-148">-ScheduleFrequency</span></span>
<span data-ttu-id="b12a5-149">Frequenza della pianificazione della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="b12a5-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="b12a5-150">-ScheduleInterval</span></span>
<span data-ttu-id="b12a5-151">Intervallo di programmazione configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="b12a5-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="b12a5-152">-ScheduleStartTime</span></span>
<span data-ttu-id="b12a5-153">L'ora di inizio della pianificazione della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="b12a5-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="b12a5-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="b12a5-155">Il fuso orario della pianificazione della configurazione batch account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b12a5-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="b12a5-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b12a5-156">-Confirm</span></span>
<span data-ttu-id="b12a5-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b12a5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b12a5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b12a5-158">-WhatIf</span></span>
<span data-ttu-id="b12a5-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b12a5-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b12a5-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b12a5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b12a5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12a5-161">CommonParameters</span></span>
<span data-ttu-id="b12a5-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b12a5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12a5-163">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b12a5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12a5-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b12a5-164">INPUTS</span></span>

### <span data-ttu-id="b12a5-165">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b12a5-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="b12a5-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b12a5-166">System.String</span></span>

## <span data-ttu-id="b12a5-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b12a5-167">OUTPUTS</span></span>

### <span data-ttu-id="b12a5-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b12a5-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="b12a5-169">Note</span><span class="sxs-lookup"><span data-stu-id="b12a5-169">NOTES</span></span>

## <span data-ttu-id="b12a5-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b12a5-170">RELATED LINKS</span></span>