---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023656"
---
# <span data-ttu-id="0dc5c-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="0dc5c-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="0dc5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0dc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc5c-103">Copia il disco utente di un utente da una raccolta RemoteApp di Azure a un'altra.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="0dc5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0dc5c-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0dc5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dc5c-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc5c-106">Il cmdlet **Copy-AzureRemoteAppUserDisk** copia il disco utente di un utente da una raccolta RemoteApp di Azure a un'altra.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="0dc5c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0dc5c-107">EXAMPLES</span></span>

### <span data-ttu-id="0dc5c-108">Esempio 1: copiare un disco utente</span><span class="sxs-lookup"><span data-stu-id="0dc5c-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="0dc5c-109">Questo comando copia il disco utente di un utente di Azure Active Directory che ha l'UPN della PattiFuller@contoso.com raccolta Contoso01 alla raccolta Contoso02.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="0dc5c-110">Se un disco utente PattiFuller@contoso.com esiste già in Contoso02, questo comando lo sovrascrive.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="0dc5c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0dc5c-111">PARAMETERS</span></span>

### <span data-ttu-id="0dc5c-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="0dc5c-112">-DestinationCollectionName</span></span>
<span data-ttu-id="0dc5c-113">Specifica il nome della raccolta RemoteApp di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="0dc5c-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="0dc5c-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="0dc5c-115">Indica che questo cmdlet sovrascrive un disco utente esistente.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="0dc5c-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="0dc5c-116">-Profile</span></span>
<span data-ttu-id="0dc5c-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0dc5c-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0dc5c-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0dc5c-119">-SourceCollectionName</span></span>
<span data-ttu-id="0dc5c-120">Specifica il nome della raccolta RemoteApp di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="0dc5c-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="0dc5c-121">-UserUpn</span></span>
<span data-ttu-id="0dc5c-122">Specifica il nome dell'entità utente (UPN) dell'utente per cui questo cmdlet copia il disco.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc5c-123">CommonParameters</span></span>
<span data-ttu-id="0dc5c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc5c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc5c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0dc5c-126">INPUTS</span></span>

## <span data-ttu-id="0dc5c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0dc5c-127">OUTPUTS</span></span>

## <span data-ttu-id="0dc5c-128">Note</span><span class="sxs-lookup"><span data-stu-id="0dc5c-128">NOTES</span></span>

## <span data-ttu-id="0dc5c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0dc5c-129">RELATED LINKS</span></span>

[<span data-ttu-id="0dc5c-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="0dc5c-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


