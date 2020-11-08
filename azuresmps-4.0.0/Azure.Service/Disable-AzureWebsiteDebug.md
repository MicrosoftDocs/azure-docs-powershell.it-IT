---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023649"
---
# <span data-ttu-id="12054-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="12054-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="12054-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12054-102">SYNOPSIS</span></span>
<span data-ttu-id="12054-103">Disabilita il debug del sito Web.</span><span class="sxs-lookup"><span data-stu-id="12054-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="12054-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12054-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="12054-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12054-105">DESCRIPTION</span></span>
<span data-ttu-id="12054-106">Disabilita il debug del sito Web in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="12054-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="12054-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12054-107">EXAMPLES</span></span>

### <span data-ttu-id="12054-108">--------------Disabilitare il debug del sito Web--------------</span><span class="sxs-lookup"><span data-stu-id="12054-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="12054-109">Disabilita il debug del sito Web nel sito Web di website</span><span class="sxs-lookup"><span data-stu-id="12054-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="12054-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12054-110">PARAMETERS</span></span>

### <span data-ttu-id="12054-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="12054-111">-Name</span></span>
<span data-ttu-id="12054-112">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="12054-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="12054-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12054-113">-PassThru</span></span>
<span data-ttu-id="12054-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="12054-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12054-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="12054-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12054-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="12054-116">-Profile</span></span>
<span data-ttu-id="12054-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12054-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12054-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="12054-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12054-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="12054-119">-Slot</span></span>
<span data-ttu-id="12054-120">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="12054-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="12054-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12054-121">CommonParameters</span></span>
<span data-ttu-id="12054-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12054-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12054-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12054-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12054-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12054-124">INPUTS</span></span>

## <span data-ttu-id="12054-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12054-125">OUTPUTS</span></span>

## <span data-ttu-id="12054-126">Note</span><span class="sxs-lookup"><span data-stu-id="12054-126">NOTES</span></span>

## <span data-ttu-id="12054-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12054-127">RELATED LINKS</span></span>

[<span data-ttu-id="12054-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="12054-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="12054-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12054-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="12054-130">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12054-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="12054-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12054-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="12054-132">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12054-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


