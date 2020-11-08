---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023695"
---
# <span data-ttu-id="27745-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="27745-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="27745-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27745-102">SYNOPSIS</span></span>
<span data-ttu-id="27745-103">Aggiorna una raccolta RemoteApp di Azure con una nuova immagine del modello.</span><span class="sxs-lookup"><span data-stu-id="27745-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="27745-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27745-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27745-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27745-105">DESCRIPTION</span></span>
<span data-ttu-id="27745-106">Il cmdlet **Update-AzureRemoteAppCollection** aggiorna una raccolta RemoteApp di Azure con una nuova immagine del modello.</span><span class="sxs-lookup"><span data-stu-id="27745-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="27745-107">Al termine dell'aggiornamento, gli utenti con sessioni esistenti hanno un'ora per disconnettersi prima di essere disconnessi automaticamente. Dopo l'accesso, si connettono alla raccolta appena aggiornata.</span><span class="sxs-lookup"><span data-stu-id="27745-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="27745-108">Per forzare l'accesso immediato degli utenti non appena viene aggiornata la raccolta, specifica il parametro *ForceLogoffWhenUpdateComplete* .</span><span class="sxs-lookup"><span data-stu-id="27745-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="27745-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27745-109">EXAMPLES</span></span>

## <span data-ttu-id="27745-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27745-110">PARAMETERS</span></span>

### <span data-ttu-id="27745-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="27745-111">-CollectionName</span></span>
<span data-ttu-id="27745-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="27745-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="27745-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="27745-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="27745-114">Indica che questo cmdlet firma gli utenti dalle sessioni esistenti non appena viene completato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="27745-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="27745-115">Quando gli utenti accedono di nuovo, si connettono alla nuova raccolta aggiornata.</span><span class="sxs-lookup"><span data-stu-id="27745-115">When users sign in again, they connect to the newly updated collection.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27745-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="27745-116">-ImageName</span></span>
<span data-ttu-id="27745-117">Specifica il nome di un'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="27745-117">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27745-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="27745-118">-Profile</span></span>
<span data-ttu-id="27745-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27745-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27745-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="27745-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27745-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="27745-121">-SubnetName</span></span>
<span data-ttu-id="27745-122">Specifica il nome della subnet in cui trasferire la raccolta.</span><span class="sxs-lookup"><span data-stu-id="27745-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27745-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27745-123">-Confirm</span></span>
<span data-ttu-id="27745-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27745-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27745-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27745-125">-WhatIf</span></span>
<span data-ttu-id="27745-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27745-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27745-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27745-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27745-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27745-128">CommonParameters</span></span>
<span data-ttu-id="27745-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27745-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27745-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27745-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27745-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27745-131">INPUTS</span></span>

## <span data-ttu-id="27745-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27745-132">OUTPUTS</span></span>

## <span data-ttu-id="27745-133">Note</span><span class="sxs-lookup"><span data-stu-id="27745-133">NOTES</span></span>

## <span data-ttu-id="27745-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27745-134">RELATED LINKS</span></span>

[<span data-ttu-id="27745-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="27745-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="27745-136">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="27745-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="27745-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="27745-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


