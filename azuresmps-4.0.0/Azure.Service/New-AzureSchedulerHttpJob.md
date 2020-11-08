---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C608BBDD-DC2B-4BEF-812D-0BAE94FB4395
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f5332c18d2d47096f246485ac0d811548f70aa9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023862"
---
# <span data-ttu-id="bc0fc-101">New-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="bc0fc-101">New-AzureSchedulerHttpJob</span></span>

## <span data-ttu-id="bc0fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0fc-103">Crea un processo di pianificazione con un'azione HTTP.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-103">Creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="bc0fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-104">SYNTAX</span></span>

### <span data-ttu-id="bc0fc-105">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="bc0fc-105">Required</span></span>
```
New-AzureSchedulerHttpJob -Location <String> -JobCollectionName <String> -JobName <String> -Method <String>
 -URI <Uri> [-RequestBody <String>] [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-ExecutionCount <Int32>] [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionMethod <String>] [-ErrorActionURI <Uri>] [-ErrorActionRequestBody <String>]
 [-ErrorActionHeaders <Hashtable>] [-ErrorActionStorageAccount <String>] [-ErrorActionStorageQueue <String>]
 [-ErrorActionSASToken <String>] [-ErrorActionQueueMessageBody <String>] [-HttpAuthenticationType <String>]
 [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc0fc-106">PutPost</span><span class="sxs-lookup"><span data-stu-id="bc0fc-106">PutPost</span></span>
```
New-AzureSchedulerHttpJob [-RequestBody <String>] [-JobState <String>] [-Headers <Hashtable>]
 [-ErrorActionHeaders <Hashtable>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc0fc-107">Ricorrenti</span><span class="sxs-lookup"><span data-stu-id="bc0fc-107">Recurring</span></span>
```
New-AzureSchedulerHttpJob [-Interval <Int32>] [-Frequency <String>] [-ExecutionCount <Int32>]
 [-EndTime <DateTime>] [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc0fc-108">Autenticazione</span><span class="sxs-lookup"><span data-stu-id="bc0fc-108">Authentication</span></span>
```
New-AzureSchedulerHttpJob [-JobState <String>] [-Headers <Hashtable>] [-ErrorActionHeaders <Hashtable>]
 -HttpAuthenticationType <String> [-ClientCertificatePfx <Object>] [-ClientCertificatePassword <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc0fc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc0fc-109">DESCRIPTION</span></span>
<span data-ttu-id="bc0fc-110">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bc0fc-111">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bc0fc-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bc0fc-112">Il cmdlet **New-AzureSchedulerHttpJob** crea un processo di pianificazione con un'azione http.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-112">The **New-AzureSchedulerHttpJob** cmdlet creates a scheduler job that has an HTTP action.</span></span>

## <span data-ttu-id="bc0fc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-113">EXAMPLES</span></span>

### <span data-ttu-id="bc0fc-114">Esempio 1: creare un processo HTTP</span><span class="sxs-lookup"><span data-stu-id="bc0fc-114">Example 1: Create an HTTP job</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01" -JobName "Job01" -Location "North Central US" -Method "GET" -URI http://www.contoso.com
```

<span data-ttu-id="bc0fc-115">Questo comando crea un processo HTTP di pianificazione nella raccolta processi denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-115">This command creates a scheduler HTTP job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="bc0fc-116">Il comando specifica un URI e specifica GET come metodo.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-116">The command specifies a URI and specifies GET as the method.</span></span>

### <span data-ttu-id="bc0fc-117">Esempio 2: creare un processo HTTP per un conteggio eseguito specifico</span><span class="sxs-lookup"><span data-stu-id="bc0fc-117">Example 2: Create an HTTP job for a specific run count</span></span>
```
PS C:\> New-AzureSchedulerHttpJob -JobCollectionName "JobCollection01 -JobName "Job23" -Location "North Central US" -Method "GET" -URI http://www.contoso.com -ExecutionCount 20
```

<span data-ttu-id="bc0fc-118">Questo comando crea il processo http dello scheduler nella raccolta processi denominata JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-118">This command creates scheduler http job in the job collection named JobCollection01.</span></span>
<span data-ttu-id="bc0fc-119">Il comando specifica un URI e specifica GET come metodo.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-119">The command specifies a URI and specifies GET as the method.</span></span>
<span data-ttu-id="bc0fc-120">Questo comando causa l'esecuzione del processo 20 volte.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-120">This command causes the job to run 20 times.</span></span>

## <span data-ttu-id="bc0fc-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-121">PARAMETERS</span></span>

### <span data-ttu-id="bc0fc-122">-ClientCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="bc0fc-122">-ClientCertificatePassword</span></span>
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

### <span data-ttu-id="bc0fc-123">-ClientCertificatePfx</span><span class="sxs-lookup"><span data-stu-id="bc0fc-123">-ClientCertificatePfx</span></span>
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

### <span data-ttu-id="bc0fc-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bc0fc-124">-EndTime</span></span>
<span data-ttu-id="bc0fc-125">Specifica un'ora, come oggetto **DateTime** , per l'utilità di pianificazione per interrompere l'avvio dei processi.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-125">Specifies a time, as a **DateTime** object, for the scheduler to stop initiating jobs.</span></span>
<span data-ttu-id="bc0fc-126">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="bc0fc-126">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="bc0fc-127">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bc0fc-127">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="bc0fc-128">-ErrorActionHeaders</span><span class="sxs-lookup"><span data-stu-id="bc0fc-128">-ErrorActionHeaders</span></span>
<span data-ttu-id="bc0fc-129">Specifica le intestazioni come Hashtable.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-129">Specifies headers as a hashtable.</span></span>

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

### <span data-ttu-id="bc0fc-130">-ErrorActionMethod</span><span class="sxs-lookup"><span data-stu-id="bc0fc-130">-ErrorActionMethod</span></span>
<span data-ttu-id="bc0fc-131">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-131">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="bc0fc-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bc0fc-132">Valid values are:</span></span> 

- <span data-ttu-id="bc0fc-133">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bc0fc-133">GET</span></span>
- <span data-ttu-id="bc0fc-134">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="bc0fc-134">PUT</span></span>
- <span data-ttu-id="bc0fc-135">Inserisci</span><span class="sxs-lookup"><span data-stu-id="bc0fc-135">POST</span></span>
- <span data-ttu-id="bc0fc-136">TESTA</span><span class="sxs-lookup"><span data-stu-id="bc0fc-136">HEAD</span></span>
- <span data-ttu-id="bc0fc-137">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="bc0fc-137">DELETE</span></span>

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

### <span data-ttu-id="bc0fc-138">-ErrorActionQueueMessageBody</span><span class="sxs-lookup"><span data-stu-id="bc0fc-138">-ErrorActionQueueMessageBody</span></span>
<span data-ttu-id="bc0fc-139">Specifica il corpo per le azioni processo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-139">Specifies the body for storage job actions.</span></span>

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

### <span data-ttu-id="bc0fc-140">-ErrorActionRequestBody</span><span class="sxs-lookup"><span data-stu-id="bc0fc-140">-ErrorActionRequestBody</span></span>
<span data-ttu-id="bc0fc-141">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-141">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="bc0fc-142">-ErrorActionSASToken</span><span class="sxs-lookup"><span data-stu-id="bc0fc-142">-ErrorActionSASToken</span></span>
<span data-ttu-id="bc0fc-143">Specifica il token SAS (Shared Access Signature) per la coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-143">Specifies the Shared Access Signature (SAS) token for the storage queue.</span></span>

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

### <span data-ttu-id="bc0fc-144">-ErrorActionStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bc0fc-144">-ErrorActionStorageAccount</span></span>
<span data-ttu-id="bc0fc-145">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-145">Specifies the name of the storage account.</span></span>

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

### <span data-ttu-id="bc0fc-146">-ErrorActionStorageQueue</span><span class="sxs-lookup"><span data-stu-id="bc0fc-146">-ErrorActionStorageQueue</span></span>
<span data-ttu-id="bc0fc-147">Specifica il nome della coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-147">Specifies the name of the storage queue.</span></span>

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

### <span data-ttu-id="bc0fc-148">-ErrorActionURI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-148">-ErrorActionURI</span></span>
<span data-ttu-id="bc0fc-149">Specifica l'URI per l'azione processo errore.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-149">Specifies the URI for the error job action.</span></span>

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

### <span data-ttu-id="bc0fc-150">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="bc0fc-150">-ExecutionCount</span></span>
<span data-ttu-id="bc0fc-151">Specifica il numero di occorrenze di un processo che viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-151">Specifies the number occurrences of a job that run.</span></span>
<span data-ttu-id="bc0fc-152">Per impostazione predefinita, un processo si ripete a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-152">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="bc0fc-153">-Frequenza</span><span class="sxs-lookup"><span data-stu-id="bc0fc-153">-Frequency</span></span>
<span data-ttu-id="bc0fc-154">Specifica la frequenza massima per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-154">Specifies the maximum frequency for this scheduler job.</span></span>

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

### <span data-ttu-id="bc0fc-155">-Intestazioni</span><span class="sxs-lookup"><span data-stu-id="bc0fc-155">-Headers</span></span>
<span data-ttu-id="bc0fc-156">Specifica le intestazioni come Hashtable.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-156">Specifies the headers as a hashtable.</span></span>

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

### <span data-ttu-id="bc0fc-157">-HttpAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="bc0fc-157">-HttpAuthenticationType</span></span>
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

### <span data-ttu-id="bc0fc-158">-Intervallo</span><span class="sxs-lookup"><span data-stu-id="bc0fc-158">-Interval</span></span>
<span data-ttu-id="bc0fc-159">Specifica l'intervallo di ricorrenza alla frequenza specificata usando il parametro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="bc0fc-159">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="bc0fc-160">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="bc0fc-160">-JobCollectionName</span></span>
<span data-ttu-id="bc0fc-161">Specifica il nome della raccolta che contiene il processo dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-161">Specifies the name of the collection to contain the scheduler job.</span></span>

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

### <span data-ttu-id="bc0fc-162">-JobName</span><span class="sxs-lookup"><span data-stu-id="bc0fc-162">-JobName</span></span>
<span data-ttu-id="bc0fc-163">Specifica il nome per il processo dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-163">Specifies the name for the scheduler job.</span></span>

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

### <span data-ttu-id="bc0fc-164">-JobState</span><span class="sxs-lookup"><span data-stu-id="bc0fc-164">-JobState</span></span>
<span data-ttu-id="bc0fc-165">Specifica lo stato per il processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-165">Specifies the state for the scheduler job.</span></span>

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

### <span data-ttu-id="bc0fc-166">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bc0fc-166">-Location</span></span>
<span data-ttu-id="bc0fc-167">Specifica il nome della posizione che ospita il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-167">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="bc0fc-168">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bc0fc-168">Valid values are:</span></span> 

- <span data-ttu-id="bc0fc-169">Ovunque in Asia</span><span class="sxs-lookup"><span data-stu-id="bc0fc-169">Anywhere Asia</span></span>
- <span data-ttu-id="bc0fc-170">Ovunque Europa</span><span class="sxs-lookup"><span data-stu-id="bc0fc-170">Anywhere Europe</span></span>
- <span data-ttu-id="bc0fc-171">Ovunque negli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="bc0fc-171">Anywhere US</span></span>
- <span data-ttu-id="bc0fc-172">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="bc0fc-172">East Asia</span></span>
- <span data-ttu-id="bc0fc-173">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="bc0fc-173">East US</span></span>
- <span data-ttu-id="bc0fc-174">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="bc0fc-174">North Central US</span></span>
- <span data-ttu-id="bc0fc-175">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="bc0fc-175">North Europe</span></span>
- <span data-ttu-id="bc0fc-176">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="bc0fc-176">South Central US</span></span>
- <span data-ttu-id="bc0fc-177">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="bc0fc-177">Southeast Asia</span></span>
- <span data-ttu-id="bc0fc-178">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="bc0fc-178">West Europe</span></span>
- <span data-ttu-id="bc0fc-179">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="bc0fc-179">West US</span></span>

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

### <span data-ttu-id="bc0fc-180">-Method</span><span class="sxs-lookup"><span data-stu-id="bc0fc-180">-Method</span></span>
<span data-ttu-id="bc0fc-181">Specifica il metodo per i tipi di azione HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-181">Specifies the method for HTTP and HTTPS action types.</span></span>
<span data-ttu-id="bc0fc-182">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bc0fc-182">Valid values are:</span></span> 

- <span data-ttu-id="bc0fc-183">Ottieni</span><span class="sxs-lookup"><span data-stu-id="bc0fc-183">GET</span></span>
- <span data-ttu-id="bc0fc-184">INSERIRE</span><span class="sxs-lookup"><span data-stu-id="bc0fc-184">PUT</span></span>
- <span data-ttu-id="bc0fc-185">Inserisci</span><span class="sxs-lookup"><span data-stu-id="bc0fc-185">POST</span></span>
- <span data-ttu-id="bc0fc-186">TESTA</span><span class="sxs-lookup"><span data-stu-id="bc0fc-186">HEAD</span></span>
- <span data-ttu-id="bc0fc-187">ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="bc0fc-187">DELETE</span></span>

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

### <span data-ttu-id="bc0fc-188">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc0fc-188">-Profile</span></span>
<span data-ttu-id="bc0fc-189">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-189">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc0fc-190">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-190">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc0fc-191">-RequestBody</span><span class="sxs-lookup"><span data-stu-id="bc0fc-191">-RequestBody</span></span>
<span data-ttu-id="bc0fc-192">Specifica il corpo per le azioni di inserimento e POST-lavoro.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-192">Specifies the body for PUT and POST job actions.</span></span>

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

### <span data-ttu-id="bc0fc-193">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bc0fc-193">-StartTime</span></span>
<span data-ttu-id="bc0fc-194">Specifica un'ora, come oggetto **DateTime** , per l'avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-194">Specifies a time, as a **DateTime** object, for the job to start.</span></span>

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

### <span data-ttu-id="bc0fc-195">-URI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-195">-URI</span></span>
<span data-ttu-id="bc0fc-196">Specifica un URI per un'azione processo.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-196">Specifies a URI for a job action.</span></span>

```yaml
Type: Uri
Parameter Sets: Required
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc0fc-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0fc-197">CommonParameters</span></span>
<span data-ttu-id="bc0fc-198">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0fc-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0fc-199">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc0fc-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0fc-200">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-200">INPUTS</span></span>

## <span data-ttu-id="bc0fc-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc0fc-201">OUTPUTS</span></span>

## <span data-ttu-id="bc0fc-202">Note</span><span class="sxs-lookup"><span data-stu-id="bc0fc-202">NOTES</span></span>

## <span data-ttu-id="bc0fc-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc0fc-203">RELATED LINKS</span></span>

[<span data-ttu-id="bc0fc-204">Set-AzureSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="bc0fc-204">Set-AzureSchedulerHttpJob</span></span>](./Set-AzureSchedulerHttpJob.md)


