---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 03bd15f1071ac223ba7460c27bcfd9ce96a55dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515988"
---
# <span data-ttu-id="81f77-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81f77-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="81f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81f77-102">SYNOPSIS</span></span>
<span data-ttu-id="81f77-103">Rimuove un mapping di rete dall'archivio corrente del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="81f77-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81f77-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81f77-105">DESCRIPTION</span></span>
<span data-ttu-id="81f77-106">Il cmdlet **Remove-AzureRMSiteRecoveryNetworkMapping** rimuove un mapping di rete dall'archivio di ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="81f77-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="81f77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81f77-107">EXAMPLES</span></span>

## <span data-ttu-id="81f77-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81f77-108">PARAMETERS</span></span>

### <span data-ttu-id="81f77-109">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81f77-109">-NetworkMapping</span></span>
<span data-ttu-id="81f77-110">Specifica l'oggetto mapping di rete.</span><span class="sxs-lookup"><span data-stu-id="81f77-110">Specifies the network mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81f77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f77-111">-DefaultProfile</span></span>
<span data-ttu-id="81f77-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81f77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81f77-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f77-113">CommonParameters</span></span>
<span data-ttu-id="81f77-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f77-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f77-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f77-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f77-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81f77-116">INPUTS</span></span>

### <span data-ttu-id="81f77-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81f77-117">ASRNetworkMapping</span></span>
<span data-ttu-id="81f77-118">Il parametro ' NetworkMapping ' accetta il valore di tipo ' ASRNetworkMapping ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="81f77-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="81f77-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81f77-119">OUTPUTS</span></span>

### <span data-ttu-id="81f77-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="81f77-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="81f77-121">Note</span><span class="sxs-lookup"><span data-stu-id="81f77-121">NOTES</span></span>

## <span data-ttu-id="81f77-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81f77-122">RELATED LINKS</span></span>

[<span data-ttu-id="81f77-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81f77-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="81f77-124">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="81f77-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
