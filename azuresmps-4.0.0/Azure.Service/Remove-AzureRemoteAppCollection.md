---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023826"
---
# <span data-ttu-id="d6cc8-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d6cc8-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="d6cc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cc8-103">Rimuove una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d6cc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6cc8-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6cc8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="d6cc8-106">Il cmdlet **Remove-AzureRemoteAppCollection** rimuove una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="d6cc8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6cc8-107">EXAMPLES</span></span>

## <span data-ttu-id="d6cc8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6cc8-108">PARAMETERS</span></span>

### <span data-ttu-id="d6cc8-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d6cc8-109">-CollectionName</span></span>
<span data-ttu-id="d6cc8-110">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-110">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cc8-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6cc8-111">-Profile</span></span>
<span data-ttu-id="d6cc8-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6cc8-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6cc8-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6cc8-114">-Confirm</span></span>
<span data-ttu-id="d6cc8-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cc8-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cc8-116">-WhatIf</span></span>
<span data-ttu-id="d6cc8-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cc8-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cc8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cc8-119">CommonParameters</span></span>
<span data-ttu-id="d6cc8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cc8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cc8-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6cc8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cc8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6cc8-122">INPUTS</span></span>

## <span data-ttu-id="d6cc8-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6cc8-123">OUTPUTS</span></span>

## <span data-ttu-id="d6cc8-124">Note</span><span class="sxs-lookup"><span data-stu-id="d6cc8-124">NOTES</span></span>

## <span data-ttu-id="d6cc8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6cc8-125">RELATED LINKS</span></span>

[<span data-ttu-id="d6cc8-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d6cc8-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="d6cc8-127">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d6cc8-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="d6cc8-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d6cc8-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="d6cc8-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d6cc8-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


