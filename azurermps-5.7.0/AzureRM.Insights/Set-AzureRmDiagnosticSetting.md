---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 086ca93f7b975f6c9b7f4de806dac0c7c99012b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509860"
---
# <span data-ttu-id="0768f-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0768f-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="0768f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0768f-102">SYNOPSIS</span></span>
<span data-ttu-id="0768f-103">Imposta le impostazioni dei registri e delle metriche per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0768f-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0768f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0768f-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0768f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0768f-105">DESCRIPTION</span></span>
<span data-ttu-id="0768f-106">Il cmdlet **set-AzureRmDiagnosticSetting** Abilita o disabilita ogni categoria di granulosità e log per la particolare risorsa.</span><span class="sxs-lookup"><span data-stu-id="0768f-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="0768f-107">I registri e le metriche sono archiviati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0768f-107">The logs and metrics are stored in the specified storage account.</span></span>

<span data-ttu-id="0768f-108">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0768f-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0768f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0768f-109">EXAMPLES</span></span>

### <span data-ttu-id="0768f-110">Esempio 1: abilitare tutte le metriche e i registri per una risorsa</span><span class="sxs-lookup"><span data-stu-id="0768f-110">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="0768f-111">Questo comando consente di abilitare tutte le metriche e i registri disponibili per Resource01.</span><span class="sxs-lookup"><span data-stu-id="0768f-111">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="0768f-112">Esempio 2: disabilitare tutte le metriche e i registri</span><span class="sxs-lookup"><span data-stu-id="0768f-112">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="0768f-113">Questo comando Disabilita tutte le metriche e i registri disponibili per la risorsa Resource01.</span><span class="sxs-lookup"><span data-stu-id="0768f-113">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="0768f-114">Esempio 3: abilitare più categorie</span><span class="sxs-lookup"><span data-stu-id="0768f-114">Example 3: Enable multiple categories</span></span>
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

<span data-ttu-id="0768f-115">Questo comando consente di abilitare Categoria1 e Categoria2.</span><span class="sxs-lookup"><span data-stu-id="0768f-115">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="0768f-116">Tutte le timegrains e le altre categorie restano invariate.</span><span class="sxs-lookup"><span data-stu-id="0768f-116">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="0768f-117">Esempio 4: abilitare una granulosità temporale e più categorie</span><span class="sxs-lookup"><span data-stu-id="0768f-117">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="0768f-118">Questo comando consente di abilitare solo Categoria1, Categoria2 e Time Grain PT1M.</span><span class="sxs-lookup"><span data-stu-id="0768f-118">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="0768f-119">Tutti gli altri grani e categorie di tempo sono invariati.</span><span class="sxs-lookup"><span data-stu-id="0768f-119">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="0768f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0768f-120">PARAMETERS</span></span>

### <span data-ttu-id="0768f-121">-Categorie</span><span class="sxs-lookup"><span data-stu-id="0768f-121">-Categories</span></span>
<span data-ttu-id="0768f-122">Specifica l'elenco delle categorie di log da abilitare o disabilitare, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="0768f-122">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="0768f-123">Se non specifichi una categoria, questo comando funziona in tutte le categorie.</span><span class="sxs-lookup"><span data-stu-id="0768f-123">If you do not specify a category, this command operates on all categories.</span></span>

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

### <span data-ttu-id="0768f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0768f-124">-DefaultProfile</span></span>
<span data-ttu-id="0768f-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0768f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-126">-Enabled</span><span class="sxs-lookup"><span data-stu-id="0768f-126">-Enabled</span></span>
<span data-ttu-id="0768f-127">Indica se abilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0768f-127">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="0768f-128">Specificare $True per abilitare la diagnostica o $False per disabilitare la diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0768f-128">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-129">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="0768f-129">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="0768f-130">Regola dell'hub eventi i</span><span class="sxs-lookup"><span data-stu-id="0768f-130">The event hub rule i</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0768f-131">-ResourceId</span></span>
<span data-ttu-id="0768f-132">Specifica l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0768f-132">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-133">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="0768f-133">-RetentionEnabled</span></span>
<span data-ttu-id="0768f-134">Indica se la conservazione delle informazioni di diagnostica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="0768f-134">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0768f-135">-RetentionInDays</span></span>
<span data-ttu-id="0768f-136">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="0768f-136">Specifies the retention policy, in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-137">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="0768f-137">-ServiceBusRuleId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0768f-138">-StorageAccountId</span></span>
<span data-ttu-id="0768f-139">Specifica l'ID dell'account di archiviazione in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="0768f-139">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-140">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="0768f-140">-Timegrains</span></span>
<span data-ttu-id="0768f-141">Specifica i grani temporali da abilitare o disabilitare per le metriche, in base al valore di *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="0768f-141">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="0768f-142">Se non specifichi una granulosità temporale, questo comando funziona in tutti i grani temporali disponibili.</span><span class="sxs-lookup"><span data-stu-id="0768f-142">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="0768f-143">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="0768f-143">-WorkspaceId</span></span>
<span data-ttu-id="0768f-144">ID dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0768f-144">The Id of the workspace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0768f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0768f-145">CommonParameters</span></span>
<span data-ttu-id="0768f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0768f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0768f-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0768f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0768f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0768f-148">INPUTS</span></span>

### <span data-ttu-id="0768f-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0768f-149">None</span></span>
<span data-ttu-id="0768f-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0768f-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0768f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0768f-151">OUTPUTS</span></span>

### <span data-ttu-id="0768f-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="0768f-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="0768f-153">Note</span><span class="sxs-lookup"><span data-stu-id="0768f-153">NOTES</span></span>

## <span data-ttu-id="0768f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0768f-154">RELATED LINKS</span></span>

[<span data-ttu-id="0768f-155">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0768f-155">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


