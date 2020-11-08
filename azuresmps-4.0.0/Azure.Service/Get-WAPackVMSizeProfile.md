---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030892"
---
# <span data-ttu-id="99d5b-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="99d5b-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="99d5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="99d5b-103">Ottiene gli oggetti del profilo di dimensione.</span><span class="sxs-lookup"><span data-stu-id="99d5b-103">Gets size profile objects.</span></span>

## <span data-ttu-id="99d5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99d5b-104">SYNTAX</span></span>

### <span data-ttu-id="99d5b-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99d5b-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99d5b-106">FromId</span><span class="sxs-lookup"><span data-stu-id="99d5b-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="99d5b-107">FromName</span><span class="sxs-lookup"><span data-stu-id="99d5b-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99d5b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99d5b-108">DESCRIPTION</span></span>
<span data-ttu-id="99d5b-109">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="99d5b-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="99d5b-110">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="99d5b-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99d5b-111">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99d5b-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="99d5b-112">Il cmdlet **Get-WAPackVMSizeProfile** ottiene gli oggetti del profilo di dimensione per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="99d5b-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="99d5b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99d5b-113">EXAMPLES</span></span>

### <span data-ttu-id="99d5b-114">Esempio 1: ottenere un profilo di dimensione usando un nome</span><span class="sxs-lookup"><span data-stu-id="99d5b-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="99d5b-115">Questo comando ottiene il profilo di dimensione denominato ContosoSizeProfile07.</span><span class="sxs-lookup"><span data-stu-id="99d5b-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="99d5b-116">Esempio 2: ottenere un profilo di dimensione usando un ID</span><span class="sxs-lookup"><span data-stu-id="99d5b-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="99d5b-117">Questo comando ottiene il profilo di dimensione con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="99d5b-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="99d5b-118">Esempio 3: ottenere tutti i profili di dimensione</span><span class="sxs-lookup"><span data-stu-id="99d5b-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="99d5b-119">Questo comando ottiene tutti i profili di dimensione.</span><span class="sxs-lookup"><span data-stu-id="99d5b-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="99d5b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99d5b-120">PARAMETERS</span></span>

### <span data-ttu-id="99d5b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="99d5b-121">-ID</span></span>
<span data-ttu-id="99d5b-122">Specifica l'ID univoco di un profilo di dimensione.</span><span class="sxs-lookup"><span data-stu-id="99d5b-122">Specifies the unique ID of a size profile.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d5b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="99d5b-123">-Name</span></span>
<span data-ttu-id="99d5b-124">Specifica il nome di un profilo di dimensione.</span><span class="sxs-lookup"><span data-stu-id="99d5b-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="99d5b-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="99d5b-125">-Profile</span></span>
<span data-ttu-id="99d5b-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d5b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99d5b-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="99d5b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99d5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d5b-128">CommonParameters</span></span>
<span data-ttu-id="99d5b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d5b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d5b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d5b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99d5b-131">INPUTS</span></span>

## <span data-ttu-id="99d5b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99d5b-132">OUTPUTS</span></span>

## <span data-ttu-id="99d5b-133">Note</span><span class="sxs-lookup"><span data-stu-id="99d5b-133">NOTES</span></span>

## <span data-ttu-id="99d5b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99d5b-134">RELATED LINKS</span></span>

[<span data-ttu-id="99d5b-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="99d5b-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


