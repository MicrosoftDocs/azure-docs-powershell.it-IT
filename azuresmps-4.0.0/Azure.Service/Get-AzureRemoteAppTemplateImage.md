---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030041"
---
# <span data-ttu-id="d1b3c-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="d1b3c-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="d1b3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b3c-103">Recupera informazioni sulle immagini di modelli RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="d1b3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1b3c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d1b3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b3c-106">Il cmdlet **Get-AzureRemoteAppTemplateImage** recupera informazioni sulle immagini di modelli RemoteApp di Azure in Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="d1b3c-107">Questo cmdlet restituisce un oggetto che contiene informazioni su un'immagine del modello specificata.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="d1b3c-108">Se non viene specificata un'immagine del modello, vengono recuperate le informazioni relative a tutte le immagini del modello nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="d1b3c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1b3c-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b3c-110">Esempio 1: ottenere un elenco di tutte le immagini dei modelli</span><span class="sxs-lookup"><span data-stu-id="d1b3c-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="d1b3c-111">Questo comando restituisce l'elenco di tutte le immagini modello.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="d1b3c-112">Esempio 2: recuperare informazioni su un'immagine del modello specificata</span><span class="sxs-lookup"><span data-stu-id="d1b3c-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="d1b3c-113">Questo comando recupera le informazioni sull'immagine del modello denominata ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="d1b3c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1b3c-114">PARAMETERS</span></span>

### <span data-ttu-id="d1b3c-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d1b3c-115">-ImageName</span></span>
<span data-ttu-id="d1b3c-116">Specifica il nome di un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="d1b3c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="d1b3c-117">-Profile</span></span>
<span data-ttu-id="d1b3c-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1b3c-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1b3c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b3c-120">CommonParameters</span></span>
<span data-ttu-id="d1b3c-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b3c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b3c-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b3c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b3c-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1b3c-123">INPUTS</span></span>

## <span data-ttu-id="d1b3c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1b3c-124">OUTPUTS</span></span>

## <span data-ttu-id="d1b3c-125">Note</span><span class="sxs-lookup"><span data-stu-id="d1b3c-125">NOTES</span></span>

## <span data-ttu-id="d1b3c-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1b3c-126">RELATED LINKS</span></span>

[<span data-ttu-id="d1b3c-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d1b3c-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="d1b3c-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="d1b3c-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


