---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030050"
---
# <span data-ttu-id="61b47-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61b47-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="61b47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61b47-102">SYNOPSIS</span></span>
<span data-ttu-id="61b47-103">Interrompe il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="61b47-103">Stops the specified website.</span></span>

## <span data-ttu-id="61b47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61b47-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="61b47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61b47-105">DESCRIPTION</span></span>
<span data-ttu-id="61b47-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61b47-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="61b47-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="61b47-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="61b47-108">Il cmdlet **Stop-AzureWebsite** arresta il sito Web specificato ospitato in Azure.</span><span class="sxs-lookup"><span data-stu-id="61b47-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="61b47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61b47-109">EXAMPLES</span></span>

## <span data-ttu-id="61b47-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61b47-110">PARAMETERS</span></span>

### <span data-ttu-id="61b47-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="61b47-111">-Name</span></span>
<span data-ttu-id="61b47-112">Specifica il nome del sito Web da interrompere.</span><span class="sxs-lookup"><span data-stu-id="61b47-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="61b47-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61b47-113">-PassThru</span></span>
<span data-ttu-id="61b47-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="61b47-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="61b47-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="61b47-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="61b47-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="61b47-116">-Profile</span></span>
<span data-ttu-id="61b47-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61b47-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61b47-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="61b47-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61b47-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="61b47-119">-Slot</span></span>
<span data-ttu-id="61b47-120">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="61b47-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="61b47-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b47-121">CommonParameters</span></span>
<span data-ttu-id="61b47-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b47-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b47-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b47-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b47-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61b47-124">INPUTS</span></span>

## <span data-ttu-id="61b47-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61b47-125">OUTPUTS</span></span>

## <span data-ttu-id="61b47-126">Note</span><span class="sxs-lookup"><span data-stu-id="61b47-126">NOTES</span></span>

## <span data-ttu-id="61b47-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61b47-127">RELATED LINKS</span></span>

[<span data-ttu-id="61b47-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61b47-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="61b47-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="61b47-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


