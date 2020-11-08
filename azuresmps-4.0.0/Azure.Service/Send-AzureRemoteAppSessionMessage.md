---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029895"
---
# <span data-ttu-id="76ba9-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="76ba9-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="76ba9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="76ba9-103">Invia un messaggio a un utente.</span><span class="sxs-lookup"><span data-stu-id="76ba9-103">Sends a message to a user.</span></span>

## <span data-ttu-id="76ba9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76ba9-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="76ba9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76ba9-105">DESCRIPTION</span></span>
<span data-ttu-id="76ba9-106">Il cmdlet **Send-AzureRemoteAppSessionMessage** Invia un messaggio a un utente connesso a una sessione RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ba9-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="76ba9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76ba9-107">EXAMPLES</span></span>

### <span data-ttu-id="76ba9-108">Esempio 1: inviare un messaggio a un utente</span><span class="sxs-lookup"><span data-stu-id="76ba9-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="76ba9-109">Questo comando Invia un messaggio all'utente il cui UPN è PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="76ba9-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="76ba9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76ba9-110">PARAMETERS</span></span>

### <span data-ttu-id="76ba9-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="76ba9-111">-CollectionName</span></span>
<span data-ttu-id="76ba9-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="76ba9-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="76ba9-113">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="76ba9-113">-Message</span></span>
<span data-ttu-id="76ba9-114">Specifica il messaggio da inviare.</span><span class="sxs-lookup"><span data-stu-id="76ba9-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ba9-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="76ba9-115">-Profile</span></span>
<span data-ttu-id="76ba9-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76ba9-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76ba9-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="76ba9-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76ba9-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="76ba9-118">-UserUpn</span></span>
<span data-ttu-id="76ba9-119">Specifica il nome dell'entità utente (UPN) di un utente, ad esempio PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="76ba9-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76ba9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76ba9-120">CommonParameters</span></span>
<span data-ttu-id="76ba9-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76ba9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76ba9-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76ba9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76ba9-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76ba9-123">INPUTS</span></span>

## <span data-ttu-id="76ba9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76ba9-124">OUTPUTS</span></span>

## <span data-ttu-id="76ba9-125">Note</span><span class="sxs-lookup"><span data-stu-id="76ba9-125">NOTES</span></span>

## <span data-ttu-id="76ba9-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76ba9-126">RELATED LINKS</span></span>

[<span data-ttu-id="76ba9-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="76ba9-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="76ba9-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="76ba9-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="76ba9-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="76ba9-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


