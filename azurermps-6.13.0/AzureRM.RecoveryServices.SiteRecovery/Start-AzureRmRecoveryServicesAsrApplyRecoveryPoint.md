---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 8a99625cc19eb9ac5f3d842b7c5c99979cdee69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509171"
---
# <span data-ttu-id="ea775-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea775-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="ea775-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea775-102">SYNOPSIS</span></span>
<span data-ttu-id="ea775-103">Cambia un punto di recupero per un elemento non superato protetto prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="ea775-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea775-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea775-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea775-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea775-105">DESCRIPTION</span></span>
<span data-ttu-id="ea775-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** modifica il punto di ripristino per un elemento non riuscito tramite protezione prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="ea775-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="ea775-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea775-107">EXAMPLES</span></span>

### <span data-ttu-id="ea775-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea775-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="ea775-109">Inizia ad applicare il punto di ripristino specificato all'elemento protetto da replica e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea775-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ea775-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea775-110">PARAMETERS</span></span>

### <span data-ttu-id="ea775-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ea775-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ea775-112">Specifica il file di certificato principale se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="ea775-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ea775-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ea775-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ea775-114">Specifica il file di certificato secondario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="ea775-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ea775-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea775-115">-DefaultProfile</span></span>
<span data-ttu-id="ea775-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea775-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ea775-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea775-117">-RecoveryPoint</span></span>
<span data-ttu-id="ea775-118">Specifica l'oggetto punto di ripristino che corrisponde al punto di recupero da applicare.</span><span class="sxs-lookup"><span data-stu-id="ea775-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea775-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ea775-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ea775-120">Specifica l'oggetto elemento protetto per la replica ASR.</span><span class="sxs-lookup"><span data-stu-id="ea775-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea775-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea775-121">-Confirm</span></span>
<span data-ttu-id="ea775-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea775-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea775-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea775-123">-WhatIf</span></span>
<span data-ttu-id="ea775-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea775-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea775-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea775-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea775-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea775-126">CommonParameters</span></span>
<span data-ttu-id="ea775-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea775-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea775-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea775-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea775-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea775-129">INPUTS</span></span>

### <span data-ttu-id="ea775-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ea775-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ea775-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea775-131">OUTPUTS</span></span>

### <span data-ttu-id="ea775-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea775-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea775-133">Note</span><span class="sxs-lookup"><span data-stu-id="ea775-133">NOTES</span></span>

## <span data-ttu-id="ea775-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea775-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea775-135">Cmdlet di ripristino del sito di Azure</span><span class="sxs-lookup"><span data-stu-id="ea775-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
