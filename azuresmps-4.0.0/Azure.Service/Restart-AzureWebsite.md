---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023428"
---
# <span data-ttu-id="49f47-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="49f47-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="49f47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49f47-102">SYNOPSIS</span></span>
<span data-ttu-id="49f47-103">Si arresta e quindi riavvia il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="49f47-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="49f47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49f47-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49f47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f47-105">DESCRIPTION</span></span>
<span data-ttu-id="49f47-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49f47-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="49f47-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="49f47-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="49f47-108">Il cmdlet **Restart-AzureWebsite** si arresta e quindi riavvia il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="49f47-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="49f47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49f47-109">EXAMPLES</span></span>

### <span data-ttu-id="49f47-110">Esempio 1: riavviare un sito Web</span><span class="sxs-lookup"><span data-stu-id="49f47-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="49f47-111">In questo esempio viene riavviato un sito Web denominato sito Web.</span><span class="sxs-lookup"><span data-stu-id="49f47-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="49f47-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49f47-112">PARAMETERS</span></span>

### <span data-ttu-id="49f47-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="49f47-113">-Name</span></span>
<span data-ttu-id="49f47-114">Specifica il nome del sito Web di Azure da riavviare.</span><span class="sxs-lookup"><span data-stu-id="49f47-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="49f47-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49f47-115">-PassThru</span></span>
<span data-ttu-id="49f47-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="49f47-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49f47-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="49f47-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49f47-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="49f47-118">-Profile</span></span>
<span data-ttu-id="49f47-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49f47-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49f47-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="49f47-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49f47-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="49f47-121">-Slot</span></span>
<span data-ttu-id="49f47-122">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="49f47-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="49f47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f47-123">CommonParameters</span></span>
<span data-ttu-id="49f47-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49f47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f47-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f47-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f47-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49f47-126">INPUTS</span></span>

## <span data-ttu-id="49f47-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49f47-127">OUTPUTS</span></span>

## <span data-ttu-id="49f47-128">Note</span><span class="sxs-lookup"><span data-stu-id="49f47-128">NOTES</span></span>

## <span data-ttu-id="49f47-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49f47-129">RELATED LINKS</span></span>

[<span data-ttu-id="49f47-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="49f47-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="49f47-131">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="49f47-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="49f47-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="49f47-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="49f47-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="49f47-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


