---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507955"
---
# <span data-ttu-id="fe45d-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe45d-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="fe45d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe45d-102">SYNOPSIS</span></span>
<span data-ttu-id="fe45d-103">Rimuove un provider di servizi di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="fe45d-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe45d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe45d-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe45d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe45d-105">DESCRIPTION</span></span>
<span data-ttu-id="fe45d-106">Il cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** rimuove un provider di servizi di ripristino di Azure sito dal Vault.</span><span class="sxs-lookup"><span data-stu-id="fe45d-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="fe45d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe45d-107">EXAMPLES</span></span>

## <span data-ttu-id="fe45d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe45d-108">PARAMETERS</span></span>

### <span data-ttu-id="fe45d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe45d-109">-DefaultProfile</span></span>
<span data-ttu-id="fe45d-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe45d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe45d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fe45d-111">-Force</span></span>
<span data-ttu-id="fe45d-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="fe45d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe45d-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe45d-113">-ServicesProvider</span></span>
<span data-ttu-id="fe45d-114">Specifica l'oggetto provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="fe45d-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe45d-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe45d-115">-Confirm</span></span>
<span data-ttu-id="fe45d-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe45d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe45d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe45d-117">-WhatIf</span></span>
<span data-ttu-id="fe45d-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe45d-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fe45d-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe45d-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe45d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe45d-120">CommonParameters</span></span>
<span data-ttu-id="fe45d-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe45d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe45d-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe45d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe45d-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe45d-123">INPUTS</span></span>

### <span data-ttu-id="fe45d-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe45d-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="fe45d-125">Il parametro ' ServicesProvider ' accetta il valore di tipo ' ASRRecoveryServicesProvider ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe45d-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="fe45d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe45d-126">OUTPUTS</span></span>

### <span data-ttu-id="fe45d-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fe45d-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fe45d-128">Note</span><span class="sxs-lookup"><span data-stu-id="fe45d-128">NOTES</span></span>

## <span data-ttu-id="fe45d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe45d-129">RELATED LINKS</span></span>

[<span data-ttu-id="fe45d-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe45d-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="fe45d-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fe45d-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
