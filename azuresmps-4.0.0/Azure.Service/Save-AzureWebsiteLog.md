---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023416"
---
# <span data-ttu-id="9e6b3-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="9e6b3-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="9e6b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6b3-103">Scarica e salva i registri per un sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="9e6b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e6b3-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9e6b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6b3-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9e6b3-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9e6b3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9e6b3-108">Il cmdlet **Save-AzureWebsiteLog** Scarica i registri per un sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="9e6b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e6b3-109">EXAMPLES</span></span>

### <span data-ttu-id="9e6b3-110">Esempio 1: scaricare e salvare i log per un sito Web</span><span class="sxs-lookup"><span data-stu-id="9e6b3-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="9e6b3-111">In questo esempio vengono scaricati i registri di runtime e distribuzione per sito Web site nel file logs.zip nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="9e6b3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e6b3-112">PARAMETERS</span></span>

### <span data-ttu-id="9e6b3-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e6b3-113">-Name</span></span>
<span data-ttu-id="9e6b3-114">Specifica il nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="9e6b3-115">-Output</span><span class="sxs-lookup"><span data-stu-id="9e6b3-115">-Output</span></span>
<span data-ttu-id="9e6b3-116">Specifica il percorso in cui archiviare il file scaricato.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="9e6b3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e6b3-117">-PassThru</span></span>
<span data-ttu-id="9e6b3-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e6b3-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e6b3-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="9e6b3-120">-Profile</span></span>
<span data-ttu-id="9e6b3-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e6b3-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e6b3-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="9e6b3-123">-Slot</span></span>
<span data-ttu-id="9e6b3-124">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="9e6b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6b3-125">CommonParameters</span></span>
<span data-ttu-id="9e6b3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6b3-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6b3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6b3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e6b3-128">INPUTS</span></span>

## <span data-ttu-id="9e6b3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e6b3-129">OUTPUTS</span></span>

## <span data-ttu-id="9e6b3-130">Note</span><span class="sxs-lookup"><span data-stu-id="9e6b3-130">NOTES</span></span>

## <span data-ttu-id="9e6b3-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e6b3-131">RELATED LINKS</span></span>

[<span data-ttu-id="9e6b3-132">Ripristinare-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="9e6b3-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


