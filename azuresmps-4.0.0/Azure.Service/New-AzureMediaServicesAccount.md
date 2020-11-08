---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023869"
---
# <span data-ttu-id="a2bc1-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a2bc1-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="a2bc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bc1-103">Crea un account di servizi di Azure Media.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="a2bc1-104">**Nota:** Questa versione è deprecata, vedere la [versione più recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="a2bc1-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="a2bc1-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2bc1-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2bc1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2bc1-106">DESCRIPTION</span></span>
<span data-ttu-id="a2bc1-107">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a2bc1-108">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a2bc1-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a2bc1-109">Il cmdlet **New-AzureMediaServicesAccount** crea un nuovo account di servizi multimediali con il nome dell'account di servizi multimediali specificato, la posizione del centro dati in cui si vuole creare l'account e un nome dell'account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="a2bc1-110">L'account di archiviazione deve trovarsi nello stesso centro dati del nuovo account di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="a2bc1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2bc1-111">EXAMPLES</span></span>

### <span data-ttu-id="a2bc1-112">Esempio 1: creare un nuovo account di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="a2bc1-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="a2bc1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2bc1-113">PARAMETERS</span></span>

### <span data-ttu-id="a2bc1-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a2bc1-114">-Location</span></span>
<span data-ttu-id="a2bc1-115">Specifica la posizione del centro dati Media Services.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="a2bc1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2bc1-116">-Name</span></span>
<span data-ttu-id="a2bc1-117">Specifica il nome dell'account dei servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="a2bc1-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="a2bc1-118">-Profile</span></span>
<span data-ttu-id="a2bc1-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2bc1-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2bc1-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2bc1-121">-StorageAccountName</span></span>
<span data-ttu-id="a2bc1-122">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-122">Specifies the storage account name.</span></span>
<span data-ttu-id="a2bc1-123">L'account di archiviazione deve essere già presente nello stesso data center del nuovo account di servizi multimediali.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="a2bc1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bc1-124">CommonParameters</span></span>
<span data-ttu-id="a2bc1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2bc1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bc1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2bc1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bc1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2bc1-127">INPUTS</span></span>

## <span data-ttu-id="a2bc1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2bc1-128">OUTPUTS</span></span>

## <span data-ttu-id="a2bc1-129">Note</span><span class="sxs-lookup"><span data-stu-id="a2bc1-129">NOTES</span></span>

## <span data-ttu-id="a2bc1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2bc1-130">RELATED LINKS</span></span>

[<span data-ttu-id="a2bc1-131">Come usare Azure PowerShell per i servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="a2bc1-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="a2bc1-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a2bc1-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="a2bc1-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a2bc1-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


