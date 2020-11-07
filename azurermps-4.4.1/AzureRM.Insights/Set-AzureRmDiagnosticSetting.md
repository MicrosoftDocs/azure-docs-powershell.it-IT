---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686829"
---
# <span data-ttu-id="b7964-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b7964-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="b7964-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7964-102">SYNOPSIS</span></span>
<span data-ttu-id="b7964-103">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b7964-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7964-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7964-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7964-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7964-105">DESCRIPTION</span></span>
<span data-ttu-id="b7964-106">Il cmdlet **set-AzureRmDiagnosticSetting** Abilita o disabilita ogni categoria di granulosità e log per la particolare risorsa.</span><span class="sxs-lookup"><span data-stu-id="b7964-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="b7964-107">I registri e le metriche sono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b7964-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="b7964-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7964-108">EXAMPLES</span></span>

### <span data-ttu-id="b7964-109">Esempio 1: abilitare tutte le metriche e i registri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="b7964-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="b7964-110">Questo comando consente di abilitare tutte le metriche e i registri disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="b7964-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="b7964-111">Esempio 2: disabilitare tutte le metriche e i registri</span><span class="sxs-lookup"><span data-stu-id="b7964-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="b7964-112">Questo comando Disabilita tutte le metriche e i registri disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="b7964-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="b7964-113">Esempio 3: abilitare più categorie</span><span class="sxs-lookup"><span data-stu-id="b7964-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="b7964-114">Questo comando consente di abilitare Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="b7964-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="b7964-115">Tutte le timegrains e le altre categorie restano invariate.</span><span class="sxs-lookup"><span data-stu-id="b7964-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="b7964-116">Esempio 4: abilitare una granulosità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="b7964-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="b7964-117">Questo comando consente di abilitare solo Categoria1, Categoria2 e Time Grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="b7964-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="b7964-118">Tutti gli altri grani e categorie di tempo sono invariati.</span><span class="sxs-lookup"><span data-stu-id="b7964-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="b7964-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7964-119">PARAMETERS</span></span>

### <span data-ttu-id="b7964-120">-Categorie</span><span class="sxs-lookup"><span data-stu-id="b7964-120">-Categories</span></span>
<span data-ttu-id="b7964-121">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="b7964-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="b7964-122">Se non specifichi una categoria, questo comando funziona in tutte le categorie.</span><span class="sxs-lookup"><span data-stu-id="b7964-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b7964-123">-Enabled</span></span>
<span data-ttu-id="b7964-124">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="b7964-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="b7964-125">Specificare $True per abilitare la diagnostica o $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="b7964-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7964-126">-ResourceId</span></span>
<span data-ttu-id="b7964-127">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b7964-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="b7964-128">-RetentionEnabled</span></span>
<span data-ttu-id="b7964-129">Indica se la conservazione delle informazioni di diagnostica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b7964-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b7964-130">-RetentionInDays</span></span>
<span data-ttu-id="b7964-131">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="b7964-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="b7964-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b7964-133">-StorageAccountId</span></span>
<span data-ttu-id="b7964-134">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="b7964-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="b7964-135">-Timegrains</span></span>
<span data-ttu-id="b7964-136">Specifica i grani temporali da abilitare o disabilitare per le metriche, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="b7964-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="b7964-137">Se non specifichi una granulosità temporale, questo comando funziona in tutti i grani temporali disponibili.</span><span class="sxs-lookup"><span data-stu-id="b7964-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b7964-138">-WorkspaceId</span></span>
<span data-ttu-id="b7964-139">ID dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b7964-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7964-140">-DefaultProfile</span></span>
<span data-ttu-id="b7964-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7964-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7964-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="b7964-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="b7964-143">ID regola dell'hub eventi</span><span class="sxs-lookup"><span data-stu-id="b7964-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7964-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7964-144">CommonParameters</span></span>
<span data-ttu-id="b7964-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7964-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7964-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7964-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7964-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7964-147">INPUTS</span></span>

## <span data-ttu-id="b7964-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7964-148">OUTPUTS</span></span>

### <span data-ttu-id="b7964-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="b7964-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="b7964-150">Note</span><span class="sxs-lookup"><span data-stu-id="b7964-150">NOTES</span></span>

## <span data-ttu-id="b7964-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7964-151">RELATED LINKS</span></span>

[<span data-ttu-id="b7964-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b7964-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


