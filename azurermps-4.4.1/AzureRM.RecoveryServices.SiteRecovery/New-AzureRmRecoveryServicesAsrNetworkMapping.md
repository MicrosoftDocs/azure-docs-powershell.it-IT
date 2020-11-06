---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520002"
---
# <span data-ttu-id="72e14-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="72e14-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="72e14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72e14-102">SYNOPSIS</span></span>
<span data-ttu-id="72e14-103">Crea un mapping di rete ASR tra due reti.</span><span class="sxs-lookup"><span data-stu-id="72e14-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72e14-104">SYNTAX</span></span>

### <span data-ttu-id="72e14-105">EnterpriseToEnterprise (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72e14-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e14-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="72e14-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72e14-107">DESCRIPTION</span></span>
<span data-ttu-id="72e14-108">Il cmdlet **New-AzureRmRecoveryServicesAsrNetworkMapping** avvia l'operazione di creazione di un mapping di rete ASR tra due reti e restituisce l'oggetto processo ASR per il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="72e14-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="72e14-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72e14-109">EXAMPLES</span></span>

### <span data-ttu-id="72e14-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72e14-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="72e14-111">Avvia l'operazione di creazione del mapping di rete con il nome specificato, le reti primarie e di ripristino e restituisce un processo ASR per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="72e14-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="72e14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72e14-112">PARAMETERS</span></span>

### <span data-ttu-id="72e14-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="72e14-113">-Name</span></span>
<span data-ttu-id="72e14-114">Nome del mapping di rete ASR da creare.</span><span class="sxs-lookup"><span data-stu-id="72e14-114">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="72e14-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="72e14-115">-PrimaryNetwork</span></span>
<span data-ttu-id="72e14-116">Specifica l'oggetto di rete principale per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="72e14-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72e14-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="72e14-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="72e14-118">Specifica l'ID di rete di Azure recupero per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="72e14-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="72e14-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="72e14-119">-RecoveryNetwork</span></span>
<span data-ttu-id="72e14-120">Specifica l'oggetto rete di ripristino per il mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="72e14-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e14-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72e14-121">-Confirm</span></span>
<span data-ttu-id="72e14-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72e14-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e14-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e14-123">-WhatIf</span></span>
<span data-ttu-id="72e14-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72e14-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72e14-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72e14-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e14-126">CommonParameters</span></span>
<span data-ttu-id="72e14-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e14-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e14-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e14-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72e14-129">INPUTS</span></span>

### <span data-ttu-id="72e14-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="72e14-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="72e14-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72e14-131">OUTPUTS</span></span>

### <span data-ttu-id="72e14-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="72e14-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="72e14-133">Note</span><span class="sxs-lookup"><span data-stu-id="72e14-133">NOTES</span></span>

## <span data-ttu-id="72e14-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72e14-134">RELATED LINKS</span></span>

[<span data-ttu-id="72e14-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="72e14-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="72e14-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="72e14-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
