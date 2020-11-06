---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513084"
---
# <span data-ttu-id="a1f02-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1f02-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="a1f02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1f02-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f02-103">Crea un mapping del contenitore di protezione del ripristino di Azure site associando i criteri di replica specificati al contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f02-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1f02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1f02-104">SYNTAX</span></span>

### <span data-ttu-id="a1f02-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1f02-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1f02-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a1f02-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1f02-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f02-107">DESCRIPTION</span></span>
<span data-ttu-id="a1f02-108">Il cmdlet **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** crea un mapping del contenitore di protezione del ripristino di Azure site associando i criteri di replica specificati al contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="a1f02-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="a1f02-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1f02-109">EXAMPLES</span></span>

### <span data-ttu-id="a1f02-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1f02-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="a1f02-111">Avvia la creazione del mapping del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1f02-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a1f02-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1f02-112">PARAMETERS</span></span>

### <span data-ttu-id="a1f02-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1f02-113">-Name</span></span>
<span data-ttu-id="a1f02-114">Specifica il nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="a1f02-114">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="a1f02-115">-Policy</span><span class="sxs-lookup"><span data-stu-id="a1f02-115">-Policy</span></span>
<span data-ttu-id="a1f02-116">Specifica l'oggetto Criteri di replica ASR per il criterio di replica da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="a1f02-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1f02-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1f02-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="a1f02-118">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione principale da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="a1f02-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f02-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a1f02-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="a1f02-120">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione ripristino da usare nel mapping (usato se viene replicato in una posizione di ripristino che non è Azure).</span><span class="sxs-lookup"><span data-stu-id="a1f02-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1f02-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1f02-121">-Confirm</span></span>
<span data-ttu-id="a1f02-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1f02-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f02-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f02-123">-WhatIf</span></span>
<span data-ttu-id="a1f02-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1f02-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1f02-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1f02-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f02-126">CommonParameters</span></span>
<span data-ttu-id="a1f02-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f02-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1f02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f02-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1f02-129">INPUTS</span></span>

### <span data-ttu-id="a1f02-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a1f02-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a1f02-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1f02-131">OUTPUTS</span></span>

### <span data-ttu-id="a1f02-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a1f02-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a1f02-133">Note</span><span class="sxs-lookup"><span data-stu-id="a1f02-133">NOTES</span></span>

## <span data-ttu-id="a1f02-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1f02-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1f02-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1f02-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="a1f02-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a1f02-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
