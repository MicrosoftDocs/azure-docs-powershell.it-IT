---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023906"
---
# <span data-ttu-id="0334b-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="0334b-101">Show-AzurePortal</span></span>

## <span data-ttu-id="0334b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0334b-102">SYNOPSIS</span></span>
<span data-ttu-id="0334b-103">Mostra il portale di gestione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0334b-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="0334b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0334b-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0334b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0334b-105">DESCRIPTION</span></span>
<span data-ttu-id="0334b-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0334b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0334b-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0334b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0334b-108">Il cmdlet **show-AzurePortal** Mostra il portale di gestione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0334b-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="0334b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0334b-109">EXAMPLES</span></span>

### <span data-ttu-id="0334b-110">Esempio 1: visualizzare informazioni su un sito Web</span><span class="sxs-lookup"><span data-stu-id="0334b-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="0334b-111">Questo esempio apre un browser in Azure Portal, che mostra le informazioni su un sito Web denominato sito.</span><span class="sxs-lookup"><span data-stu-id="0334b-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="0334b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0334b-112">PARAMETERS</span></span>

### <span data-ttu-id="0334b-113">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="0334b-113">-Environment</span></span>
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

### <span data-ttu-id="0334b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0334b-114">-Name</span></span>
<span data-ttu-id="0334b-115">Specifica il nome del sito Web da visualizzare nel portale.</span><span class="sxs-lookup"><span data-stu-id="0334b-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="0334b-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="0334b-116">-Profile</span></span>
<span data-ttu-id="0334b-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0334b-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0334b-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0334b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0334b-119">-Realm</span><span class="sxs-lookup"><span data-stu-id="0334b-119">-Realm</span></span>
<span data-ttu-id="0334b-120">Specifica l'ID organizzazione da usare per l'autenticazione federata quando si Visualizza il portale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0334b-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="0334b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0334b-121">CommonParameters</span></span>
<span data-ttu-id="0334b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0334b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0334b-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0334b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0334b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0334b-124">INPUTS</span></span>

## <span data-ttu-id="0334b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0334b-125">OUTPUTS</span></span>

## <span data-ttu-id="0334b-126">Note</span><span class="sxs-lookup"><span data-stu-id="0334b-126">NOTES</span></span>

## <span data-ttu-id="0334b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0334b-127">RELATED LINKS</span></span>

[<span data-ttu-id="0334b-128">Mostra-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0334b-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


