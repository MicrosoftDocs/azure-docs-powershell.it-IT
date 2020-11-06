---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508047"
---
# <span data-ttu-id="0d404-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0d404-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="0d404-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d404-102">SYNOPSIS</span></span>
<span data-ttu-id="0d404-103">Cambia un punto di recupero per un elemento non superato protetto prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="0d404-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d404-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d404-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d404-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d404-105">DESCRIPTION</span></span>
<span data-ttu-id="0d404-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** modifica il punto di ripristino per un elemento non riuscito tramite protezione prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="0d404-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="0d404-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d404-107">EXAMPLES</span></span>

### <span data-ttu-id="0d404-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d404-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="0d404-109">Inizia ad applicare il punto di ripristino specificato all'elemento protetto da replica e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0d404-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0d404-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d404-110">PARAMETERS</span></span>

### <span data-ttu-id="0d404-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d404-111">-Confirm</span></span>
<span data-ttu-id="0d404-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d404-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d404-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0d404-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0d404-114">Specifica il file di certificato principale se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="0d404-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="0d404-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0d404-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0d404-116">Specifica il file di certificato secondario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="0d404-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="0d404-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d404-117">-DefaultProfile</span></span>
<span data-ttu-id="0d404-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d404-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d404-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0d404-119">-RecoveryPoint</span></span>
<span data-ttu-id="0d404-120">Specifica l'oggetto punto di ripristino che corrisponde al punto di recupero da applicare.</span><span class="sxs-lookup"><span data-stu-id="0d404-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d404-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d404-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0d404-122">Specifica l'oggetto elemento protetto per la replica ASR.</span><span class="sxs-lookup"><span data-stu-id="0d404-122">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d404-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d404-123">-WhatIf</span></span>
<span data-ttu-id="0d404-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d404-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d404-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d404-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d404-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d404-126">CommonParameters</span></span>
<span data-ttu-id="0d404-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d404-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d404-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d404-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d404-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d404-129">INPUTS</span></span>

### <span data-ttu-id="0d404-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d404-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0d404-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d404-131">OUTPUTS</span></span>

### <span data-ttu-id="0d404-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0d404-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0d404-133">Note</span><span class="sxs-lookup"><span data-stu-id="0d404-133">NOTES</span></span>

## <span data-ttu-id="0d404-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d404-134">RELATED LINKS</span></span>

[<span data-ttu-id="0d404-135">Cmdlet di ripristino del sito di Azure</span><span class="sxs-lookup"><span data-stu-id="0d404-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)