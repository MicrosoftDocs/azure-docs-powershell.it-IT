---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023571"
---
# <span data-ttu-id="6b73c-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="6b73c-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="6b73c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b73c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b73c-103">Ottiene lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6b73c-103">Gets the namespace.</span></span>


## <span data-ttu-id="6b73c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b73c-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6b73c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b73c-105">DESCRIPTION</span></span>
<span data-ttu-id="6b73c-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b73c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6b73c-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6b73c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6b73c-108">Il cmdlet **Get-AzureSBNamespace** restituisce gli spazi dei nomi del servizio bus di servizio associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6b73c-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="6b73c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b73c-109">EXAMPLES</span></span>

### <span data-ttu-id="6b73c-110">Esempio 1: ottenere lo spazio dei nomi Service Bus</span><span class="sxs-lookup"><span data-stu-id="6b73c-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="6b73c-111">Questo esempio consente di ottenere gli spazi dei nomi del servizio bus di servizio associati alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6b73c-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="6b73c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b73c-112">PARAMETERS</span></span>

### <span data-ttu-id="6b73c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b73c-113">-Name</span></span>
<span data-ttu-id="6b73c-114">Specifica il nome di uno spazio dei nomi di Service Bus da cercare.</span><span class="sxs-lookup"><span data-stu-id="6b73c-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="6b73c-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="6b73c-115">-Profile</span></span>
<span data-ttu-id="6b73c-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b73c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b73c-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6b73c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b73c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b73c-118">CommonParameters</span></span>
<span data-ttu-id="6b73c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b73c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b73c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b73c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b73c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b73c-121">INPUTS</span></span>

## <span data-ttu-id="6b73c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b73c-122">OUTPUTS</span></span>

## <span data-ttu-id="6b73c-123">Note</span><span class="sxs-lookup"><span data-stu-id="6b73c-123">NOTES</span></span>

## <span data-ttu-id="6b73c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b73c-124">RELATED LINKS</span></span>

[<span data-ttu-id="6b73c-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="6b73c-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


