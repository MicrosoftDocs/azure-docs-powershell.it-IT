---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029482"
---
# <span data-ttu-id="b2e25-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="b2e25-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="b2e25-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2e25-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e25-103">Annulla la pubblicazione di un programma RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e25-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="b2e25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2e25-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e25-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2e25-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e25-106">Il cmdlet **Unpublish-AzureRemoteAppProgram** Annulla la pubblicazione di un programma RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e25-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="b2e25-107">Dopo avere annullato la pubblicazione di un programma, non sarà più disponibile per gli utenti di una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e25-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b2e25-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2e25-108">EXAMPLES</span></span>

## <span data-ttu-id="b2e25-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2e25-109">PARAMETERS</span></span>

### <span data-ttu-id="b2e25-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="b2e25-110">-Alias</span></span>
<span data-ttu-id="b2e25-111">Specifica una matrice di alias dei programmi da annullare la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b2e25-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="b2e25-112">USA **Get-AzureRemoteAppProgram** per recuperare l'alias di un programma da annullare la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b2e25-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e25-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b2e25-113">-CollectionName</span></span>
<span data-ttu-id="b2e25-114">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e25-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="b2e25-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="b2e25-115">-Profile</span></span>
<span data-ttu-id="b2e25-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e25-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2e25-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b2e25-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2e25-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2e25-118">-Confirm</span></span>
<span data-ttu-id="b2e25-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e25-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e25-120">-WhatIf</span></span>
<span data-ttu-id="b2e25-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e25-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e25-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2e25-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e25-123">CommonParameters</span></span>
<span data-ttu-id="b2e25-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e25-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e25-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e25-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2e25-126">INPUTS</span></span>

## <span data-ttu-id="b2e25-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2e25-127">OUTPUTS</span></span>

## <span data-ttu-id="b2e25-128">Note</span><span class="sxs-lookup"><span data-stu-id="b2e25-128">NOTES</span></span>

## <span data-ttu-id="b2e25-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2e25-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2e25-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="b2e25-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="b2e25-131">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="b2e25-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


