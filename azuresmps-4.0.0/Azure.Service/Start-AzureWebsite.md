---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023728"
---
# <span data-ttu-id="89bd6-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="89bd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="89bd6-103">Avvia il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="89bd6-103">Starts the specified website.</span></span>

## <span data-ttu-id="89bd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89bd6-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="89bd6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="89bd6-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="89bd6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="89bd6-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="89bd6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="89bd6-108">Il cmdlet **Start-AzureWebsite** avvia un sito Web specificato in uso in Azure.</span><span class="sxs-lookup"><span data-stu-id="89bd6-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="89bd6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89bd6-109">EXAMPLES</span></span>

## <span data-ttu-id="89bd6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89bd6-110">PARAMETERS</span></span>

### <span data-ttu-id="89bd6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="89bd6-111">-Name</span></span>
<span data-ttu-id="89bd6-112">Specifica il nome del sito Web da avviare.</span><span class="sxs-lookup"><span data-stu-id="89bd6-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="89bd6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89bd6-113">-PassThru</span></span>
<span data-ttu-id="89bd6-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="89bd6-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="89bd6-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="89bd6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="89bd6-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="89bd6-116">-Profile</span></span>
<span data-ttu-id="89bd6-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89bd6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89bd6-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="89bd6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89bd6-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="89bd6-119">-Slot</span></span>
<span data-ttu-id="89bd6-120">Specifica il nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="89bd6-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="89bd6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bd6-121">CommonParameters</span></span>
<span data-ttu-id="89bd6-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bd6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bd6-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89bd6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bd6-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89bd6-124">INPUTS</span></span>

## <span data-ttu-id="89bd6-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89bd6-125">OUTPUTS</span></span>

## <span data-ttu-id="89bd6-126">Note</span><span class="sxs-lookup"><span data-stu-id="89bd6-126">NOTES</span></span>

## <span data-ttu-id="89bd6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89bd6-127">RELATED LINKS</span></span>

[<span data-ttu-id="89bd6-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="89bd6-129">Riavviare-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="89bd6-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="89bd6-131">Mostra-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="89bd6-132">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="89bd6-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


