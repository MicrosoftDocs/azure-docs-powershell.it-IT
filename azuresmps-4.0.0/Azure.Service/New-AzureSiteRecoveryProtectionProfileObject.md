---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023849"
---
# <span data-ttu-id="0c1bd-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="0c1bd-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="0c1bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1bd-103">Crea un oggetto del profilo di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="0c1bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c1bd-104">SYNTAX</span></span>

### <span data-ttu-id="0c1bd-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c1bd-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c1bd-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0c1bd-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c1bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="0c1bd-108">Il cmdlet **New-AzureSiteRecoveryProtectionProfileObject** crea un oggetto profilo di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="0c1bd-109">Questo cmdlet crea un oggetto **ASRProtectionProfile** da usare con altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="0c1bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c1bd-110">EXAMPLES</span></span>

### <span data-ttu-id="0c1bd-111">Esempio 1: creare un profilo di protezione</span><span class="sxs-lookup"><span data-stu-id="0c1bd-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="0c1bd-112">Questo comando crea un oggetto profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="0c1bd-113">Esempio 2: creare un profilo di protezione per il provider di HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="0c1bd-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="0c1bd-114">Questo comando crea un profilo di protezione per un provider di HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="0c1bd-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c1bd-115">PARAMETERS</span></span>

### <span data-ttu-id="0c1bd-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="0c1bd-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="0c1bd-117">Indica che il profilo di protezione consente l'eliminazione delle entità di replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="0c1bd-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="0c1bd-119">Specifica la frequenza, in ore, per gli snapshot coerenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="0c1bd-120">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="0c1bd-120">-Authentication</span></span>
<span data-ttu-id="0c1bd-121">Specifica il tipo di autenticazione da usare.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="0c1bd-122">I valori accettabili per questo parametro sono: certificate e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="0c1bd-123">-CompressionEnabled</span></span>
<span data-ttu-id="0c1bd-124">Indica che il profilo di protezione consente la compressione.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0c1bd-125">-Force</span></span>
<span data-ttu-id="0c1bd-126">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c1bd-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c1bd-127">-Name</span></span>
<span data-ttu-id="0c1bd-128">Specifica un nome per il profilo di protezione.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="0c1bd-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="0c1bd-129">-Profile</span></span>
<span data-ttu-id="0c1bd-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c1bd-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c1bd-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0c1bd-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="0c1bd-133">Specifica il nome di un account di archiviazione di Azure in cui archiviare l'entità di replica di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0c1bd-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="0c1bd-135">Specifica l'ID di un abbonamento a Azure per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="0c1bd-136">Questo parametro fa riferimento all'account in cui archiviare l'entità di replica di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="0c1bd-137">-RecoveryPoints</span></span>
<span data-ttu-id="0c1bd-138">Specifica il numero di ore per mantenere i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="0c1bd-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="0c1bd-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="0c1bd-140">Specifica l'intervallo di frequenza, in secondi, per la replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="0c1bd-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1bd-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c1bd-142">30</span><span class="sxs-lookup"><span data-stu-id="0c1bd-142">30</span></span> 
- <span data-ttu-id="0c1bd-143">300</span><span class="sxs-lookup"><span data-stu-id="0c1bd-143">300</span></span> 
- <span data-ttu-id="0c1bd-144">900</span><span class="sxs-lookup"><span data-stu-id="0c1bd-144">900</span></span>

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

### <span data-ttu-id="0c1bd-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="0c1bd-145">-ReplicationMethod</span></span>
<span data-ttu-id="0c1bd-146">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-146">Specifies the replication method.</span></span> <span data-ttu-id="0c1bd-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c1bd-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c1bd-148">Online.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-148">Online.</span></span>
<span data-ttu-id="0c1bd-149">Replica tramite la rete.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-149">Replication over the network.</span></span>
- <span data-ttu-id="0c1bd-150">Offline.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1bd-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="0c1bd-151">-ReplicationPort</span></span>
<span data-ttu-id="0c1bd-152">Specifica il numero della porta in cui si trova la replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="0c1bd-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="0c1bd-153">-ReplicationProvider</span></span>
<span data-ttu-id="0c1bd-154">Specifica il tipo di provider di replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="0c1bd-155">I valori accettabili per questo parametro sono: HyperVReplica e HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="0c1bd-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="0c1bd-156">-ReplicationStartTime</span></span>
<span data-ttu-id="0c1bd-157">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="0c1bd-158">Specificare un'ora entro 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="0c1bd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1bd-159">CommonParameters</span></span>
<span data-ttu-id="0c1bd-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c1bd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1bd-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1bd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1bd-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c1bd-162">INPUTS</span></span>

## <span data-ttu-id="0c1bd-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c1bd-163">OUTPUTS</span></span>

## <span data-ttu-id="0c1bd-164">Note</span><span class="sxs-lookup"><span data-stu-id="0c1bd-164">NOTES</span></span>

## <span data-ttu-id="0c1bd-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c1bd-165">RELATED LINKS</span></span>

[<span data-ttu-id="0c1bd-166">Cmdlet di servizi di ripristino siti di Azure</span><span class="sxs-lookup"><span data-stu-id="0c1bd-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


