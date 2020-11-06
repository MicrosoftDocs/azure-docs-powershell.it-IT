---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520746"
---
# <span data-ttu-id="807a9-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="807a9-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="807a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="807a9-102">SYNOPSIS</span></span>
<span data-ttu-id="807a9-103">Avvia un failover di test per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="807a9-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="807a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="807a9-104">SYNTAX</span></span>

### <span data-ttu-id="807a9-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="807a9-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="807a9-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="807a9-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="807a9-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="807a9-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="807a9-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="807a9-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="807a9-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="807a9-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="807a9-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="807a9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="807a9-114">DESCRIPTION</span></span>
<span data-ttu-id="807a9-115">Il cmdlet **Start-AzureRmSiteRecoveryTestFailoverJob** avvia il failover dei test di un'entità o un piano di ripristino di un sito di Azure Protection.</span><span class="sxs-lookup"><span data-stu-id="807a9-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="807a9-116">Puoi verificare se il processo è riuscito usando il cmdlet Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="807a9-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="807a9-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="807a9-117">EXAMPLES</span></span>

## <span data-ttu-id="807a9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="807a9-118">PARAMETERS</span></span>

### <span data-ttu-id="807a9-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="807a9-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="807a9-120">Specifica l'ID rete virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="807a9-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="807a9-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="807a9-122">Specifica il file di certificato principale.</span><span class="sxs-lookup"><span data-stu-id="807a9-122">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="807a9-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="807a9-124">Specifica il file di certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="807a9-124">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-125">-Direzione</span><span class="sxs-lookup"><span data-stu-id="807a9-125">-Direction</span></span>
<span data-ttu-id="807a9-126">Specifica la direzione del failover.</span><span class="sxs-lookup"><span data-stu-id="807a9-126">Specifies the failover direction.</span></span>
<span data-ttu-id="807a9-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="807a9-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="807a9-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="807a9-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="807a9-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="807a9-129">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="807a9-130">-ProtectionEntity</span></span>
<span data-ttu-id="807a9-131">Specifica l'oggetto entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="807a9-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="807a9-132">-RecoveryPlan</span></span>
<span data-ttu-id="807a9-133">Specifica un oggetto piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="807a9-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="807a9-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="807a9-135">-VMNetwork</span></span>
<span data-ttu-id="807a9-136">Specifica la rete della macchina virtuale ripristino sito.</span><span class="sxs-lookup"><span data-stu-id="807a9-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807a9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807a9-137">-DefaultProfile</span></span>
<span data-ttu-id="807a9-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="807a9-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="807a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807a9-139">CommonParameters</span></span>
<span data-ttu-id="807a9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807a9-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="807a9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807a9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="807a9-142">INPUTS</span></span>

### <span data-ttu-id="807a9-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="807a9-143">ASRProtectionEntity</span></span>
<span data-ttu-id="807a9-144">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="807a9-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="807a9-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="807a9-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="807a9-146">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="807a9-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="807a9-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="807a9-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="807a9-148">Il parametro ' ReplicationProtectedItem ' accetta il valore di tipo ' ASRReplicationProtectedItem ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="807a9-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="807a9-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="807a9-149">OUTPUTS</span></span>

### <span data-ttu-id="807a9-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="807a9-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="807a9-151">Note</span><span class="sxs-lookup"><span data-stu-id="807a9-151">NOTES</span></span>

## <span data-ttu-id="807a9-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="807a9-152">RELATED LINKS</span></span>

[<span data-ttu-id="807a9-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="807a9-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
