---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029725"
---
# <span data-ttu-id="6ce67-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="6ce67-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="6ce67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ce67-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce67-103">Ottiene reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="6ce67-103">Gets virtual networks.</span></span>

## <span data-ttu-id="6ce67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ce67-104">SYNTAX</span></span>

### <span data-ttu-id="6ce67-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ce67-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ce67-106">FromId</span><span class="sxs-lookup"><span data-stu-id="6ce67-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6ce67-107">FromName</span><span class="sxs-lookup"><span data-stu-id="6ce67-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ce67-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ce67-108">DESCRIPTION</span></span>
<span data-ttu-id="6ce67-109">Il cmdlet **Get-WAPackVNet** ottiene reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="6ce67-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="6ce67-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ce67-110">EXAMPLES</span></span>

### <span data-ttu-id="6ce67-111">Esempio 1: ottenere tutte le reti virtuali</span><span class="sxs-lookup"><span data-stu-id="6ce67-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="6ce67-112">Questo comando consente di ottenere tutte le reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="6ce67-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="6ce67-113">Esempio 2: ottenere una rete virtuale usando un ID</span><span class="sxs-lookup"><span data-stu-id="6ce67-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="6ce67-114">Questo comando consente di ottenere la rete virtuale con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="6ce67-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="6ce67-115">Esempio 3: ottenere una rete virtuale usando un nome</span><span class="sxs-lookup"><span data-stu-id="6ce67-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="6ce67-116">Questo comando consente di ottenere la rete virtuale denominata ContosoVNet08.</span><span class="sxs-lookup"><span data-stu-id="6ce67-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="6ce67-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ce67-117">PARAMETERS</span></span>

### <span data-ttu-id="6ce67-118">-ID</span><span class="sxs-lookup"><span data-stu-id="6ce67-118">-ID</span></span>
<span data-ttu-id="6ce67-119">Specifica l'ID univoco di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ce67-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce67-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ce67-120">-Name</span></span>
<span data-ttu-id="6ce67-121">Specifica il nome di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ce67-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce67-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ce67-122">-Profile</span></span>
<span data-ttu-id="6ce67-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce67-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ce67-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6ce67-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ce67-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce67-125">CommonParameters</span></span>
<span data-ttu-id="6ce67-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce67-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce67-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce67-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce67-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ce67-128">INPUTS</span></span>

## <span data-ttu-id="6ce67-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ce67-129">OUTPUTS</span></span>

## <span data-ttu-id="6ce67-130">Note</span><span class="sxs-lookup"><span data-stu-id="6ce67-130">NOTES</span></span>

## <span data-ttu-id="6ce67-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ce67-131">RELATED LINKS</span></span>

