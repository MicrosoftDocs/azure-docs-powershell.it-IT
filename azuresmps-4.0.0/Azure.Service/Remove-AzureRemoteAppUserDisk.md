---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029609"
---
# <span data-ttu-id="43f26-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="43f26-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="43f26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43f26-102">SYNOPSIS</span></span>
<span data-ttu-id="43f26-103">Rimuove il disco utente di un utente da una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f26-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="43f26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43f26-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43f26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f26-105">DESCRIPTION</span></span>
<span data-ttu-id="43f26-106">Il cmdlet **Remove-AzureRemoteAppUserDisk** rimuove il disco utente di un utente da una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f26-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="43f26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43f26-107">EXAMPLES</span></span>

### <span data-ttu-id="43f26-108">Esempio 1: rimuovere un disco utente</span><span class="sxs-lookup"><span data-stu-id="43f26-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="43f26-109">Questo comando rimuove il disco utente di un utente di Azure Active Directory che ha l'UPN della PattiFuller@contoso.com raccolta Contoso01.</span><span class="sxs-lookup"><span data-stu-id="43f26-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="43f26-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43f26-110">PARAMETERS</span></span>

### <span data-ttu-id="43f26-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="43f26-111">-CollectionName</span></span>
<span data-ttu-id="43f26-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f26-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f26-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="43f26-113">-Profile</span></span>
<span data-ttu-id="43f26-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f26-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43f26-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="43f26-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43f26-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="43f26-116">-UserUpn</span></span>
<span data-ttu-id="43f26-117">Specifica il nome dell'entità utente (UPN) dell'utente per cui questo cmdlet rimuove il disco.</span><span class="sxs-lookup"><span data-stu-id="43f26-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="43f26-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43f26-118">-Confirm</span></span>
<span data-ttu-id="43f26-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f26-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f26-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f26-120">-WhatIf</span></span>
<span data-ttu-id="43f26-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f26-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f26-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f26-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f26-123">CommonParameters</span></span>
<span data-ttu-id="43f26-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f26-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f26-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f26-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43f26-126">INPUTS</span></span>

## <span data-ttu-id="43f26-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43f26-127">OUTPUTS</span></span>

## <span data-ttu-id="43f26-128">Note</span><span class="sxs-lookup"><span data-stu-id="43f26-128">NOTES</span></span>

## <span data-ttu-id="43f26-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43f26-129">RELATED LINKS</span></span>

[<span data-ttu-id="43f26-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="43f26-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


