---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023893"
---
# <span data-ttu-id="f186f-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="f186f-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="f186f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f186f-102">SYNOPSIS</span></span>
<span data-ttu-id="f186f-103">Controlla se un nome di dominio è disponibile come profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f186f-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="f186f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f186f-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f186f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f186f-105">DESCRIPTION</span></span>
<span data-ttu-id="f186f-106">Il cmdlet **test-AzureTrafficManagerDomainName** controlla se un nome di dominio è disponibile come profilo di Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f186f-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f186f-107">Se il nome di dominio è disponibile, questo cmdlet restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="f186f-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="f186f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f186f-108">EXAMPLES</span></span>

### <span data-ttu-id="f186f-109">Esempio 1: verificare se è disponibile un nome di dominio</span><span class="sxs-lookup"><span data-stu-id="f186f-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="f186f-110">Questo comando controlla se il nome di dominio ContosoApp.trafficmanager.net è disponibile come profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f186f-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="f186f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f186f-111">PARAMETERS</span></span>

### <span data-ttu-id="f186f-112">-DomainName</span><span class="sxs-lookup"><span data-stu-id="f186f-112">-DomainName</span></span>
<span data-ttu-id="f186f-113">Specifica il nome di dominio da testare.</span><span class="sxs-lookup"><span data-stu-id="f186f-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="f186f-114">È necessario includere la stringa seguente:</span><span class="sxs-lookup"><span data-stu-id="f186f-114">You must include the following string:</span></span> 

<span data-ttu-id="f186f-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="f186f-115">.trafficmanager.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f186f-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="f186f-116">-Profile</span></span>
<span data-ttu-id="f186f-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f186f-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f186f-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f186f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f186f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f186f-119">CommonParameters</span></span>
<span data-ttu-id="f186f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f186f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f186f-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f186f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f186f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f186f-122">INPUTS</span></span>

## <span data-ttu-id="f186f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f186f-123">OUTPUTS</span></span>

### <span data-ttu-id="f186f-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f186f-124">System.Boolean</span></span>
<span data-ttu-id="f186f-125">Questo cmdlet genera $True o $False.</span><span class="sxs-lookup"><span data-stu-id="f186f-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="f186f-126">Se il nome di dominio è disponibile, questo cmdlet restituisce un valore di $True.</span><span class="sxs-lookup"><span data-stu-id="f186f-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="f186f-127">Note</span><span class="sxs-lookup"><span data-stu-id="f186f-127">NOTES</span></span>

## <span data-ttu-id="f186f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f186f-128">RELATED LINKS</span></span>

