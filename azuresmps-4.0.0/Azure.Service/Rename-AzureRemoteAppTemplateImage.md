---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023432"
---
# <span data-ttu-id="b6ea7-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6ea7-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="b6ea7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ea7-103">Rinomina un'immagine di modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b6ea7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6ea7-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6ea7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6ea7-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ea7-106">Il cmdlet **Rename-AzureRemoteAppTemplateImage Rinomina** un'immagine di modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="b6ea7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6ea7-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ea7-108">Esempio 1: rinominare un'immagine del modello</span><span class="sxs-lookup"><span data-stu-id="b6ea7-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="b6ea7-109">Questo comando Rinomina l'immagine del modello RemoteApp di Azure denominata ContosoApps in ContosoFinanceApps.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="b6ea7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6ea7-110">PARAMETERS</span></span>

### <span data-ttu-id="b6ea7-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b6ea7-111">-ImageName</span></span>
<span data-ttu-id="b6ea7-112">Specifica il nome di un'immagine di modello RemoteApp di Azure da rinominare.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ea7-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="b6ea7-113">-NewName</span></span>
<span data-ttu-id="b6ea7-114">Specifica un nuovo nome per un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ea7-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6ea7-115">-Profile</span></span>
<span data-ttu-id="b6ea7-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6ea7-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6ea7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ea7-118">CommonParameters</span></span>
<span data-ttu-id="b6ea7-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ea7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ea7-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ea7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ea7-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6ea7-121">INPUTS</span></span>

## <span data-ttu-id="b6ea7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6ea7-122">OUTPUTS</span></span>

## <span data-ttu-id="b6ea7-123">Note</span><span class="sxs-lookup"><span data-stu-id="b6ea7-123">NOTES</span></span>

## <span data-ttu-id="b6ea7-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6ea7-124">RELATED LINKS</span></span>

[<span data-ttu-id="b6ea7-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6ea7-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b6ea7-126">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6ea7-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="b6ea7-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="b6ea7-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


