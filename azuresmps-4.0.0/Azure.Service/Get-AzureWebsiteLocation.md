---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029734"
---
# <span data-ttu-id="e105a-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="e105a-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="e105a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e105a-102">SYNOPSIS</span></span>
<span data-ttu-id="e105a-103">Ottiene tutte le posizioni disponibili per il sito Web.</span><span class="sxs-lookup"><span data-stu-id="e105a-103">Gets all available website locations.</span></span>

## <span data-ttu-id="e105a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e105a-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e105a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e105a-105">DESCRIPTION</span></span>
<span data-ttu-id="e105a-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e105a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e105a-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e105a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e105a-108">Ottiene tutti i percorsi del sito Web disponibili per l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e105a-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="e105a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e105a-109">EXAMPLES</span></span>

### <span data-ttu-id="e105a-110">Esempio 1: ottenere tutte le posizioni disponibili</span><span class="sxs-lookup"><span data-stu-id="e105a-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="e105a-111">Questo esempio consente di ottenere tutti i percorsi del sito Web disponibili per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e105a-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="e105a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e105a-112">PARAMETERS</span></span>

### <span data-ttu-id="e105a-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="e105a-113">-Profile</span></span>
<span data-ttu-id="e105a-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e105a-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e105a-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e105a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e105a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e105a-116">CommonParameters</span></span>
<span data-ttu-id="e105a-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e105a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e105a-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e105a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e105a-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e105a-119">INPUTS</span></span>

## <span data-ttu-id="e105a-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e105a-120">OUTPUTS</span></span>

## <span data-ttu-id="e105a-121">Note</span><span class="sxs-lookup"><span data-stu-id="e105a-121">NOTES</span></span>

## <span data-ttu-id="e105a-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e105a-122">RELATED LINKS</span></span>

[<span data-ttu-id="e105a-123">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e105a-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


