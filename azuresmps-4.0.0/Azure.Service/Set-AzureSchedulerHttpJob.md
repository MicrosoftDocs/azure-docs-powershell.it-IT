---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BBB1A0B7-2F5A-4799-8375-1D775C9D6E2F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 935d9ace51144cdd54cbcf3348ed9fc6b9b4ea02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023757"
---
# <span data-ttu-id="7710b-101">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7710b-101">Set-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="7710b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7710b-102">SYNOPSIS</span></span>
<span data-ttu-id="7710b-103">Aggiorna un processo di pianificazione con un'azione HTTP.</span><span class="sxs-lookup"><span data-stu-id="7710b-103">Updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="7710b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7710b-104">SYNTAX</span></span>

### <span data-ttu-id="7710b-105">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="7710b-105">Required</span></span>
```
Set-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> [-Method <String>]
 [-URI <Uri>] [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7710b-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="7710b-106">PutPost</span></span>
```
Set-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7710b-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="7710b-107">Recurring</span></span>
```
Set-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7710b-108">Autenticazione</span><span class="sxs-lookup"><span data-stu-id="7710b-108">Authentication</span></span>
```
Set-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7710b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7710b-109">DESCRIPTION</span></span>
<span data-ttu-id="7710b-110">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7710b-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7710b-111">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7710b-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7710b-112">Il cmdlet **set-AzureSchedulerHttpJob** aggiorna un processo di pianificazione con un'azione http.</span><span class="sxs-lookup"><span data-stu-id="7710b-112">The **Set-AzureSchedulerHttpJob** cmdlet updates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="7710b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7710b-113">EXAMPLES</span></span>

### <span data-ttu-id="7710b-114">Esempio 1: cambiare lo stato di un processo in disabilitato</span><span class="sxs-lookup"><span data-stu-id="7710b-114">Example 1: Change the state of a job to Disabled</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01" -JobState "Disabled"
```

<span data-ttu-id="7710b-115">Questo comando modifica lo stato del processo denominato Job01 su Disabled.</span><span class="sxs-lookup"><span data-stu-id="7710b-115">This command changes the state of the job named Job01 to Disabled.</span></span>
<span data-ttu-id="7710b-116">Questo processo fa parte della raccolta processi denominata JobColleciton01 per la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7710b-116">That job is part of the job collection named JobColleciton01 for the specified location.</span></span>

### <span data-ttu-id="7710b-117">Esempio 2: aggiornare l'URI di un processo</span><span class="sxs-lookup"><span data-stu-id="7710b-117">Example 2: Update the URI of a job</span></span>
```
PS C:\> Set-AzureSchedulerHttpJob -Location "North Central US" -JobCollectionName "JobCollection02" -JobName "Job37" -URI http://www.contoso.com
```

<span data-ttu-id="7710b-118">Questo comando Aggiorna l'URI del processo denominato Job01 http://www.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="7710b-118">This command updates the URI of the job named Job01 to be http://www.contoso.com.</span></span>

## <span data-ttu-id="7710b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7710b-119">PARAMETERS</span></span>

### <span data-ttu-id="7710b-120">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7710b-120">-ClientCertificatePassword</span></span>
```yaml
Type: String
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-121">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="7710b-121">-ClientCertificatePfx</span></span>
```yaml
Type: Object
Parameter Sets: Required, Authentication
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7710b-122">-EndTime</span></span>
<span data-ttu-id="7710b-123">Specifica un'ora, come oggetto **DateTime** , per l'utilità di pianificazione per interrompere l'avvio dei processi.</span><span class="sxs-lookup"><span data-stu-id="7710b-123">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="7710b-124">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="7710b-124">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7710b-125">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7710b-125">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-126">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="7710b-126">-ErrorActionHeaders</span></span>
<span data-ttu-id="7710b-127">Specifica le intestazioni come Hashtable.</span><span class="sxs-lookup"><span data-stu-id="7710b-127">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="7710b-128">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="7710b-128">-ErrorActionMethod</span></span>
<span data-ttu-id="7710b-129">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7710b-129">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="7710b-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7710b-130">Valid values are:</span></span> 

- <span data-ttu-id="7710b-131">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7710b-131">GET</span></span>
- <span data-ttu-id="7710b-132">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="7710b-132">PUT</span></span>
- <span data-ttu-id="7710b-133">Inserisci</span><span class="sxs-lookup"><span data-stu-id="7710b-133">POST</span></span>
- <span data-ttu-id="7710b-134">TESTA</span><span class="sxs-lookup"><span data-stu-id="7710b-134">HEAD</span></span>
- <span data-ttu-id="7710b-135">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="7710b-135">DELETE</span></span>

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

### <span data-ttu-id="7710b-136">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="7710b-136">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="7710b-137">Specifica il corpo per le azioni processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-137">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="7710b-138">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="7710b-138">-ErrorActionRequestBody</span></span>
<span data-ttu-id="7710b-139">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="7710b-139">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="7710b-140">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="7710b-140">-ErrorActionSASToken</span></span>
<span data-ttu-id="7710b-141">Specifica il token SAS (Shared Access Signature) per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-141">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="7710b-142">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7710b-142">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="7710b-143">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-143">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="7710b-144">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="7710b-144">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="7710b-145">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-145">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="7710b-146">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="7710b-146">-ErrorActionURI</span></span>
<span data-ttu-id="7710b-147">Specifica l'URI per l'azione processo errore.</span><span class="sxs-lookup"><span data-stu-id="7710b-147">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="7710b-148">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="7710b-148">-ExecutionCount</span></span>
<span data-ttu-id="7710b-149">Specifica il numero di occorrenze di un processo che viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7710b-149">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="7710b-150">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="7710b-150">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-151">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="7710b-151">-Frequency</span></span>
<span data-ttu-id="7710b-152">Specifica la frequenza massima per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-152">Specifies the maximum frequency for this scheduler job.</span></span>

```yaml
Type: String
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-153">-Intestazioni</span><span class="sxs-lookup"><span data-stu-id="7710b-153">-Headers</span></span>
<span data-ttu-id="7710b-154">Specifica le intestazioni come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="7710b-154">Specifies the headers as a hash table.</span></span>

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

### <span data-ttu-id="7710b-155">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="7710b-155">-HttpAuthenticationType</span></span>
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

```yaml
Type: String
Parameter Sets: Authentication
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-156">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="7710b-156">-Interval</span></span>
<span data-ttu-id="7710b-157">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="7710b-157">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: Required, Recurring
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-158">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="7710b-158">-JobCollectionName</span></span>
<span data-ttu-id="7710b-159">Specifica il nome della raccolta che contiene il processo di pianificazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="7710b-159">Specifies the name of the collection that contains the scheduler job to modify.</span></span>

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

### <span data-ttu-id="7710b-160">-JobName</span><span class="sxs-lookup"><span data-stu-id="7710b-160">-JobName</span></span>
<span data-ttu-id="7710b-161">Specifica il nome del processo di pianificazione da modificare.</span><span class="sxs-lookup"><span data-stu-id="7710b-161">Specifies the name of scheduler job to modify.</span></span>

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

### <span data-ttu-id="7710b-162">-JobState</span><span class="sxs-lookup"><span data-stu-id="7710b-162">-JobState</span></span>
<span data-ttu-id="7710b-163">Specifica lo stato per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7710b-163">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="7710b-164">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7710b-164">-Location</span></span>
<span data-ttu-id="7710b-165">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="7710b-165">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="7710b-166">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7710b-166">Valid values are:</span></span> 

- <span data-ttu-id="7710b-167">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="7710b-167">Anywhere Asia</span></span>
- <span data-ttu-id="7710b-168">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="7710b-168">Anywhere Europe</span></span>
- <span data-ttu-id="7710b-169">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="7710b-169">Anywhere US</span></span>
- <span data-ttu-id="7710b-170">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="7710b-170">East Asia</span></span>
- <span data-ttu-id="7710b-171">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="7710b-171">East US</span></span>
- <span data-ttu-id="7710b-172">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="7710b-172">North Central US</span></span>
- <span data-ttu-id="7710b-173">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="7710b-173">North Europe</span></span>
- <span data-ttu-id="7710b-174">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="7710b-174">South Central US</span></span>
- <span data-ttu-id="7710b-175">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="7710b-175">Southeast Asia</span></span>
- <span data-ttu-id="7710b-176">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="7710b-176">West Europe</span></span>
- <span data-ttu-id="7710b-177">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="7710b-177">West US</span></span>

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

### <span data-ttu-id="7710b-178">-Method</span><span class="sxs-lookup"><span data-stu-id="7710b-178">-Method</span></span>
<span data-ttu-id="7710b-179">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7710b-179">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="7710b-180">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7710b-180">Valid values are:</span></span> 

- <span data-ttu-id="7710b-181">Ottieni</span><span class="sxs-lookup"><span data-stu-id="7710b-181">GET</span></span>
- <span data-ttu-id="7710b-182">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="7710b-182">PUT</span></span>
- <span data-ttu-id="7710b-183">Inserisci</span><span class="sxs-lookup"><span data-stu-id="7710b-183">POST</span></span>
- <span data-ttu-id="7710b-184">TESTA</span><span class="sxs-lookup"><span data-stu-id="7710b-184">HEAD</span></span>
- <span data-ttu-id="7710b-185">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="7710b-185">DELETE</span></span>

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

### <span data-ttu-id="7710b-186">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7710b-186">-PassThru</span></span>
<span data-ttu-id="7710b-187">Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.</span><span class="sxs-lookup"><span data-stu-id="7710b-187">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="7710b-188">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7710b-188">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7710b-189">-Profile</span><span class="sxs-lookup"><span data-stu-id="7710b-189">-Profile</span></span>
<span data-ttu-id="7710b-190">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7710b-190">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7710b-191">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7710b-191">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7710b-192">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="7710b-192">-RequestBody</span></span>
<span data-ttu-id="7710b-193">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="7710b-193">Specifies the body for PUT and POST job actions.</span></span>

```yaml
Type: String
Parameter Sets: Required, PutPost
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7710b-194">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7710b-194">-StartTime</span></span>
<span data-ttu-id="7710b-195">Specifica un'ora, come oggetto **DateTime** , per l'avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="7710b-195">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="7710b-196">-URI</span><span class="sxs-lookup"><span data-stu-id="7710b-196">-URI</span></span>
<span data-ttu-id="7710b-197">Specifica un URI per un'azione processo.</span><span class="sxs-lookup"><span data-stu-id="7710b-197">Specifies a URI for a job action.</span></span>

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

### <span data-ttu-id="7710b-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7710b-198">CommonParameters</span></span>
<span data-ttu-id="7710b-199">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7710b-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7710b-200">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7710b-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7710b-201">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7710b-201">INPUTS</span></span>

## <span data-ttu-id="7710b-202">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7710b-202">OUTPUTS</span></span>

## <span data-ttu-id="7710b-203">Note</span><span class="sxs-lookup"><span data-stu-id="7710b-203">NOTES</span></span>

## <span data-ttu-id="7710b-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7710b-204">RELATED LINKS</span></span>

[<span data-ttu-id="7710b-205">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="7710b-205">New-AzureSchedulerHttpJob</span></span>](./New-AzureSchedulerHttpJob.md)


