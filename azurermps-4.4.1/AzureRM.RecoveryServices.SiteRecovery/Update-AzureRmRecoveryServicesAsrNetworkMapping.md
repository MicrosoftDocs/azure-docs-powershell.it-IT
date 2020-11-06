---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519996"
---
# <span data-ttu-id="58f5c-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="58f5c-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="58f5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="58f5c-103">Aggiorna il mapping di rete ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="58f5c-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58f5c-104">SYNTAX</span></span>

### <span data-ttu-id="58f5c-105">ByNetworkObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58f5c-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f5c-106">ById</span><span class="sxs-lookup"><span data-stu-id="58f5c-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f5c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f5c-107">DESCRIPTION</span></span>
<span data-ttu-id="58f5c-108">Il cmdlet **Update-AzureRmRecoveryServicesAsrNetworkMapping** aggiorna il mapping di rete di ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="58f5c-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="58f5c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58f5c-109">EXAMPLES</span></span>

### <span data-ttu-id="58f5c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58f5c-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="58f5c-111">Avvia l'operazione di mapping della rete di aggiornamento usando i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="58f5c-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="58f5c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58f5c-112">PARAMETERS</span></span>

### <span data-ttu-id="58f5c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58f5c-113">-InputObject</span></span>
<span data-ttu-id="58f5c-114">Oggetto di input: specifica l'oggetto mapping di rete ASR che corrisponde al mapping di rete ASR da aggiornare</span><span class="sxs-lookup"><span data-stu-id="58f5c-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58f5c-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="58f5c-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="58f5c-116">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="58f5c-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f5c-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="58f5c-117">-RecoveryNetwork</span></span>
<span data-ttu-id="58f5c-118">Specifica l'oggetto rete di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="58f5c-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f5c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58f5c-119">-Confirm</span></span>
<span data-ttu-id="58f5c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f5c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f5c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f5c-121">-WhatIf</span></span>
<span data-ttu-id="58f5c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f5c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58f5c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f5c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f5c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f5c-124">CommonParameters</span></span>
<span data-ttu-id="58f5c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f5c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f5c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f5c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f5c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58f5c-127">INPUTS</span></span>

### <span data-ttu-id="58f5c-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58f5c-128">None</span></span>

## <span data-ttu-id="58f5c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58f5c-129">OUTPUTS</span></span>

### <span data-ttu-id="58f5c-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="58f5c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="58f5c-131">Note</span><span class="sxs-lookup"><span data-stu-id="58f5c-131">NOTES</span></span>

## <span data-ttu-id="58f5c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58f5c-132">RELATED LINKS</span></span>

