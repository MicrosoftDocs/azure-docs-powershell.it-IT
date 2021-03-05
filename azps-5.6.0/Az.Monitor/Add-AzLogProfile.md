---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980318"
---
# <span data-ttu-id="985ef-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="985ef-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="985ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="985ef-102">SYNOPSIS</span></span>
<span data-ttu-id="985ef-103">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="985ef-103">Creates a new activity log profile.</span></span> <span data-ttu-id="985ef-104">Questo profilo viene usato per archiviare il log attività in un account di archiviazione di Azure o per trasmettere il log a un hub eventi di Azure nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="985ef-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="985ef-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="985ef-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="985ef-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="985ef-106">DESCRIPTION</span></span>
<span data-ttu-id="985ef-107">Il cmdlet **Add-AzLogProfile** crea un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="985ef-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="985ef-108">**Account di archiviazione:** è supportato solo l'account di archiviazione standard (l'account di archiviazione Premium non è supportato).</span><span class="sxs-lookup"><span data-stu-id="985ef-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="985ef-109">Può essere di tipo ARM o classico.</span><span class="sxs-lookup"><span data-stu-id="985ef-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="985ef-110">Se è registrato a un account di archiviazione, il costo di archiviazione del log attività viene fatturato a tariffe standard di archiviazione normali.</span><span class="sxs-lookup"><span data-stu-id="985ef-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="985ef-111">Per ogni abbonamento può essere usato un solo profilo di log per ogni abbonamento, consequenzialemente, per esportare il log attività.</span><span class="sxs-lookup"><span data-stu-id="985ef-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="985ef-112">**Hub eventi:** per esportare il log attività può essere usato un solo profilo di log per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="985ef-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="985ef-113">Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="985ef-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="985ef-114">Nel log attività gli eventi possono riguardare un'area geografica o "globale".</span><span class="sxs-lookup"><span data-stu-id="985ef-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="985ef-115">Globalmente, significa essenzialmente che questi eventi sono agnostici nella regione e sono indipendenti dall'area geografica, di fatto la maggior parte degli eventi rientrano in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="985ef-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="985ef-116">Se il profilo del log attività viene impostato dal portale, viene aggiunto in modo implicito "Globale" insieme a qualsiasi altra area geografica selezionata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="985ef-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="985ef-117">Quando si usa il cmdlet, la posizione "Globale" deve essere esplicitamente menzionata oltre a qualsiasi altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="985ef-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="985ef-118">**Nota:-** **Se non si imposta "Globale" nelle** posizioni, la maggior parte del log attività non viene esportata.</span><span class="sxs-lookup"><span data-stu-id="985ef-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="985ef-119">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="985ef-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="985ef-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="985ef-120">EXAMPLES</span></span>

### <span data-ttu-id="985ef-121">Esempio 1: Aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione della posizione a un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="985ef-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="985ef-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="985ef-122">Example 2</span></span>

<span data-ttu-id="985ef-123">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="985ef-123">Creates a new activity log profile.</span></span> <span data-ttu-id="985ef-124">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="985ef-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="985ef-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="985ef-125">PARAMETERS</span></span>

### <span data-ttu-id="985ef-126">-Category</span><span class="sxs-lookup"><span data-stu-id="985ef-126">-Category</span></span>
<span data-ttu-id="985ef-127">Specifica l'elenco delle categorie.</span><span class="sxs-lookup"><span data-stu-id="985ef-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="985ef-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="985ef-128">-DefaultProfile</span></span>
<span data-ttu-id="985ef-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="985ef-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="985ef-130">-Location</span><span class="sxs-lookup"><span data-stu-id="985ef-130">-Location</span></span>
<span data-ttu-id="985ef-131">Specifica la posizione del profilo di log.</span><span class="sxs-lookup"><span data-stu-id="985ef-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="985ef-132">Valori validi: eseguire il cmdlet seguente per ottenere l'elenco più recente di posizioni.</span><span class="sxs-lookup"><span data-stu-id="985ef-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="985ef-133">Get-AzLocation | Selezionare DisplayName</span><span class="sxs-lookup"><span data-stu-id="985ef-133">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="985ef-134">-Name</span><span class="sxs-lookup"><span data-stu-id="985ef-134">-Name</span></span>
<span data-ttu-id="985ef-135">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="985ef-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="985ef-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="985ef-136">-RetentionInDays</span></span>
<span data-ttu-id="985ef-137">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="985ef-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="985ef-138">Numero di giorni per cui i log vengono conservati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="985ef-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="985ef-139">Per conservare i dati per sempre, impostare questo valore su **0.**</span><span class="sxs-lookup"><span data-stu-id="985ef-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="985ef-140">Se non è specificato, viene utilizzato il valore predefinito **0.**</span><span class="sxs-lookup"><span data-stu-id="985ef-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="985ef-141">Per la conservazione dei dati verranno applicate tariffe normali per l'archiviazione standard o la fatturazione dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="985ef-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="985ef-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="985ef-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="985ef-143">Specifica l'ID della regola del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="985ef-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="985ef-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="985ef-144">-StorageAccountId</span></span>
<span data-ttu-id="985ef-145">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="985ef-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="985ef-146">ID è l'ID risorsa completo dell'account di archiviazione, ad esempio</span><span class="sxs-lookup"><span data-stu-id="985ef-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="985ef-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="985ef-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="985ef-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="985ef-148">-Confirm</span></span>
<span data-ttu-id="985ef-149">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="985ef-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="985ef-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="985ef-150">-WhatIf</span></span>
<span data-ttu-id="985ef-151">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="985ef-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="985ef-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="985ef-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="985ef-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="985ef-153">CommonParameters</span></span>
<span data-ttu-id="985ef-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="985ef-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="985ef-155">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="985ef-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="985ef-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="985ef-156">INPUTS</span></span>

### <span data-ttu-id="985ef-157">System.String</span><span class="sxs-lookup"><span data-stu-id="985ef-157">System.String</span></span>

### <span data-ttu-id="985ef-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="985ef-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="985ef-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="985ef-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="985ef-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="985ef-160">OUTPUTS</span></span>

### <span data-ttu-id="985ef-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="985ef-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="985ef-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="985ef-162">NOTES</span></span>

## <span data-ttu-id="985ef-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="985ef-163">RELATED LINKS</span></span>

[<span data-ttu-id="985ef-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="985ef-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="985ef-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="985ef-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


