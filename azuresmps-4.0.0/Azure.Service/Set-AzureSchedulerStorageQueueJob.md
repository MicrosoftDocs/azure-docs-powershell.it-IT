---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8D53014E-B32D-4A37-8C49-E7BA6217A228
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b4f8fb409d0bde379c3d4b57cf5f19a73fbd4e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029512"
---
# <span data-ttu-id="7d32a-101">Set-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7d32a-101">Set-AzureSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="7d32a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d32a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d32a-103">Aggiorna un processo di pianificazione con un'azione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-103">Updates a scheduler job that has a storage action.</span></span>

## <span data-ttu-id="7d32a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d32a-104">SYNTAX</span></span>

### <span data-ttu-id="7d32a-105">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7d32a-105">Required</span></span>
```
Set-AzureSchedulerStorageQueueJob -Location <String> -JobCollectionName <String> -JobName <String>
 [-StorageQueueAccount <String>] [-StorageQueueName <String>] [-SASToken <String>]
 [-StorageQueueMessage <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionMethod <String>]
 [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>] [-ErrorActionHeaders <Hashtable>]
 [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>] [-ErrorActionSASToken <String>]
 [-ErrorActionQueueMessageBody <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d32a-106">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="7d32a-106">Recurring</span></span>
```
Set-AzureSchedulerStorageQueueJob [-Interval <Int32>] [-Frequency <String>] [-EndTime <DateTime>]
 [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionHeaders <Hashtable>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d32a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d32a-107">DESCRIPTION</span></span>
<span data-ttu-id="7d32a-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7d32a-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7d32a-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7d32a-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7d32a-110">Il cmdlet **set-AzureSchedulerStorageQueueJob** aggiorna un processo di pianificazione con un'azione di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7d32a-110">The **Set-AzureSchedulerStorageQueueJob** cmdlet updates a scheduler job that has an Azure Storage action.</span></span>

## <span data-ttu-id="7d32a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d32a-111">EXAMPLES</span></span>

### <span data-ttu-id="7d32a-112">Esempio 1: aggiornare un messaggio di coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7d32a-112">Example 1: Update a Storage queue message</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection01 -JobName "Job12" -StorageQueueMessage "Updated message"
```

<span data-ttu-id="7d32a-113">Questo comando Aggiorna il messaggio di coda per il processo di archiviazione denominato Job12.</span><span class="sxs-lookup"><span data-stu-id="7d32a-113">This command updates the queue message for the Storage job named Job12.</span></span>
<span data-ttu-id="7d32a-114">Il comando specifica il nome della raccolta processi e la posizione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-114">The command specifies the job collection name and the location.</span></span>

### <span data-ttu-id="7d32a-115">Esempio 2: abilitare un processo di Accodamento dello spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7d32a-115">Example 2: Enable a Storage queue job</span></span>
```
PS C:\> Set-AzureSchedulerStorageQueueJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job16" -JobState "Enabled"
```

<span data-ttu-id="7d32a-116">Questo comando consente di abilitare il processo denominato Job16.</span><span class="sxs-lookup"><span data-stu-id="7d32a-116">This command enables the job named Job16.</span></span>
<span data-ttu-id="7d32a-117">Il comando modifica lo stato del processo in Enabled specificando il valore per il parametro *JobState* .</span><span class="sxs-lookup"><span data-stu-id="7d32a-117">The command changes the state of the job to Enabled by specifying that value for the *JobState* parameter.</span></span>

## <span data-ttu-id="7d32a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d32a-118">PARAMETERS</span></span>

### <span data-ttu-id="7d32a-119">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7d32a-119">-EndTime</span></span>
<span data-ttu-id="7d32a-120">Specifica un'ora, come oggetto **DateTime** , perché l'utilità di pianificazione smetta di avviare il processo.</span><span class="sxs-lookup"><span data-stu-id="7d32a-120">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating the job.</span></span>
<span data-ttu-id="7d32a-121">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="7d32a-121">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7d32a-122">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7d32a-122">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="7d32a-123">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="7d32a-123">-ErrorActionHeaders</span></span>
<span data-ttu-id="7d32a-124">Specifica le intestazioni come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7d32a-124">Specifies headers as a hash table.</span></span>

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

### <span data-ttu-id="7d32a-125">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="7d32a-125">-ErrorActionMethod</span></span>
<span data-ttu-id="7d32a-126">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7d32a-126">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="7d32a-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7d32a-127">Valid values are:</span></span> 

- <span data-ttu-id="7d32a-128">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7d32a-128">GET</span></span>
- <span data-ttu-id="7d32a-129">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="7d32a-129">PUT</span></span>
- <span data-ttu-id="7d32a-130">Inserisci</span><span class="sxs-lookup"><span data-stu-id="7d32a-130">POST</span></span>
- <span data-ttu-id="7d32a-131">TESTA</span><span class="sxs-lookup"><span data-stu-id="7d32a-131">HEAD</span></span>
- <span data-ttu-id="7d32a-132">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="7d32a-132">DELETE</span></span>

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

### <span data-ttu-id="7d32a-133">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="7d32a-133">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="7d32a-134">Specifica il corpo per le azioni processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-134">Specifies the body for Storage job actions.</span></span>

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

### <span data-ttu-id="7d32a-135">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="7d32a-135">-ErrorActionRequestBody</span></span>
<span data-ttu-id="7d32a-136">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="7d32a-136">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="7d32a-137">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="7d32a-137">-ErrorActionSASToken</span></span>
<span data-ttu-id="7d32a-138">Specifica il token SAS (Shared Access Signature) per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-138">Specifies the Shared Access Signature (SAS) token for the Storage queue.</span></span>

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

### <span data-ttu-id="7d32a-139">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d32a-139">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="7d32a-140">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-140">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="7d32a-141">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7d32a-141">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="7d32a-142">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-142">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="7d32a-143">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="7d32a-143">-ErrorActionURI</span></span>
<span data-ttu-id="7d32a-144">Specifica l'URI per l'azione processo errore.</span><span class="sxs-lookup"><span data-stu-id="7d32a-144">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="7d32a-145">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="7d32a-145">-ExecutionCount</span></span>
<span data-ttu-id="7d32a-146">Specifica il numero di occorrenze di un processo che viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d32a-146">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="7d32a-147">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="7d32a-147">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="7d32a-148">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="7d32a-148">-Frequency</span></span>
<span data-ttu-id="7d32a-149">Specifica la frequenza massima per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-149">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="7d32a-150">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="7d32a-150">-Interval</span></span>
<span data-ttu-id="7d32a-151">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="7d32a-151">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="7d32a-152">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7d32a-152">-JobCollectionName</span></span>
<span data-ttu-id="7d32a-153">Specifica il nome della raccolta che contiene il processo dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-153">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="7d32a-154">-JobName</span><span class="sxs-lookup"><span data-stu-id="7d32a-154">-JobName</span></span>
<span data-ttu-id="7d32a-155">Specifica il nome del processo di pianificazione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7d32a-155">Specifies the name of the scheduler job to update.</span></span>

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

### <span data-ttu-id="7d32a-156">-JobState</span><span class="sxs-lookup"><span data-stu-id="7d32a-156">-JobState</span></span>
<span data-ttu-id="7d32a-157">Specifica lo stato per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-157">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="7d32a-158">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7d32a-158">-Location</span></span>
<span data-ttu-id="7d32a-159">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="7d32a-159">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="7d32a-160">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7d32a-160">Valid values are:</span></span> 

- <span data-ttu-id="7d32a-161">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="7d32a-161">Anywhere Asia</span></span>
- <span data-ttu-id="7d32a-162">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="7d32a-162">Anywhere Europe</span></span>
- <span data-ttu-id="7d32a-163">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="7d32a-163">Anywhere US</span></span>
- <span data-ttu-id="7d32a-164">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="7d32a-164">East Asia</span></span>
- <span data-ttu-id="7d32a-165">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="7d32a-165">East US</span></span>
- <span data-ttu-id="7d32a-166">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="7d32a-166">North Central US</span></span>
- <span data-ttu-id="7d32a-167">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="7d32a-167">North Europe</span></span>
- <span data-ttu-id="7d32a-168">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="7d32a-168">South Central US</span></span>
- <span data-ttu-id="7d32a-169">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="7d32a-169">Southeast Asia</span></span>
- <span data-ttu-id="7d32a-170">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="7d32a-170">West Europe</span></span>
- <span data-ttu-id="7d32a-171">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="7d32a-171">West US</span></span>

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

### <span data-ttu-id="7d32a-172">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d32a-172">-PassThru</span></span>
<span data-ttu-id="7d32a-173">Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.</span><span class="sxs-lookup"><span data-stu-id="7d32a-173">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="7d32a-174">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7d32a-174">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d32a-175">-Profile</span><span class="sxs-lookup"><span data-stu-id="7d32a-175">-Profile</span></span>
<span data-ttu-id="7d32a-176">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d32a-176">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d32a-177">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7d32a-177">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d32a-178">-SASToken</span><span class="sxs-lookup"><span data-stu-id="7d32a-178">-SASToken</span></span>
<span data-ttu-id="7d32a-179">Specifica il token SAS per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-179">Specifies the SAS token for the Storage queue.</span></span>

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

### <span data-ttu-id="7d32a-180">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7d32a-180">-StartTime</span></span>
<span data-ttu-id="7d32a-181">Specifica un'ora, come oggetto **DateTime** , per l'avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="7d32a-181">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="7d32a-182">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="7d32a-182">-StorageQueueAccount</span></span>
<span data-ttu-id="7d32a-183">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-183">Specifies the Storage account name.</span></span>

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

### <span data-ttu-id="7d32a-184">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="7d32a-184">-StorageQueueMessage</span></span>
<span data-ttu-id="7d32a-185">Specifica il messaggio della coda per il processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-185">Specifies the queue message for the Storage job.</span></span>

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

### <span data-ttu-id="7d32a-186">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="7d32a-186">-StorageQueueName</span></span>
<span data-ttu-id="7d32a-187">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7d32a-187">Specifies the name of the Storage queue.</span></span>

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

### <span data-ttu-id="7d32a-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d32a-188">CommonParameters</span></span>
<span data-ttu-id="7d32a-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d32a-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d32a-190">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d32a-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d32a-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d32a-191">INPUTS</span></span>

## <span data-ttu-id="7d32a-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d32a-192">OUTPUTS</span></span>

## <span data-ttu-id="7d32a-193">Note</span><span class="sxs-lookup"><span data-stu-id="7d32a-193">NOTES</span></span>

## <span data-ttu-id="7d32a-194">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d32a-194">RELATED LINKS</span></span>

[<span data-ttu-id="7d32a-195">New-AzureSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="7d32a-195">New-AzureSchedulerStorageQueueJob</span></span>](./New-AzureSchedulerStorageQueueJob.md)


