---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: b96c8717e20395c57e6c9d5d4520327d97dfa174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514296"
---
# <span data-ttu-id="e8862-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e8862-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="e8862-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8862-102">SYNOPSIS</span></span>
<span data-ttu-id="e8862-103">Ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="e8862-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8862-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8862-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8862-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8862-105">DESCRIPTION</span></span>
<span data-ttu-id="e8862-106">Il cmdlet **Get-AzureRmLogProfile** ottiene un profilo di log.</span><span class="sxs-lookup"><span data-stu-id="e8862-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="e8862-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8862-107">EXAMPLES</span></span>

## <span data-ttu-id="e8862-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8862-108">PARAMETERS</span></span>

### <span data-ttu-id="e8862-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8862-109">-DefaultProfile</span></span>
<span data-ttu-id="e8862-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8862-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8862-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8862-111">-Name</span></span>
<span data-ttu-id="e8862-112">Specifica il nome del profilo del log da ottenere.</span><span class="sxs-lookup"><span data-stu-id="e8862-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8862-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8862-113">CommonParameters</span></span>
<span data-ttu-id="e8862-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8862-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8862-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8862-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8862-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8862-116">INPUTS</span></span>

### <span data-ttu-id="e8862-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e8862-117">None</span></span>
<span data-ttu-id="e8862-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e8862-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8862-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8862-119">OUTPUTS</span></span>

### <span data-ttu-id="e8862-120">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="e8862-120">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="e8862-121">Note</span><span class="sxs-lookup"><span data-stu-id="e8862-121">NOTES</span></span>

## <span data-ttu-id="e8862-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8862-122">RELATED LINKS</span></span>

[<span data-ttu-id="e8862-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e8862-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="e8862-124">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e8862-124">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


