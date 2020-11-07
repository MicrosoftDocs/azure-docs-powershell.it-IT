---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687967"
---
# <span data-ttu-id="75a76-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="75a76-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="75a76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75a76-102">SYNOPSIS</span></span>
<span data-ttu-id="75a76-103">Crea un criterio di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="75a76-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75a76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75a76-104">SYNTAX</span></span>

### <span data-ttu-id="75a76-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75a76-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75a76-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="75a76-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a76-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75a76-107">DESCRIPTION</span></span>
<span data-ttu-id="75a76-108">Il cmdlet **New-AzureRmSiteRecoveryPolicy** crea un criterio di replica del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="75a76-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="75a76-109">Il criterio di replica viene usato per specificare le impostazioni di replica, ad esempio la frequenza di replica e il numero di punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="75a76-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="75a76-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75a76-110">EXAMPLES</span></span>

## <span data-ttu-id="75a76-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75a76-111">PARAMETERS</span></span>

### <span data-ttu-id="75a76-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="75a76-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="75a76-113">Specifica la frequenza dello snapshot coerente dell'applicazione in ore.</span><span class="sxs-lookup"><span data-stu-id="75a76-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-114">-Autenticazione</span><span class="sxs-lookup"><span data-stu-id="75a76-114">-Authentication</span></span>
<span data-ttu-id="75a76-115">Specifica il tipo di autenticazione usato.</span><span class="sxs-lookup"><span data-stu-id="75a76-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="75a76-116">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="75a76-116">Valid values are:</span></span>

- <span data-ttu-id="75a76-117">Certificato</span><span class="sxs-lookup"><span data-stu-id="75a76-117">Certificate</span></span>
-  <span data-ttu-id="75a76-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="75a76-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-119">-Compressione</span><span class="sxs-lookup"><span data-stu-id="75a76-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-120">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="75a76-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="75a76-121">-Name</span></span>
<span data-ttu-id="75a76-122">Specifica un nome descrittivo che identifica i criteri di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="75a76-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="75a76-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="75a76-124">Specifica l'ID dell'account di archiviazione di Azure della destinazione di replica.</span><span class="sxs-lookup"><span data-stu-id="75a76-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="75a76-125">-RecoveryPoints</span></span>
<span data-ttu-id="75a76-126">Specifica il numero di ore per mantenere i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="75a76-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="75a76-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="75a76-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="75a76-129">Specifica l'intervallo di frequenza della replica in secondi.</span><span class="sxs-lookup"><span data-stu-id="75a76-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="75a76-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="75a76-130">Valid values are:</span></span>

- <span data-ttu-id="75a76-131">30</span><span class="sxs-lookup"><span data-stu-id="75a76-131">30</span></span>
- <span data-ttu-id="75a76-132">300</span><span class="sxs-lookup"><span data-stu-id="75a76-132">300</span></span>
- <span data-ttu-id="75a76-133">900</span><span class="sxs-lookup"><span data-stu-id="75a76-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="75a76-134">-ReplicationMethod</span></span>
<span data-ttu-id="75a76-135">Specifica il metodo di replica.</span><span class="sxs-lookup"><span data-stu-id="75a76-135">Specifies the replication method.</span></span>
<span data-ttu-id="75a76-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="75a76-136">Valid values are:</span></span>

- <span data-ttu-id="75a76-137">Online</span><span class="sxs-lookup"><span data-stu-id="75a76-137">Online</span></span>
- <span data-ttu-id="75a76-138">Offline</span><span class="sxs-lookup"><span data-stu-id="75a76-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="75a76-139">-ReplicationPort</span></span>
<span data-ttu-id="75a76-140">Specifica la porta usata per la replica.</span><span class="sxs-lookup"><span data-stu-id="75a76-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="75a76-141">-ReplicationProvider</span></span>
<span data-ttu-id="75a76-142">Specifica il provider di replica.</span><span class="sxs-lookup"><span data-stu-id="75a76-142">Specifies the replication provider.</span></span>
<span data-ttu-id="75a76-143">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="75a76-143">Valid values are:</span></span>

- <span data-ttu-id="75a76-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="75a76-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="75a76-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="75a76-145">HyperVReplica2012</span></span>
- <span data-ttu-id="75a76-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="75a76-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="75a76-147">-ReplicationStartTime</span></span>
<span data-ttu-id="75a76-148">Specifica l'ora di inizio della replica.</span><span class="sxs-lookup"><span data-stu-id="75a76-148">Specifies the replication start time.</span></span>
<span data-ttu-id="75a76-149">Non deve essere più tardi di 24 ore dall'inizio del processo.</span><span class="sxs-lookup"><span data-stu-id="75a76-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a76-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a76-150">-DefaultProfile</span></span>
<span data-ttu-id="75a76-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75a76-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75a76-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a76-152">CommonParameters</span></span>
<span data-ttu-id="75a76-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a76-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a76-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a76-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a76-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75a76-155">INPUTS</span></span>

## <span data-ttu-id="75a76-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75a76-156">OUTPUTS</span></span>

## <span data-ttu-id="75a76-157">Note</span><span class="sxs-lookup"><span data-stu-id="75a76-157">NOTES</span></span>

## <span data-ttu-id="75a76-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75a76-158">RELATED LINKS</span></span>

[<span data-ttu-id="75a76-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="75a76-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="75a76-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="75a76-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
