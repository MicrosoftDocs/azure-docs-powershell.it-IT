---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519995"
---
# <span data-ttu-id="e230d-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e230d-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e230d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e230d-102">SYNOPSIS</span></span>
<span data-ttu-id="e230d-103">Aggiorna un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="e230d-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e230d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e230d-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e230d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e230d-105">DESCRIPTION</span></span>
<span data-ttu-id="e230d-106">Il cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aggiorna i criteri di replica del ripristino del sito di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="e230d-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="e230d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e230d-107">EXAMPLES</span></span>

### <span data-ttu-id="e230d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e230d-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="e230d-109">Avvia l'operazione di aggiornamento dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e230d-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e230d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e230d-110">PARAMETERS</span></span>

### <span data-ttu-id="e230d-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="e230d-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="e230d-112">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e230d-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="e230d-113">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="e230d-113">-Authentication</span></span>
<span data-ttu-id="e230d-114">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="e230d-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="e230d-115">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e230d-115">Valid values are:</span></span>

- <span data-ttu-id="e230d-116">Certificato</span><span class="sxs-lookup"><span data-stu-id="e230d-116">Certificate</span></span>
-  <span data-ttu-id="e230d-117">Kerberos</span><span class="sxs-lookup"><span data-stu-id="e230d-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-118">-Compressione</span><span class="sxs-lookup"><span data-stu-id="e230d-118">-Compression</span></span>
<span data-ttu-id="e230d-119">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="e230d-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-120">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="e230d-120">-Encryption</span></span>
<span data-ttu-id="e230d-121">Specifica se la crittografia deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e230d-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e230d-122">-InputObject</span></span>
<span data-ttu-id="e230d-123">Oggetto di input per il cmdlet: specifica l'oggetto Criteri di replica ASR che corrisponde ai criteri di replica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e230d-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="e230d-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="e230d-125">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="e230d-125">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e230d-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e230d-127">Specifica l'ID dell'account di archiviazione di Azure della destinazione di replica.</span><span class="sxs-lookup"><span data-stu-id="e230d-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="e230d-128">Usato come account di archiviazione di destinazione per la replica se non viene fornita un'alternativa durante l'abilitazione della replica tramite il cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="e230d-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

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

### <span data-ttu-id="e230d-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="e230d-129">-ReplicaDeletion</span></span>
<span data-ttu-id="e230d-130">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="e230d-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="e230d-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="e230d-132">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="e230d-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="e230d-133">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e230d-133">Valid values are:</span></span>

- <span data-ttu-id="e230d-134">30</span><span class="sxs-lookup"><span data-stu-id="e230d-134">30</span></span>
- <span data-ttu-id="e230d-135">300</span><span class="sxs-lookup"><span data-stu-id="e230d-135">300</span></span>
- <span data-ttu-id="e230d-136">900</span><span class="sxs-lookup"><span data-stu-id="e230d-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="e230d-137">-ReplicationMethod</span></span>
<span data-ttu-id="e230d-138">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="e230d-138">Specifies the replication method.</span></span>
<span data-ttu-id="e230d-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e230d-139">Valid values are:</span></span>

- <span data-ttu-id="e230d-140">Online</span><span class="sxs-lookup"><span data-stu-id="e230d-140">Online</span></span>
- <span data-ttu-id="e230d-141">Offline</span><span class="sxs-lookup"><span data-stu-id="e230d-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="e230d-142">-ReplicationPort</span></span>
<span data-ttu-id="e230d-143">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="e230d-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="e230d-144">-ReplicationStartTime</span></span>
<span data-ttu-id="e230d-145">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="e230d-145">Specifies the replication start time.</span></span>
<span data-ttu-id="e230d-146">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="e230d-146">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e230d-147">-Confirm</span></span>
<span data-ttu-id="e230d-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e230d-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e230d-149">-WhatIf</span></span>
<span data-ttu-id="e230d-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e230d-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e230d-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e230d-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e230d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e230d-152">CommonParameters</span></span>
<span data-ttu-id="e230d-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e230d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e230d-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e230d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e230d-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e230d-155">INPUTS</span></span>

### <span data-ttu-id="e230d-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e230d-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e230d-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e230d-157">OUTPUTS</span></span>

### <span data-ttu-id="e230d-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="e230d-158">System.Object</span></span>

## <span data-ttu-id="e230d-159">Note</span><span class="sxs-lookup"><span data-stu-id="e230d-159">NOTES</span></span>

## <span data-ttu-id="e230d-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e230d-160">RELATED LINKS</span></span>

