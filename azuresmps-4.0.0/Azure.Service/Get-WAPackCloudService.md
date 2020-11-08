---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030815"
---
# <span data-ttu-id="c20a6-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c20a6-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="c20a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c20a6-102">SYNOPSIS</span></span>
<span data-ttu-id="c20a6-103">Ottiene gli oggetti del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c20a6-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="c20a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c20a6-104">SYNTAX</span></span>

### <span data-ttu-id="c20a6-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c20a6-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c20a6-106">FromName</span><span class="sxs-lookup"><span data-stu-id="c20a6-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c20a6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c20a6-107">DESCRIPTION</span></span>
<span data-ttu-id="c20a6-108">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="c20a6-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="c20a6-109">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a6-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c20a6-110">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c20a6-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c20a6-111">Il cmdlet **Get-WAPackCloudService** ottiene gli oggetti del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c20a6-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="c20a6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c20a6-112">EXAMPLES</span></span>

## <span data-ttu-id="c20a6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c20a6-113">PARAMETERS</span></span>

### <span data-ttu-id="c20a6-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c20a6-114">-Name</span></span>
<span data-ttu-id="c20a6-115">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="c20a6-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="c20a6-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="c20a6-116">-Profile</span></span>
<span data-ttu-id="c20a6-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c20a6-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c20a6-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c20a6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c20a6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20a6-119">CommonParameters</span></span>
<span data-ttu-id="c20a6-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c20a6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20a6-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20a6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20a6-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c20a6-122">INPUTS</span></span>

## <span data-ttu-id="c20a6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c20a6-123">OUTPUTS</span></span>

## <span data-ttu-id="c20a6-124">Note</span><span class="sxs-lookup"><span data-stu-id="c20a6-124">NOTES</span></span>

## <span data-ttu-id="c20a6-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c20a6-125">RELATED LINKS</span></span>

[<span data-ttu-id="c20a6-126">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c20a6-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="c20a6-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="c20a6-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


