---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200757"
---
# <span data-ttu-id="d64c8-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="d64c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d64c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d64c8-103">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="d64c8-103">Creates a new activity log profile.</span></span> <span data-ttu-id="d64c8-104">Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d64c8-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="d64c8-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d64c8-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d64c8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d64c8-106">DESCRIPTION</span></span>
<span data-ttu-id="d64c8-107">Il cmdlet **Add-AzLogProfile** crea un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="d64c8-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="d64c8-108">Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato.</span><span class="sxs-lookup"><span data-stu-id="d64c8-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="d64c8-109">Potrebbe essere di tipo ARM o Classic.</span><span class="sxs-lookup"><span data-stu-id="d64c8-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="d64c8-110">Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard.</span><span class="sxs-lookup"><span data-stu-id="d64c8-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="d64c8-111">Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d64c8-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="d64c8-112">**Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d64c8-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="d64c8-113">Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d64c8-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="d64c8-114">Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale".</span><span class="sxs-lookup"><span data-stu-id="d64c8-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="d64c8-115">Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="d64c8-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="d64c8-116">Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d64c8-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="d64c8-117">Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="d64c8-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="d64c8-118">**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.**</span><span class="sxs-lookup"><span data-stu-id="d64c8-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="d64c8-119">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d64c8-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d64c8-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d64c8-120">EXAMPLES</span></span>

### <span data-ttu-id="d64c8-121">Esempio 1: aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione di posizione a un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d64c8-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="d64c8-122">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d64c8-122">Example 2</span></span>

<span data-ttu-id="d64c8-123">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="d64c8-123">Creates a new activity log profile.</span></span> <span data-ttu-id="d64c8-124">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d64c8-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="d64c8-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d64c8-125">PARAMETERS</span></span>

### <span data-ttu-id="d64c8-126">-Categoria</span><span class="sxs-lookup"><span data-stu-id="d64c8-126">-Category</span></span>
<span data-ttu-id="d64c8-127">Specifica l'elenco di categorie.</span><span class="sxs-lookup"><span data-stu-id="d64c8-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="d64c8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-128">-DefaultProfile</span></span>
<span data-ttu-id="d64c8-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d64c8-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d64c8-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d64c8-130">-Location</span></span>
<span data-ttu-id="d64c8-131">Specifica la posizione del profilo del log.</span><span class="sxs-lookup"><span data-stu-id="d64c8-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="d64c8-132">Valori validi: Esegui sotto cmdlet per ottenere l'elenco più recente di posizioni.</span><span class="sxs-lookup"><span data-stu-id="d64c8-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="d64c8-133">Get-AzLocation | Selezionare DisplayName</span><span class="sxs-lookup"><span data-stu-id="d64c8-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="d64c8-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d64c8-134">-Name</span></span>
<span data-ttu-id="d64c8-135">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="d64c8-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="d64c8-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d64c8-136">-RetentionInDays</span></span>
<span data-ttu-id="d64c8-137">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="d64c8-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="d64c8-138">Questo è il numero di giorni in cui i registri vengono conservati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d64c8-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="d64c8-139">Per mantenere i dati impostati per sempre su **0**.</span><span class="sxs-lookup"><span data-stu-id="d64c8-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="d64c8-140">Se non viene specificato, il valore predefinito è **0**.</span><span class="sxs-lookup"><span data-stu-id="d64c8-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="d64c8-141">L'archiviazione standard normale o le tariffe di fatturazione dell'hub eventi verranno applicate per la conservazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="d64c8-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="d64c8-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="d64c8-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="d64c8-143">Specifica l'ID della regola Service Bus.</span><span class="sxs-lookup"><span data-stu-id="d64c8-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="d64c8-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d64c8-144">-StorageAccountId</span></span>
<span data-ttu-id="d64c8-145">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d64c8-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="d64c8-146">ID è l'ID di risorsa completo dell'account di archiviazione, ad esempio</span><span class="sxs-lookup"><span data-stu-id="d64c8-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="d64c8-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="d64c8-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="d64c8-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d64c8-148">-Confirm</span></span>
<span data-ttu-id="d64c8-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d64c8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d64c8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d64c8-150">-WhatIf</span></span>
<span data-ttu-id="d64c8-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d64c8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d64c8-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d64c8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d64c8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d64c8-153">CommonParameters</span></span>
<span data-ttu-id="d64c8-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d64c8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d64c8-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d64c8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d64c8-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d64c8-156">INPUTS</span></span>

### <span data-ttu-id="d64c8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d64c8-157">System.String</span></span>

### <span data-ttu-id="d64c8-158">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d64c8-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d64c8-159">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d64c8-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d64c8-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d64c8-160">OUTPUTS</span></span>

### <span data-ttu-id="d64c8-161">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="d64c8-162">Note</span><span class="sxs-lookup"><span data-stu-id="d64c8-162">NOTES</span></span>

## <span data-ttu-id="d64c8-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d64c8-163">RELATED LINKS</span></span>

[<span data-ttu-id="d64c8-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="d64c8-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="d64c8-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


