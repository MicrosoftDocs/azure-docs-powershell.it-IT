---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023644"
---
# <span data-ttu-id="d6463-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d6463-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="d6463-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6463-102">SYNOPSIS</span></span>
<span data-ttu-id="d6463-103">Disconnette una sessione RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6463-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="d6463-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6463-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6463-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6463-105">DESCRIPTION</span></span>
<span data-ttu-id="d6463-106">Il cmdlet **Disconnect-AzureRemoteAppSession** disconnette una sessione RemoteApp di Azure dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d6463-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="d6463-107">Il client dell'utente si disconnette dalla sessione RemoteApp di Azure, ma i programmi dell'utente continuano a essere eseguiti.</span><span class="sxs-lookup"><span data-stu-id="d6463-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="d6463-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6463-108">EXAMPLES</span></span>

### <span data-ttu-id="d6463-109">Esempio 1: disconnettere una sessione di un utente</span><span class="sxs-lookup"><span data-stu-id="d6463-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="d6463-110">Questo comando disconnette la sessione RemoteApp di Azure nella raccolta ContosoApps per l'utente il cui UPN è PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d6463-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="d6463-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6463-111">PARAMETERS</span></span>

### <span data-ttu-id="d6463-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d6463-112">-CollectionName</span></span>
<span data-ttu-id="d6463-113">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6463-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d6463-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6463-114">-Profile</span></span>
<span data-ttu-id="d6463-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6463-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6463-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d6463-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6463-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d6463-117">-UserUpn</span></span>
<span data-ttu-id="d6463-118">Specifica il nome dell'entità utente (UPN) di un utente, ad esempio PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d6463-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="d6463-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6463-119">CommonParameters</span></span>
<span data-ttu-id="d6463-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6463-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6463-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6463-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6463-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6463-122">INPUTS</span></span>

## <span data-ttu-id="d6463-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6463-123">OUTPUTS</span></span>

## <span data-ttu-id="d6463-124">Note</span><span class="sxs-lookup"><span data-stu-id="d6463-124">NOTES</span></span>

## <span data-ttu-id="d6463-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6463-125">RELATED LINKS</span></span>

[<span data-ttu-id="d6463-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d6463-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="d6463-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="d6463-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="d6463-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="d6463-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


