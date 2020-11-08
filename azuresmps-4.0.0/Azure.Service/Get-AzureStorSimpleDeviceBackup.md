---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029752"
---
# <span data-ttu-id="bc615-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="bc615-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="bc615-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc615-102">SYNOPSIS</span></span>
<span data-ttu-id="bc615-103">Ottiene i backup da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc615-103">Gets backups from a device.</span></span>

## <span data-ttu-id="bc615-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc615-104">SYNTAX</span></span>

### <span data-ttu-id="bc615-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc615-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc615-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="bc615-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc615-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="bc615-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc615-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="bc615-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="bc615-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="bc615-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc615-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc615-110">DESCRIPTION</span></span>
<span data-ttu-id="bc615-111">Il cmdlet **Get-AzureStorSimpleDeviceBackup** ottiene i backup da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc615-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="bc615-112">È possibile specificare i criteri di backup, il volume e l'ora di creazione per i backup.</span><span class="sxs-lookup"><span data-stu-id="bc615-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="bc615-113">Questo cmdlet può restituire un massimo di backup di 100 nella prima pagina.</span><span class="sxs-lookup"><span data-stu-id="bc615-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="bc615-114">Se sono presenti più di 100 backup, recuperare le pagine successive usando i parametri *First* e *Skip* .</span><span class="sxs-lookup"><span data-stu-id="bc615-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="bc615-115">Se si specifica un valore di 100 per *Skip* e 50 per *First* , questo cmdlet non restituisce i primi 100 risultati.</span><span class="sxs-lookup"><span data-stu-id="bc615-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="bc615-116">Restituisce i risultati successivi di 50 dopo il 100 che viene saltato.</span><span class="sxs-lookup"><span data-stu-id="bc615-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="bc615-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc615-117">EXAMPLES</span></span>

### <span data-ttu-id="bc615-118">Esempio 1: ottenere tutti i backup in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="bc615-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="bc615-119">Questo comando consente di ottenere tutti i backup presenti nel dispositivo denominato Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="bc615-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="bc615-120">Se sono consentiti più di un massimo di backup di 100 per la prima pagina, usare i parametri *First* e *Skip* per visualizzare altri risultati.</span><span class="sxs-lookup"><span data-stu-id="bc615-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="bc615-121">Esempio 2: ottenere backup creati tra due date</span><span class="sxs-lookup"><span data-stu-id="bc615-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="bc615-122">Questo comando consente di ottenere backup nel dispositivo denominato Contoso63-AppVm creati in o dopo 10/7/2014 e prima o prima di 10/8/2014.</span><span class="sxs-lookup"><span data-stu-id="bc615-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="bc615-123">Questo cmdlet ignora il primo risultato e restituisce i primi due risultati successivi al primo risultato.</span><span class="sxs-lookup"><span data-stu-id="bc615-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="bc615-124">Modificare i valori per *First* e *Skip* per visualizzare altri risultati.</span><span class="sxs-lookup"><span data-stu-id="bc615-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="bc615-125">Esempio 3: ottenere backup per un ID criterio di backup</span><span class="sxs-lookup"><span data-stu-id="bc615-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="bc615-126">Questo comando consente di ottenere backup nel dispositivo denominato Contoso63-AppVm creato nella o prima della data specificata.</span><span class="sxs-lookup"><span data-stu-id="bc615-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="bc615-127">Il comando ottiene i backup creati usando i criteri di backup con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="bc615-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="bc615-128">Questo comando specifica il *primo* parametro, quindi restituisce solo i primi 10 risultati.</span><span class="sxs-lookup"><span data-stu-id="bc615-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="bc615-129">Esempio 4: ottenere backup per un oggetto Criteri di backup</span><span class="sxs-lookup"><span data-stu-id="bc615-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="bc615-130">Questo comando ottiene un oggetto **BackupPolicyDetails** usando il cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc615-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc615-131">Questo cmdlet ottiene i backup per il dispositivo denominato Contoso63-AppVm creato usando i criteri di backup della prima parte del comando.</span><span class="sxs-lookup"><span data-stu-id="bc615-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="bc615-132">Il comando ottiene i backup creati in precedenza o prima della data specificata, come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="bc615-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="bc615-133">Questo comando restituisce solo i primi 10 risultati.</span><span class="sxs-lookup"><span data-stu-id="bc615-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="bc615-134">Esempio 5: ottenere un backup per un ID volume</span><span class="sxs-lookup"><span data-stu-id="bc615-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="bc615-135">Questo comando ottiene un backup nel dispositivo creato nel volume con l'ID istanza specificato.</span><span class="sxs-lookup"><span data-stu-id="bc615-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="bc615-136">Questo comando specifica il *primo* parametro, quindi restituisce solo il primo risultato.</span><span class="sxs-lookup"><span data-stu-id="bc615-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="bc615-137">Esempio 6: ottenere un backup per un nome di volume</span><span class="sxs-lookup"><span data-stu-id="bc615-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="bc615-138">Questo comando ottiene un oggetto **VirtualDisk** usando il cmdlet **Get-AzureStorSimpleDeviceVolume** e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc615-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc615-139">Questo cmdlet ottiene i backup per il dispositivo denominato Contoso63-AppVm creato nel volume dalla prima parte del comando.</span><span class="sxs-lookup"><span data-stu-id="bc615-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="bc615-140">Questo comando restituisce solo il primo risultato.</span><span class="sxs-lookup"><span data-stu-id="bc615-140">This command returns only the first result.</span></span>

## <span data-ttu-id="bc615-141">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc615-141">PARAMETERS</span></span>

### <span data-ttu-id="bc615-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bc615-142">-BackupPolicy</span></span>
<span data-ttu-id="bc615-143">Specifica un oggetto **BackupPolicyDetails** .</span><span class="sxs-lookup"><span data-stu-id="bc615-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="bc615-144">Questo cmdlet usa la **InstanceID** di questo oggetto per determinare quali backup ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc615-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="bc615-145">Per ottenere un oggetto **BackupPolicyDetails** , usa il cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="bc615-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="bc615-146">-BackupPolicyId</span></span>
<span data-ttu-id="bc615-147">Specifica un ID istanza di un criterio di backup.</span><span class="sxs-lookup"><span data-stu-id="bc615-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="bc615-148">Questo cmdlet ottiene i backup del dispositivo per i criteri specificati da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bc615-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-149">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="bc615-149">-DeviceName</span></span>
<span data-ttu-id="bc615-150">Specifica il nome del dispositivo StorSimple per cui recuperare i backup.</span><span class="sxs-lookup"><span data-stu-id="bc615-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-151">-Primo</span><span class="sxs-lookup"><span data-stu-id="bc615-151">-First</span></span>
<span data-ttu-id="bc615-152">Ottiene solo il numero di oggetti specificato.</span><span class="sxs-lookup"><span data-stu-id="bc615-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="bc615-153">Immettere il numero di oggetti da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc615-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-154">-Da</span><span class="sxs-lookup"><span data-stu-id="bc615-154">-From</span></span>
<span data-ttu-id="bc615-155">Specifica la data e l'ora di inizio per i backup ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc615-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc615-156">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc615-156">-Profile</span></span>
<span data-ttu-id="bc615-157">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="bc615-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="bc615-158">-Skip</span><span class="sxs-lookup"><span data-stu-id="bc615-158">-Skip</span></span>
<span data-ttu-id="bc615-159">Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="bc615-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="bc615-160">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="bc615-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-161">-To</span><span class="sxs-lookup"><span data-stu-id="bc615-161">-To</span></span>
<span data-ttu-id="bc615-162">Specifica la data e l'ora di fine per i backup ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc615-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bc615-163">-Volume</span><span class="sxs-lookup"><span data-stu-id="bc615-163">-Volume</span></span>
<span data-ttu-id="bc615-164">Specifica un oggetto **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="bc615-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="bc615-165">Questo cmdlet usa la **InstanceID** di questo oggetto per determinare il volume in cui esistono i backup.</span><span class="sxs-lookup"><span data-stu-id="bc615-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="bc615-166">Per ottenere un oggetto **VirtualDisk** , usa il parametro **Get-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="bc615-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="bc615-167">-VolumeId</span></span>
<span data-ttu-id="bc615-168">Specifica l'ID istanza del volume in cui esistono i backup.</span><span class="sxs-lookup"><span data-stu-id="bc615-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc615-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc615-169">CommonParameters</span></span>
<span data-ttu-id="bc615-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc615-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc615-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc615-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc615-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc615-172">INPUTS</span></span>

### <span data-ttu-id="bc615-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="bc615-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="bc615-174">Questo cmdlet accetta oggetti **BackupPolicyDetails** e **VirtualDisk** .</span><span class="sxs-lookup"><span data-stu-id="bc615-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="bc615-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc615-175">OUTPUTS</span></span>

### <span data-ttu-id="bc615-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="bc615-176">IList\<Backup\></span></span>
<span data-ttu-id="bc615-177">Questo cmdlet restituisce un elenco di oggetti di **backup** .</span><span class="sxs-lookup"><span data-stu-id="bc615-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="bc615-178">Note</span><span class="sxs-lookup"><span data-stu-id="bc615-178">NOTES</span></span>

## <span data-ttu-id="bc615-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc615-179">RELATED LINKS</span></span>

[<span data-ttu-id="bc615-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="bc615-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="bc615-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bc615-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="bc615-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="bc615-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


