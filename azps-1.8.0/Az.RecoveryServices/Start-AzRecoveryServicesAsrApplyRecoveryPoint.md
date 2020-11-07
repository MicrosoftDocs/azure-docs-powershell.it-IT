---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 294af442998a49800f866ce1681365eae547ffd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677561"
---
# <span data-ttu-id="066f1-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="066f1-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="066f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="066f1-102">SYNOPSIS</span></span>
<span data-ttu-id="066f1-103">Cambia un punto di recupero per un elemento non superato protetto prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="066f1-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

## <span data-ttu-id="066f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="066f1-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="066f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="066f1-105">DESCRIPTION</span></span>
<span data-ttu-id="066f1-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** modifica il punto di ripristino per un elemento non riuscito tramite protezione prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="066f1-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="066f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="066f1-107">EXAMPLES</span></span>

### <span data-ttu-id="066f1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="066f1-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="066f1-109">Inizia ad applicare il punto di ripristino specificato all'elemento protetto da replica e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="066f1-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="066f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="066f1-110">PARAMETERS</span></span>

### <span data-ttu-id="066f1-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="066f1-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="066f1-112">Specifica il file di certificato principale se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="066f1-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="066f1-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="066f1-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="066f1-114">Specifica il file di certificato secondario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="066f1-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="066f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066f1-115">-DefaultProfile</span></span>
<span data-ttu-id="066f1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="066f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066f1-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="066f1-117">-RecoveryPoint</span></span>
<span data-ttu-id="066f1-118">Specifica l'oggetto punto di ripristino che corrisponde al punto di recupero da applicare.</span><span class="sxs-lookup"><span data-stu-id="066f1-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="066f1-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="066f1-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="066f1-120">Specifica l'oggetto elemento protetto per la replica ASR.</span><span class="sxs-lookup"><span data-stu-id="066f1-120">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="066f1-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="066f1-121">-Confirm</span></span>
<span data-ttu-id="066f1-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="066f1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066f1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066f1-123">-WhatIf</span></span>
<span data-ttu-id="066f1-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="066f1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="066f1-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="066f1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066f1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066f1-126">CommonParameters</span></span>
<span data-ttu-id="066f1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066f1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066f1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066f1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066f1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="066f1-129">INPUTS</span></span>

### <span data-ttu-id="066f1-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="066f1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="066f1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="066f1-131">OUTPUTS</span></span>

### <span data-ttu-id="066f1-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="066f1-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="066f1-133">Note</span><span class="sxs-lookup"><span data-stu-id="066f1-133">NOTES</span></span>

## <span data-ttu-id="066f1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="066f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="066f1-135">Cmdlet di ripristino del sito di Azure</span><span class="sxs-lookup"><span data-stu-id="066f1-135">Azure Site Recovery Cmdlets</span></span>](./Az.SiteRecovery.md)
