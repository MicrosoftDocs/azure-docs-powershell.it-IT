---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029797"
---
# <span data-ttu-id="d0b06-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d0b06-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="d0b06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0b06-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b06-103">Ottiene gli account di servizi di Azure Media disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0b06-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="d0b06-104">**Nota:** Questa versione è deprecata, vedere la [versione più recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="d0b06-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="d0b06-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0b06-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0b06-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0b06-106">DESCRIPTION</span></span>
<span data-ttu-id="d0b06-107">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b06-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d0b06-108">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d0b06-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d0b06-109">Per elencare tutti gli account, usare il `Get-AzureMediaServicesAccount` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b06-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="d0b06-110">Per ottenere informazioni più dettagliate su un account specifico, usare il `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b06-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="d0b06-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0b06-111">EXAMPLES</span></span>

### <span data-ttu-id="d0b06-112">Esempio 1: elencare tutti gli account di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="d0b06-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="d0b06-113">Questo comando elenca tutti gli account di servizi multimediali disponibili.</span><span class="sxs-lookup"><span data-stu-id="d0b06-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="d0b06-114">Esempio 2: ottenere informazioni dettagliate su un account di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="d0b06-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="d0b06-115">Questo comando Visualizza le proprietà di un account di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="d0b06-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="d0b06-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0b06-116">PARAMETERS</span></span>

### <span data-ttu-id="d0b06-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0b06-117">-Name</span></span>
<span data-ttu-id="d0b06-118">Nome dell'account dei servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="d0b06-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="d0b06-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="d0b06-119">-Profile</span></span>
<span data-ttu-id="d0b06-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0b06-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d0b06-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d0b06-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0b06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b06-122">CommonParameters</span></span>
<span data-ttu-id="d0b06-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b06-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0b06-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b06-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0b06-125">INPUTS</span></span>

## <span data-ttu-id="d0b06-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0b06-126">OUTPUTS</span></span>

## <span data-ttu-id="d0b06-127">Note</span><span class="sxs-lookup"><span data-stu-id="d0b06-127">NOTES</span></span>

## <span data-ttu-id="d0b06-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0b06-128">RELATED LINKS</span></span>

[<span data-ttu-id="d0b06-129">Come usare Azure PowerShell per i servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="d0b06-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


