---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513091"
---
# <span data-ttu-id="247f5-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="247f5-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="247f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="247f5-102">SYNOPSIS</span></span>
<span data-ttu-id="247f5-103">Crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="247f5-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="247f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="247f5-104">SYNTAX</span></span>

### <span data-ttu-id="247f5-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="247f5-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="247f5-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="247f5-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="247f5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="247f5-107">DESCRIPTION</span></span>
<span data-ttu-id="247f5-108">Il cmdlet **New-AzureRmRecoveryServicesAsrPolicy** crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="247f5-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="247f5-109">Il criterio di replica viene usato per specificare le impostazioni di replica, ad esempio la frequenza di replica e il numero di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="247f5-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="247f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="247f5-110">EXAMPLES</span></span>

### <span data-ttu-id="247f5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="247f5-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="247f5-112">Avvia l'operazione di creazione dei criteri di replica usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="247f5-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="247f5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="247f5-113">PARAMETERS</span></span>

### <span data-ttu-id="247f5-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="247f5-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="247f5-115">Specifica la frequenza (in ore) in cui creare punti di ripristino coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="247f5-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="247f5-116">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="247f5-116">-Authentication</span></span>
<span data-ttu-id="247f5-117">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="247f5-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="247f5-118">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="247f5-118">Valid values are:</span></span>

- <span data-ttu-id="247f5-119">Certificato</span><span class="sxs-lookup"><span data-stu-id="247f5-119">Certificate</span></span>
-  <span data-ttu-id="247f5-120">Kerberos</span><span class="sxs-lookup"><span data-stu-id="247f5-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-121">-Compressione</span><span class="sxs-lookup"><span data-stu-id="247f5-121">-Compression</span></span>
<span data-ttu-id="247f5-122">Specifica se la compressione deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="247f5-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-123">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="247f5-123">-Encryption</span></span>
<span data-ttu-id="247f5-124">Specifica se la crittografia deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="247f5-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="247f5-125">-Name</span></span>
<span data-ttu-id="247f5-126">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="247f5-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="247f5-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="247f5-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="247f5-128">Specifica i punti di ripristino dei numeri da mantenere.</span><span class="sxs-lookup"><span data-stu-id="247f5-128">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="247f5-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="247f5-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="247f5-130">Specifica l'ID dell'account di archiviazione di Azure della destinazione di replica.</span><span class="sxs-lookup"><span data-stu-id="247f5-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="247f5-131">Usato come account di archiviazione di destinazione per la replica se non viene fornita un'alternativa durante l'abilitazione della replica tramite il cmdlet New-AzureRmRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="247f5-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="247f5-132">-ReplicaDeletion</span></span>
<span data-ttu-id="247f5-133">Specifica se la macchina virtuale della replica deve essere eliminata per disabilitare la replica da un sito gestito da VMM a un altro.</span><span class="sxs-lookup"><span data-stu-id="247f5-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="247f5-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="247f5-135">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="247f5-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="247f5-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="247f5-136">Valid values are:</span></span>

- <span data-ttu-id="247f5-137">30</span><span class="sxs-lookup"><span data-stu-id="247f5-137">30</span></span>
- <span data-ttu-id="247f5-138">300</span><span class="sxs-lookup"><span data-stu-id="247f5-138">300</span></span>
- <span data-ttu-id="247f5-139">900</span><span class="sxs-lookup"><span data-stu-id="247f5-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="247f5-140">-ReplicationMethod</span></span>
<span data-ttu-id="247f5-141">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="247f5-141">Specifies the replication method.</span></span>
<span data-ttu-id="247f5-142">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="247f5-142">Valid values are:</span></span>

- <span data-ttu-id="247f5-143">Online</span><span class="sxs-lookup"><span data-stu-id="247f5-143">Online</span></span>
- <span data-ttu-id="247f5-144">Offline</span><span class="sxs-lookup"><span data-stu-id="247f5-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="247f5-145">-ReplicationPort</span></span>
<span data-ttu-id="247f5-146">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="247f5-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="247f5-147">-ReplicationProvider</span></span>
<span data-ttu-id="247f5-148">Specifica il provider di replica.</span><span class="sxs-lookup"><span data-stu-id="247f5-148">Specifies the replication provider.</span></span>
<span data-ttu-id="247f5-149">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="247f5-149">Valid values are:</span></span>

- <span data-ttu-id="247f5-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="247f5-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="247f5-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="247f5-151">HyperVReplica2012</span></span>
- <span data-ttu-id="247f5-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="247f5-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="247f5-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="247f5-153">-ReplicationStartTime</span></span>
<span data-ttu-id="247f5-154">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="247f5-154">Specifies the replication start time.</span></span>
<span data-ttu-id="247f5-155">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="247f5-155">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="247f5-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="247f5-156">-Confirm</span></span>
<span data-ttu-id="247f5-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="247f5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247f5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247f5-158">-WhatIf</span></span>
<span data-ttu-id="247f5-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="247f5-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="247f5-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="247f5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247f5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247f5-161">CommonParameters</span></span>
<span data-ttu-id="247f5-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="247f5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247f5-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="247f5-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247f5-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="247f5-164">INPUTS</span></span>

### <span data-ttu-id="247f5-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="247f5-165">None</span></span>

## <span data-ttu-id="247f5-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="247f5-166">OUTPUTS</span></span>

### <span data-ttu-id="247f5-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="247f5-167">System.Object</span></span>

## <span data-ttu-id="247f5-168">Note</span><span class="sxs-lookup"><span data-stu-id="247f5-168">NOTES</span></span>

## <span data-ttu-id="247f5-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="247f5-169">RELATED LINKS</span></span>

[<span data-ttu-id="247f5-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="247f5-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="247f5-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="247f5-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
