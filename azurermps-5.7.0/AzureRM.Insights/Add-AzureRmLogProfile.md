---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521440"
---
# <span data-ttu-id="6a20b-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6a20b-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="6a20b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a20b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a20b-103">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="6a20b-103">Creates a new activity log profile.</span></span> <span data-ttu-id="6a20b-104">Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a20b-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a20b-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a20b-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a20b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a20b-106">DESCRIPTION</span></span>
<span data-ttu-id="6a20b-107">Il cmdlet **Add-AzureRmLogProfile** crea un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="6a20b-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="6a20b-108">Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato.</span><span class="sxs-lookup"><span data-stu-id="6a20b-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="6a20b-109">Potrebbe essere di tipo ARM o Classic.</span><span class="sxs-lookup"><span data-stu-id="6a20b-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="6a20b-110">Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard.</span><span class="sxs-lookup"><span data-stu-id="6a20b-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="6a20b-111">Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a20b-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="6a20b-112">**Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a20b-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="6a20b-113">Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="6a20b-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="6a20b-114">Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale".</span><span class="sxs-lookup"><span data-stu-id="6a20b-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="6a20b-115">Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="6a20b-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="6a20b-116">Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6a20b-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="6a20b-117">Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="6a20b-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="6a20b-118">**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.**</span><span class="sxs-lookup"><span data-stu-id="6a20b-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="6a20b-119">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a20b-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6a20b-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a20b-120">EXAMPLES</span></span>

### <span data-ttu-id="6a20b-121">Esempio 1: aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione di posizione a un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6a20b-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="6a20b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a20b-122">PARAMETERS</span></span>

### <span data-ttu-id="6a20b-123">-Categoria</span><span class="sxs-lookup"><span data-stu-id="6a20b-123">-Category</span></span>
<span data-ttu-id="6a20b-124">Specifica l'elenco di categorie.</span><span class="sxs-lookup"><span data-stu-id="6a20b-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a20b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a20b-125">-DefaultProfile</span></span>
<span data-ttu-id="6a20b-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6a20b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a20b-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6a20b-127">-Location</span></span>
<span data-ttu-id="6a20b-128">Specifica la posizione del profilo del log.</span><span class="sxs-lookup"><span data-stu-id="6a20b-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="6a20b-129">Valori validi: Esegui sotto cmdlet per ottenere l'elenco più recente di posizioni.</span><span class="sxs-lookup"><span data-stu-id="6a20b-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="6a20b-130">Get-AzureLocation | Selezionare DisplayName</span><span class="sxs-lookup"><span data-stu-id="6a20b-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a20b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a20b-131">-Name</span></span>
<span data-ttu-id="6a20b-132">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="6a20b-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="6a20b-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6a20b-133">-RetentionInDays</span></span>
<span data-ttu-id="6a20b-134">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="6a20b-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="6a20b-135">Questo è il numero di giorni in cui i registri vengono conservati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="6a20b-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="6a20b-136">Per mantenere i dati impostati per sempre su **0**.</span><span class="sxs-lookup"><span data-stu-id="6a20b-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="6a20b-137">Se non viene specificato, il valore predefinito è **0**.</span><span class="sxs-lookup"><span data-stu-id="6a20b-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="6a20b-138">L'archiviazione standard normale o le tariffe di fatturazione dell'hub eventi verranno applicate per la conservazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="6a20b-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="6a20b-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="6a20b-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="6a20b-140">Specifica l'ID della regola Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6a20b-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="6a20b-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6a20b-141">-StorageAccountId</span></span>
<span data-ttu-id="6a20b-142">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a20b-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="6a20b-143">ID è l'ID di risorsa completo dell'account di archiviazione, ad esempio</span><span class="sxs-lookup"><span data-stu-id="6a20b-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="6a20b-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="6a20b-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="6a20b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a20b-145">CommonParameters</span></span>
<span data-ttu-id="6a20b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a20b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a20b-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a20b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a20b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a20b-148">INPUTS</span></span>

### <span data-ttu-id="6a20b-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a20b-149">None</span></span>
<span data-ttu-id="6a20b-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6a20b-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a20b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a20b-151">OUTPUTS</span></span>

### <span data-ttu-id="6a20b-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="6a20b-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="6a20b-153">Note</span><span class="sxs-lookup"><span data-stu-id="6a20b-153">NOTES</span></span>

## <span data-ttu-id="6a20b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a20b-154">RELATED LINKS</span></span>

[<span data-ttu-id="6a20b-155">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6a20b-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="6a20b-156">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6a20b-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


