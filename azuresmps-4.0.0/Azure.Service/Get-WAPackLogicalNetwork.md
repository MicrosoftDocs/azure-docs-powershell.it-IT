---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030816"
---
# <span data-ttu-id="862f3-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="862f3-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="862f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="862f3-102">SYNOPSIS</span></span>
<span data-ttu-id="862f3-103">Ottiene oggetti di rete logici.</span><span class="sxs-lookup"><span data-stu-id="862f3-103">Gets logical network objects.</span></span>

## <span data-ttu-id="862f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="862f3-104">SYNTAX</span></span>

### <span data-ttu-id="862f3-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="862f3-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="862f3-106">FromName</span><span class="sxs-lookup"><span data-stu-id="862f3-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="862f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="862f3-107">DESCRIPTION</span></span>
<span data-ttu-id="862f3-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="862f3-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="862f3-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="862f3-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="862f3-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="862f3-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="862f3-111">Il cmdlet **Get-WAPackLogicalNetwork** ottiene gli oggetti di rete logici.</span><span class="sxs-lookup"><span data-stu-id="862f3-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="862f3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="862f3-112">EXAMPLES</span></span>

### <span data-ttu-id="862f3-113">Esempio 1: ottenere una rete logica usando un nome</span><span class="sxs-lookup"><span data-stu-id="862f3-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="862f3-114">Questo comando consente di ottenere una rete logica denominata ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="862f3-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="862f3-115">Esempio 2: ottenere tutte le reti logiche</span><span class="sxs-lookup"><span data-stu-id="862f3-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="862f3-116">Questo comando consente di ottenere tutte le reti logiche.</span><span class="sxs-lookup"><span data-stu-id="862f3-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="862f3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="862f3-117">PARAMETERS</span></span>

### <span data-ttu-id="862f3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="862f3-118">-Name</span></span>
<span data-ttu-id="862f3-119">Specifica il nome di una rete logica.</span><span class="sxs-lookup"><span data-stu-id="862f3-119">Specifies the name of a logical network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862f3-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="862f3-120">-Profile</span></span>
<span data-ttu-id="862f3-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="862f3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="862f3-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="862f3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="862f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862f3-123">CommonParameters</span></span>
<span data-ttu-id="862f3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="862f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862f3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862f3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862f3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="862f3-126">INPUTS</span></span>

## <span data-ttu-id="862f3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="862f3-127">OUTPUTS</span></span>

## <span data-ttu-id="862f3-128">Note</span><span class="sxs-lookup"><span data-stu-id="862f3-128">NOTES</span></span>

## <span data-ttu-id="862f3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="862f3-129">RELATED LINKS</span></span>

