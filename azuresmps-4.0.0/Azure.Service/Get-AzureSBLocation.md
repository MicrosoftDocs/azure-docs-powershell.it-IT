---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029774"
---
# <span data-ttu-id="69cd3-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="69cd3-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="69cd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="69cd3-103">Ottiene la posizione del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="69cd3-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="69cd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69cd3-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69cd3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="69cd3-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69cd3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69cd3-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="69cd3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69cd3-108">Il cmdlet **Get-AzureSBLocation** restituisce i percorsi da cui è disponibile il bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="69cd3-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="69cd3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="69cd3-110">Esempio 1: ottenere la posizione del bus di servizio</span><span class="sxs-lookup"><span data-stu-id="69cd3-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="69cd3-111">Questo esempio consente di ottenere la posizione del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="69cd3-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="69cd3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69cd3-112">PARAMETERS</span></span>

### <span data-ttu-id="69cd3-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="69cd3-113">-Profile</span></span>
<span data-ttu-id="69cd3-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69cd3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69cd3-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="69cd3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69cd3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69cd3-116">CommonParameters</span></span>
<span data-ttu-id="69cd3-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69cd3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69cd3-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69cd3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69cd3-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69cd3-119">INPUTS</span></span>

## <span data-ttu-id="69cd3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69cd3-120">OUTPUTS</span></span>

## <span data-ttu-id="69cd3-121">Note</span><span class="sxs-lookup"><span data-stu-id="69cd3-121">NOTES</span></span>

## <span data-ttu-id="69cd3-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69cd3-122">RELATED LINKS</span></span>

[<span data-ttu-id="69cd3-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="69cd3-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


