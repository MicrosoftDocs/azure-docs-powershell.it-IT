---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685476"
---
# <span data-ttu-id="e6e74-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e6e74-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="e6e74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6e74-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e74-103">Crea un mapping di classificazione di archiviazione ASR nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6e74-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6e74-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6e74-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e74-106">Il cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** crea una classificazione di archiviazione che mappa il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e6e74-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="e6e74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6e74-107">EXAMPLES</span></span>

### <span data-ttu-id="e6e74-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6e74-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="e6e74-109">Avvia l'operazione di creazione del mapping della classificazione di archiviazione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e6e74-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e6e74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6e74-110">PARAMETERS</span></span>

### <span data-ttu-id="e6e74-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6e74-111">-Confirm</span></span>
<span data-ttu-id="e6e74-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e74-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e74-113">-DefaultProfile</span></span>
<span data-ttu-id="e6e74-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e6e74-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6e74-115">-Name</span></span>
<span data-ttu-id="e6e74-116">Specifica un nome per il mapping della classificazione di archiviazione ASR.</span><span class="sxs-lookup"><span data-stu-id="e6e74-116">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="e6e74-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e6e74-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="e6e74-118">Specifica l'oggetto di classificazione dello spazio di archiviazione ASR principale per il mapping.</span><span class="sxs-lookup"><span data-stu-id="e6e74-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6e74-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e6e74-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="e6e74-120">Specifica l'oggetto di classificazione dello spazio di ripristino ASR per il mapping.</span><span class="sxs-lookup"><span data-stu-id="e6e74-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e74-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e74-121">-WhatIf</span></span>
<span data-ttu-id="e6e74-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e74-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6e74-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6e74-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e74-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e74-124">CommonParameters</span></span>
<span data-ttu-id="e6e74-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e74-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e74-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e74-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e74-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6e74-127">INPUTS</span></span>

### <span data-ttu-id="e6e74-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e6e74-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e6e74-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6e74-129">OUTPUTS</span></span>

### <span data-ttu-id="e6e74-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6e74-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6e74-131">Note</span><span class="sxs-lookup"><span data-stu-id="e6e74-131">NOTES</span></span>

## <span data-ttu-id="e6e74-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6e74-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6e74-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e6e74-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="e6e74-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e6e74-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
