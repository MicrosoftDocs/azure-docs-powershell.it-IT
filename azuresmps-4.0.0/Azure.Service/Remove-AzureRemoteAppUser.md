---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023824"
---
# <span data-ttu-id="1310b-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1310b-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="1310b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1310b-102">SYNOPSIS</span></span>
<span data-ttu-id="1310b-103">Rimuove un utente da una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1310b-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1310b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1310b-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1310b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1310b-105">DESCRIPTION</span></span>
<span data-ttu-id="1310b-106">Il cmdlet **Remove-AzureRemoteAppUser** consente di rimuovere un utente da una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1310b-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="1310b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1310b-107">EXAMPLES</span></span>

### <span data-ttu-id="1310b-108">Esempio1: rimuovere un utente da una raccolta</span><span class="sxs-lookup"><span data-stu-id="1310b-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="1310b-109">Questo comando rimuove l'utente di Azure ActiveDirectory PattiFuller@contoso.com dalla raccolta contoso.</span><span class="sxs-lookup"><span data-stu-id="1310b-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="1310b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1310b-110">PARAMETERS</span></span>

### <span data-ttu-id="1310b-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="1310b-111">-Alias</span></span>
<span data-ttu-id="1310b-112">Specifica un alias di programma pubblicato.</span><span class="sxs-lookup"><span data-stu-id="1310b-112">Specifies a published program alias.</span></span>
<span data-ttu-id="1310b-113">Puoi usare questo parametro solo in modalità di pubblicazione per-app.</span><span class="sxs-lookup"><span data-stu-id="1310b-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="1310b-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1310b-114">-CollectionName</span></span>
<span data-ttu-id="1310b-115">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1310b-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1310b-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1310b-116">-Profile</span></span>
<span data-ttu-id="1310b-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1310b-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1310b-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1310b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1310b-119">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1310b-119">-Type</span></span>
<span data-ttu-id="1310b-120">Specifica un tipo di utente.</span><span class="sxs-lookup"><span data-stu-id="1310b-120">Specifies a user type.</span></span>
<span data-ttu-id="1310b-121">I valori accettabili per questo parametro sono: OrgId o MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="1310b-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="1310b-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="1310b-122">-UserUpn</span></span>
<span data-ttu-id="1310b-123">Specifica il nome dell'entità utente (UPN) di un utente, ad esempio user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="1310b-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="1310b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1310b-124">CommonParameters</span></span>
<span data-ttu-id="1310b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1310b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1310b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1310b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1310b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1310b-127">INPUTS</span></span>

## <span data-ttu-id="1310b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1310b-128">OUTPUTS</span></span>

## <span data-ttu-id="1310b-129">Note</span><span class="sxs-lookup"><span data-stu-id="1310b-129">NOTES</span></span>

## <span data-ttu-id="1310b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1310b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1310b-131">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1310b-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="1310b-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="1310b-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


