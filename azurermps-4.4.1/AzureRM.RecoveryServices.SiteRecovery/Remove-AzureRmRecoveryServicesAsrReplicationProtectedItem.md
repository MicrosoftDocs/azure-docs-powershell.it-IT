---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 17836b900e56fdfd5d90211c9bceb79fce87c66e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688251"
---
# <span data-ttu-id="4fee7-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fee7-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="4fee7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fee7-102">SYNOPSIS</span></span>
<span data-ttu-id="4fee7-103">Interrompe/Disabilita la replica per un elemento protetto della replica di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="4fee7-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fee7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fee7-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fee7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fee7-105">DESCRIPTION</span></span>
<span data-ttu-id="4fee7-106">Il cmdlet **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** Disabilita la replica dell'elemento protetto della replica di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="4fee7-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="4fee7-107">Questa operazione causa l'interruzione della replica per l'elemento protetto.</span><span class="sxs-lookup"><span data-stu-id="4fee7-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="4fee7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fee7-108">EXAMPLES</span></span>

### <span data-ttu-id="4fee7-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4fee7-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="4fee7-110">Avvia l'operazione di disabilitazione della replica per l'elemento protetto della replica specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4fee7-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4fee7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fee7-111">PARAMETERS</span></span>

### <span data-ttu-id="4fee7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4fee7-112">-Force</span></span>
<span data-ttu-id="4fee7-113">Forzare l'esecuzione del comando senza fornire un altro avviso.</span><span class="sxs-lookup"><span data-stu-id="4fee7-113">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="4fee7-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fee7-114">-InputObject</span></span>
<span data-ttu-id="4fee7-115">L'oggetto di input per il cmdlet: l'oggetto elemento protetto della replica ASR che corrisponde all'elemento protetto della replica per cui deve essere disabilitata la replica.</span><span class="sxs-lookup"><span data-stu-id="4fee7-115">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fee7-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4fee7-116">-WaitForCompletion</span></span>
<span data-ttu-id="4fee7-117">Indica che il cmdlet deve attendere il completamento dell'operazione prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="4fee7-117">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="4fee7-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4fee7-118">-Confirm</span></span>
<span data-ttu-id="4fee7-119">Specificare se è necessaria la conferma.</span><span class="sxs-lookup"><span data-stu-id="4fee7-119">Specify if confirmation is required.</span></span> <span data-ttu-id="4fee7-120">Impostare il valore del parametro Confirm su $false per ignorare la conferma.</span><span class="sxs-lookup"><span data-stu-id="4fee7-120">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="4fee7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fee7-121">-WhatIf</span></span>
<span data-ttu-id="4fee7-122">Mostra cosa succede se il cmdlet viene eseguito senza eseguire effettivamente il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fee7-122">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="4fee7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fee7-123">CommonParameters</span></span>
<span data-ttu-id="4fee7-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fee7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fee7-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fee7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fee7-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fee7-126">INPUTS</span></span>

### <span data-ttu-id="4fee7-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fee7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4fee7-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fee7-128">OUTPUTS</span></span>

### <span data-ttu-id="4fee7-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4fee7-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4fee7-130">Note</span><span class="sxs-lookup"><span data-stu-id="4fee7-130">NOTES</span></span>

## <span data-ttu-id="4fee7-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fee7-131">RELATED LINKS</span></span>

[<span data-ttu-id="4fee7-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fee7-132">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4fee7-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fee7-133">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4fee7-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fee7-134">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
