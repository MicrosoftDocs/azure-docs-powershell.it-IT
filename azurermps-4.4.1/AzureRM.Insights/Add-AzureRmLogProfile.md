---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521638"
---
# <span data-ttu-id="876a2-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="876a2-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="876a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="876a2-102">SYNOPSIS</span></span>
<span data-ttu-id="876a2-103">Crea un nuovo profilo del log attività.</span><span class="sxs-lookup"><span data-stu-id="876a2-103">Creates a new activity log profile.</span></span> <span data-ttu-id="876a2-104">Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="876a2-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="876a2-105">Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato.</span><span class="sxs-lookup"><span data-stu-id="876a2-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="876a2-106">Potrebbe essere di tipo ARM o Classic.</span><span class="sxs-lookup"><span data-stu-id="876a2-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="876a2-107">Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard.</span><span class="sxs-lookup"><span data-stu-id="876a2-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="876a2-108">Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento.</span><span class="sxs-lookup"><span data-stu-id="876a2-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="876a2-109">**Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento.</span><span class="sxs-lookup"><span data-stu-id="876a2-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="876a2-110">Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="876a2-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="876a2-111">Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale".</span><span class="sxs-lookup"><span data-stu-id="876a2-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="876a2-112">Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="876a2-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="876a2-113">Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="876a2-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="876a2-114">Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica.</span><span class="sxs-lookup"><span data-stu-id="876a2-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="876a2-115">**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.**</span><span class="sxs-lookup"><span data-stu-id="876a2-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="876a2-116">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="876a2-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="876a2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="876a2-117">DESCRIPTION</span></span>
<span data-ttu-id="876a2-118">Il cmdlet **Add-AzureRmLogProfile** crea un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="876a2-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="876a2-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="876a2-119">EXAMPLES</span></span>

### <span data-ttu-id="876a2-120">Esempio 1: aggiungere un nuovo profilo di log per esportare il log attività che corrisponde alla condizione di posizione a un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="876a2-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="876a2-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="876a2-121">PARAMETERS</span></span>

### <span data-ttu-id="876a2-122">-Categorie</span><span class="sxs-lookup"><span data-stu-id="876a2-122">-Categories</span></span>
<span data-ttu-id="876a2-123">Specifica l'elenco di categorie.</span><span class="sxs-lookup"><span data-stu-id="876a2-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="876a2-124">-Locations</span><span class="sxs-lookup"><span data-stu-id="876a2-124">-Locations</span></span>
<span data-ttu-id="876a2-125">Specifica la posizione del profilo del log.</span><span class="sxs-lookup"><span data-stu-id="876a2-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="876a2-126">Valori validi: Esegui sotto cmdlet per ottenere l'elenco più recente di posizioni.</span><span class="sxs-lookup"><span data-stu-id="876a2-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="876a2-127">Get-AzureLocation | Selezionare DisplayName</span><span class="sxs-lookup"><span data-stu-id="876a2-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="876a2-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="876a2-128">-Name</span></span>
<span data-ttu-id="876a2-129">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="876a2-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="876a2-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="876a2-130">-RetentionInDays</span></span>
<span data-ttu-id="876a2-131">Specifica i criteri di conservazione, in giorni.</span><span class="sxs-lookup"><span data-stu-id="876a2-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="876a2-132">Questo è il numero di giorni in cui i registri vengono conservati nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="876a2-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="876a2-133">Per mantenere i dati impostati per sempre su **0**.</span><span class="sxs-lookup"><span data-stu-id="876a2-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="876a2-134">Se non viene specificato, il valore predefinito è **0**.</span><span class="sxs-lookup"><span data-stu-id="876a2-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="876a2-135">L'archiviazione standard normale o le tariffe di fatturazione dell'hub eventi verranno applicate per la conservazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="876a2-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="876a2-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="876a2-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="876a2-137">Specifica l'ID della regola Service Bus.</span><span class="sxs-lookup"><span data-stu-id="876a2-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="876a2-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="876a2-138">-StorageAccountId</span></span>
<span data-ttu-id="876a2-139">Specifica l'ID dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="876a2-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="876a2-140">ID è l'ID di risorsa completo dell'account di archiviazione, ad esempio</span><span class="sxs-lookup"><span data-stu-id="876a2-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="876a2-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="876a2-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="876a2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876a2-142">-DefaultProfile</span></span>
<span data-ttu-id="876a2-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="876a2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876a2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876a2-144">CommonParameters</span></span>
<span data-ttu-id="876a2-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876a2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876a2-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876a2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876a2-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="876a2-147">INPUTS</span></span>

## <span data-ttu-id="876a2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="876a2-148">OUTPUTS</span></span>

### <span data-ttu-id="876a2-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="876a2-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="876a2-150">Note</span><span class="sxs-lookup"><span data-stu-id="876a2-150">NOTES</span></span>

## <span data-ttu-id="876a2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="876a2-151">RELATED LINKS</span></span>

[<span data-ttu-id="876a2-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="876a2-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="876a2-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="876a2-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


