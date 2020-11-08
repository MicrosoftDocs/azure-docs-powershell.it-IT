---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029836"
---
# <span data-ttu-id="b2558-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="b2558-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="b2558-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2558-102">SYNOPSIS</span></span>
<span data-ttu-id="b2558-103">Abilita il debug del sito Web.</span><span class="sxs-lookup"><span data-stu-id="b2558-103">Enables the website's debug.</span></span>

## <span data-ttu-id="b2558-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2558-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2558-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2558-105">DESCRIPTION</span></span>
<span data-ttu-id="b2558-106">Abilita la caratteristica di debug del sito Web in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b2558-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="b2558-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2558-107">EXAMPLES</span></span>

### <span data-ttu-id="b2558-108">Abilitare il debug di Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="b2558-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="b2558-109">Abilita il debug in VS 2013.</span><span class="sxs-lookup"><span data-stu-id="b2558-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="b2558-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2558-110">PARAMETERS</span></span>

### <span data-ttu-id="b2558-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2558-111">-Name</span></span>
<span data-ttu-id="b2558-112">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2558-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="b2558-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2558-113">-PassThru</span></span>
<span data-ttu-id="b2558-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b2558-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2558-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b2558-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2558-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="b2558-116">-Profile</span></span>
<span data-ttu-id="b2558-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2558-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2558-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b2558-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2558-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2558-119">-Slot</span></span>
<span data-ttu-id="b2558-120">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2558-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="b2558-121">-Versione</span><span class="sxs-lookup"><span data-stu-id="b2558-121">-Version</span></span>
<span data-ttu-id="b2558-122">Versione di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b2558-122">The Visual Studio version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2558-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2558-123">CommonParameters</span></span>
<span data-ttu-id="b2558-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2558-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2558-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2558-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2558-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2558-126">INPUTS</span></span>

## <span data-ttu-id="b2558-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2558-127">OUTPUTS</span></span>

## <span data-ttu-id="b2558-128">Note</span><span class="sxs-lookup"><span data-stu-id="b2558-128">NOTES</span></span>

## <span data-ttu-id="b2558-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2558-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2558-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="b2558-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="b2558-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b2558-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b2558-132">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b2558-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b2558-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b2558-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="b2558-134">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b2558-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


