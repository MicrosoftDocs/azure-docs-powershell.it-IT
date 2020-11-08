---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7247CF85-78B0-4837-9162-F66077668A74
online version: ''
schema: 2.0.0
ms.openlocfilehash: d77dd294f386232f7db358696608aa47adceb1d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023860"
---
# <span data-ttu-id="69732-101">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="69732-101">New-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="69732-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69732-102">SYNOPSIS</span></span>
<span data-ttu-id="69732-103">Crea un processo di pianificazione con un'azione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-103">Creates a scheduler job that has a Storage action.</span></span>

## <span data-ttu-id="69732-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69732-104">SYNTAX</span></span>

### <span data-ttu-id="69732-105">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="69732-105">Required</span></span>
```
New-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -SASToken <String> [-StorageQueueMessage <String>]
 [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>]
 [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>]
 [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="69732-106">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="69732-106">Recurring</span></span>
```
New-AzureSchedulerStorageQueueJob [-StorageQueueMessage <String>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69732-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69732-107">DESCRIPTION</span></span>
<span data-ttu-id="69732-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69732-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69732-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="69732-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69732-110">Il cmdlet **New-AzureSchedulerStorageQueueJob** crea un processo di pianificazione con un'azione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="69732-110">The **New-AzureSchedulerStorageQueueJob** cmdlet creates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="69732-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69732-111">EXAMPLES</span></span>

### <span data-ttu-id="69732-112">Esempio 1: creare un processo di archiviazione eseguito una sola volta</span><span class="sxs-lookup"><span data-stu-id="69732-112">Example 1: Create a Storage job that runs once</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D"
```

<span data-ttu-id="69732-113">Questo comando crea un processo di archiviazione dello scheduler come parte della raccolta denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="69732-113">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="69732-114">Il comando specifica l'account di archiviazione, il nome della coda e il token SAS.</span><span class="sxs-lookup"><span data-stu-id="69732-114">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="69732-115">Il processo viene eseguito una volta, immediatamente.</span><span class="sxs-lookup"><span data-stu-id="69732-115">The job runs once, immediately.</span></span>

### <span data-ttu-id="69732-116">Esempio 2: creare un processo di archiviazione che esegua un numero specificato di volte</span><span class="sxs-lookup"><span data-stu-id="69732-116">Example 2: Create a Storage job that runs a specified number of times</span></span>
```
PS C:\> New-AzureSchedulerStorageQueueJob -JobCollectionName "JobCollection01" -JobName "Job12" -Location "North Central US"-StorageQueueAccount "ContosoStorageAccount" -StorageQueueName "ContosoStorageQueue" -SASToken "?sv=2012-02-12&si=samplePolicy%2F30%2F2014%206%3A37%3A36%20PM&sig=vLQEbSfZbTFh7q3YrzlxBeL%2BjiYKp0gE6lMJ0a5Nb4M%3D" -ExecutionCount 20 -Frequency "Hour" -Interval 2
```

<span data-ttu-id="69732-117">Questo comando crea un processo di archiviazione dello scheduler come parte della raccolta denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="69732-117">This command creates a scheduler Storage job as part of the collection named JobCollection01.</span></span>
<span data-ttu-id="69732-118">Il comando specifica l'account di archiviazione, il nome della coda e il token SAS.</span><span class="sxs-lookup"><span data-stu-id="69732-118">The command specifies the Storage account, queue name, and SAS token.</span></span>
<span data-ttu-id="69732-119">Il processo viene eseguito 20 volte in totale, due volte ogni ora.</span><span class="sxs-lookup"><span data-stu-id="69732-119">The job runs 20 times in total, twice every hour.</span></span>

## <span data-ttu-id="69732-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69732-120">PARAMETERS</span></span>

### <span data-ttu-id="69732-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="69732-121">-EndTime</span></span>
<span data-ttu-id="69732-122">Specifica un'ora, come oggetto **DateTime** , perché l'utilità di pianificazione smetta di avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="69732-122">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="69732-123">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="69732-123">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="69732-124">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="69732-124">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-125">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="69732-125">-ErrorActionHeaders</span></span>
<span data-ttu-id="69732-126">Specifica le intestazioni come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="69732-126">Specifies headers as a hash table.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-127">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="69732-127">-ErrorActionMethod</span></span>
<span data-ttu-id="69732-128">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="69732-128">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="69732-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="69732-129">Valid values are:</span></span> 

- <span data-ttu-id="69732-130">Ottieni</span><span class="sxs-lookup"><span data-stu-id="69732-130">GET</span></span>
- <span data-ttu-id="69732-131">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="69732-131">PUT</span></span>
- <span data-ttu-id="69732-132">Inserisci</span><span class="sxs-lookup"><span data-stu-id="69732-132">POST</span></span>
- <span data-ttu-id="69732-133">TESTA</span><span class="sxs-lookup"><span data-stu-id="69732-133">HEAD</span></span>
- <span data-ttu-id="69732-134">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="69732-134">DELETE</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-135">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="69732-135">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="69732-136">Specifica il corpo per le azioni processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-136">Specifies the body for Storage job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-137">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="69732-137">-ErrorActionRequestBody</span></span>
<span data-ttu-id="69732-138">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="69732-138">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-139">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="69732-139">-ErrorActionSASToken</span></span>
<span data-ttu-id="69732-140">Specifica il token SAS (Shared Access Signature) per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-140">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-141">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69732-141">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="69732-142">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-142">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-143">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="69732-143">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="69732-144">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-144">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-145">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="69732-145">-ErrorActionURI</span></span>
<span data-ttu-id="69732-146">Specifica l'URI per l'azione processo errore.</span><span class="sxs-lookup"><span data-stu-id="69732-146">Specifies the URI for the error job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-147">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="69732-147">-ExecutionCount</span></span>
<span data-ttu-id="69732-148">Specifica il numero di occorrenze di un processo che viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69732-148">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="69732-149">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="69732-149">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-150">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="69732-150">-Frequency</span></span>
<span data-ttu-id="69732-151">Specifica la frequenza massima per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="69732-151">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-152">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="69732-152">-Interval</span></span>
<span data-ttu-id="69732-153">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="69732-153">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-154">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="69732-154">-JobCollectionName</span></span>
<span data-ttu-id="69732-155">Specifica il nome della raccolta che contiene il processo dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="69732-155">Specifies the name of the collection to contain the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-156">-JobName</span><span class="sxs-lookup"><span data-stu-id="69732-156">-JobName</span></span>
<span data-ttu-id="69732-157">Specifica il nome per il processo dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="69732-157">Specifies the name for the scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-158">-JobState</span><span class="sxs-lookup"><span data-stu-id="69732-158">-JobState</span></span>
<span data-ttu-id="69732-159">Specifica lo stato per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="69732-159">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="69732-160">-Posizione</span><span class="sxs-lookup"><span data-stu-id="69732-160">-Location</span></span>
<span data-ttu-id="69732-161">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="69732-161">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="69732-162">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="69732-162">Valid values are:</span></span> 

- <span data-ttu-id="69732-163">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="69732-163">Anywhere Asia</span></span>
- <span data-ttu-id="69732-164">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="69732-164">Anywhere Europe</span></span>
- <span data-ttu-id="69732-165">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="69732-165">Anywhere US</span></span>
- <span data-ttu-id="69732-166">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="69732-166">East Asia</span></span>
- <span data-ttu-id="69732-167">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="69732-167">East US</span></span>
- <span data-ttu-id="69732-168">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="69732-168">North Central US</span></span>
- <span data-ttu-id="69732-169">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="69732-169">North Europe</span></span>
- <span data-ttu-id="69732-170">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="69732-170">South Central US</span></span>
- <span data-ttu-id="69732-171">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="69732-171">Southeast Asia</span></span>
- <span data-ttu-id="69732-172">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="69732-172">West Europe</span></span>
- <span data-ttu-id="69732-173">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="69732-173">West US</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-174">-Profile</span><span class="sxs-lookup"><span data-stu-id="69732-174">-Profile</span></span>
<span data-ttu-id="69732-175">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69732-175">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69732-176">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="69732-176">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-177">-SASToken</span><span class="sxs-lookup"><span data-stu-id="69732-177">-SASToken</span></span>
<span data-ttu-id="69732-178">Specifica il token SAS per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-178">Specifies the SAS token for the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-179">-StartTime</span><span class="sxs-lookup"><span data-stu-id="69732-179">-StartTime</span></span>
<span data-ttu-id="69732-180">Specifica un'ora, come oggetto **DateTime** , per l'avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="69732-180">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-181">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="69732-181">-StorageQueueAccount</span></span>
<span data-ttu-id="69732-182">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-182">Specifies the Storage account name.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-183">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="69732-183">-StorageQueueMessage</span></span>
<span data-ttu-id="69732-184">Specifica il messaggio di coda per il processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-184">Specifies the queue message for Storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69732-185">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="69732-185">-StorageQueueName</span></span>
<span data-ttu-id="69732-186">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69732-186">Specifies the name of the Storage queue.</span></span>

```yaml
Type: String
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69732-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69732-187">CommonParameters</span></span>
<span data-ttu-id="69732-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69732-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69732-189">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69732-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69732-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69732-190">INPUTS</span></span>

## <span data-ttu-id="69732-191">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69732-191">OUTPUTS</span></span>

## <span data-ttu-id="69732-192">Note</span><span class="sxs-lookup"><span data-stu-id="69732-192">NOTES</span></span>

## <span data-ttu-id="69732-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69732-193">RELATED LINKS</span></span>

[<span data-ttu-id="69732-194">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="69732-194">Set-AzureSchedulerStorageQueueJob</span></span>](./Set-AzureSchedulerStorageQueueJob.md)


