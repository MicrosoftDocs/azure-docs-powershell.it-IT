---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029843"
---
# <span data-ttu-id="bc05c-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="bc05c-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="bc05c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc05c-102">SYNOPSIS</span></span>
<span data-ttu-id="bc05c-103">Aggiunge un utente a una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc05c-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="bc05c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc05c-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc05c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc05c-105">DESCRIPTION</span></span>
<span data-ttu-id="bc05c-106">Il cmdlet **Add-AzureRemoteAppUser** aggiunge un utente a una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc05c-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="bc05c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc05c-107">EXAMPLES</span></span>

### <span data-ttu-id="bc05c-108">Esempio 1: aggiungere un utente con un account Microsoft</span><span class="sxs-lookup"><span data-stu-id="bc05c-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="bc05c-109">Questo comando aggiunge l'account Microsoft PattiFuller@contoso.com alla raccolta denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="bc05c-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="bc05c-110">Esempio 2: aggiungere un utente con un account di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bc05c-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="bc05c-111">Questo comando aggiunge l'account di Azure Active Directory PattiFuller@contoso.com alla raccolta denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="bc05c-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="bc05c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc05c-112">PARAMETERS</span></span>

### <span data-ttu-id="bc05c-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="bc05c-113">-Alias</span></span>
<span data-ttu-id="bc05c-114">Specifica un alias di programma pubblicato.</span><span class="sxs-lookup"><span data-stu-id="bc05c-114">Specifies a published program alias.</span></span>
<span data-ttu-id="bc05c-115">Puoi usare questo parametro solo in modalità di pubblicazione per-app.</span><span class="sxs-lookup"><span data-stu-id="bc05c-115">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc05c-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="bc05c-116">-CollectionName</span></span>
<span data-ttu-id="bc05c-117">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc05c-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="bc05c-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc05c-118">-Profile</span></span>
<span data-ttu-id="bc05c-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc05c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc05c-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bc05c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc05c-121">-Digitare</span><span class="sxs-lookup"><span data-stu-id="bc05c-121">-Type</span></span>
<span data-ttu-id="bc05c-122">Specifica un tipo di utente.</span><span class="sxs-lookup"><span data-stu-id="bc05c-122">Specifies a user type.</span></span>
<span data-ttu-id="bc05c-123">I valori accettabili per questo parametro sono: OrgId o MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="bc05c-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc05c-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="bc05c-124">-UserUpn</span></span>
<span data-ttu-id="bc05c-125">Specifica il nome dell'entità utente (UPN) di un utente, ad esempio PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="bc05c-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc05c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc05c-126">CommonParameters</span></span>
<span data-ttu-id="bc05c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc05c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc05c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc05c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc05c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc05c-129">INPUTS</span></span>

## <span data-ttu-id="bc05c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc05c-130">OUTPUTS</span></span>

## <span data-ttu-id="bc05c-131">Note</span><span class="sxs-lookup"><span data-stu-id="bc05c-131">NOTES</span></span>

## <span data-ttu-id="bc05c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc05c-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc05c-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="bc05c-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="bc05c-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="bc05c-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


