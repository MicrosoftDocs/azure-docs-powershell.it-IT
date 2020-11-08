---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023743"
---
# <span data-ttu-id="525c2-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="525c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="525c2-102">SYNOPSIS</span></span>
<span data-ttu-id="525c2-103">Apre un browser in un sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="525c2-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="525c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="525c2-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="525c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="525c2-105">DESCRIPTION</span></span>
<span data-ttu-id="525c2-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="525c2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="525c2-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="525c2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="525c2-108">Il cmdlet **show-AzureWebsite** apre un browser in un sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="525c2-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="525c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="525c2-109">EXAMPLES</span></span>

## <span data-ttu-id="525c2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="525c2-110">PARAMETERS</span></span>

### <span data-ttu-id="525c2-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="525c2-111">-Name</span></span>
<span data-ttu-id="525c2-112">Specifica il nome del sito da aprire nel browser.</span><span class="sxs-lookup"><span data-stu-id="525c2-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="525c2-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="525c2-113">-Profile</span></span>
<span data-ttu-id="525c2-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="525c2-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="525c2-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="525c2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="525c2-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="525c2-116">-Slot</span></span>
<span data-ttu-id="525c2-117">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="525c2-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="525c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525c2-118">CommonParameters</span></span>
<span data-ttu-id="525c2-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="525c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525c2-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="525c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525c2-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="525c2-121">INPUTS</span></span>

## <span data-ttu-id="525c2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="525c2-122">OUTPUTS</span></span>

## <span data-ttu-id="525c2-123">Note</span><span class="sxs-lookup"><span data-stu-id="525c2-123">NOTES</span></span>

## <span data-ttu-id="525c2-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="525c2-124">RELATED LINKS</span></span>

[<span data-ttu-id="525c2-125">Mostra-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="525c2-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="525c2-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="525c2-127">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="525c2-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="525c2-129">Riavviare-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="525c2-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="525c2-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


