---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687988"
---
# <span data-ttu-id="a20c1-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a20c1-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="a20c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a20c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a20c1-103">Crea un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a20c1-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a20c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a20c1-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a20c1-105">DESCRIPTION</span></span>
<span data-ttu-id="a20c1-106">Il cmdlet **New-AzureRmRecoveryServicesAsrFabric** crea un tessuto di recupero del sito di Azure del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="a20c1-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="a20c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a20c1-107">EXAMPLES</span></span>

### <span data-ttu-id="a20c1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a20c1-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="a20c1-109">Avvia la creazione del tessuto con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="a20c1-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="a20c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a20c1-110">PARAMETERS</span></span>

### <span data-ttu-id="a20c1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="a20c1-111">-Name</span></span>
<span data-ttu-id="a20c1-112">Specifica il nome del tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a20c1-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="a20c1-113">-Digitare</span><span class="sxs-lookup"><span data-stu-id="a20c1-113">-Type</span></span>
<span data-ttu-id="a20c1-114">Specifica il tipo di tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a20c1-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a20c1-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a20c1-115">-Confirm</span></span>
<span data-ttu-id="a20c1-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a20c1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20c1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20c1-117">-WhatIf</span></span>
<span data-ttu-id="a20c1-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20c1-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a20c1-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a20c1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20c1-120">CommonParameters</span></span>
<span data-ttu-id="a20c1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20c1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20c1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20c1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a20c1-123">INPUTS</span></span>

### <span data-ttu-id="a20c1-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a20c1-124">None</span></span>

## <span data-ttu-id="a20c1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a20c1-125">OUTPUTS</span></span>

### <span data-ttu-id="a20c1-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a20c1-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a20c1-127">Note</span><span class="sxs-lookup"><span data-stu-id="a20c1-127">NOTES</span></span>

## <span data-ttu-id="a20c1-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a20c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="a20c1-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a20c1-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="a20c1-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="a20c1-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
