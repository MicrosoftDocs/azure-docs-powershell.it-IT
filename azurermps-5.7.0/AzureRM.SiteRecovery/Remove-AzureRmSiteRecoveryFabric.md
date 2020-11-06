---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520344"
---
# <span data-ttu-id="07587-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07587-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="07587-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07587-102">SYNOPSIS</span></span>
<span data-ttu-id="07587-103">Rimuove un tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="07587-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07587-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07587-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07587-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07587-105">DESCRIPTION</span></span>
<span data-ttu-id="07587-106">Il cmdlet **Remove-AzureRmSiteRecoveryFabric** rimuove un tessuto di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="07587-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="07587-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07587-107">EXAMPLES</span></span>

## <span data-ttu-id="07587-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07587-108">PARAMETERS</span></span>

### <span data-ttu-id="07587-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07587-109">-DefaultProfile</span></span>
<span data-ttu-id="07587-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07587-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07587-111">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="07587-111">-Fabric</span></span>
<span data-ttu-id="07587-112">Specifica l'oggetto tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="07587-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07587-113">-Force</span><span class="sxs-lookup"><span data-stu-id="07587-113">-Force</span></span>
<span data-ttu-id="07587-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="07587-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07587-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07587-115">-Confirm</span></span>
<span data-ttu-id="07587-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07587-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07587-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07587-117">-WhatIf</span></span>
<span data-ttu-id="07587-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07587-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="07587-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07587-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07587-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07587-120">CommonParameters</span></span>
<span data-ttu-id="07587-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07587-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07587-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07587-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07587-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07587-123">INPUTS</span></span>

### <span data-ttu-id="07587-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="07587-124">ASRFabric</span></span>
<span data-ttu-id="07587-125">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="07587-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="07587-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07587-126">OUTPUTS</span></span>

### <span data-ttu-id="07587-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="07587-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="07587-128">Note</span><span class="sxs-lookup"><span data-stu-id="07587-128">NOTES</span></span>

## <span data-ttu-id="07587-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07587-129">RELATED LINKS</span></span>

[<span data-ttu-id="07587-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07587-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="07587-131">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="07587-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
