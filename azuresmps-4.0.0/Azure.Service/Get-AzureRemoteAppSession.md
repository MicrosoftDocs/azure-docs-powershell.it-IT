---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030039"
---
# <span data-ttu-id="5e851-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="5e851-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="5e851-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e851-102">SYNOPSIS</span></span>
<span data-ttu-id="5e851-103">Elenca tutte le sessioni RemoteApp di Azure attive e disconnesse per una raccolta.</span><span class="sxs-lookup"><span data-stu-id="5e851-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="5e851-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e851-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e851-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e851-105">DESCRIPTION</span></span>
<span data-ttu-id="5e851-106">Il cmdlet **Get-AzureRemoteAppSession** elenca tutte le sessioni RemoteApp di Azure attive e disconnesse per una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e851-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5e851-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e851-107">EXAMPLES</span></span>

### <span data-ttu-id="5e851-108">Esempio 1: elencare tutte le sessioni in una raccolta</span><span class="sxs-lookup"><span data-stu-id="5e851-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="5e851-109">Questo comando elenca tutte le sessioni della raccolta RemoteApp di Azure denominata ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="5e851-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="5e851-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e851-110">PARAMETERS</span></span>

### <span data-ttu-id="5e851-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5e851-111">-CollectionName</span></span>
<span data-ttu-id="5e851-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e851-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="5e851-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="5e851-113">-Profile</span></span>
<span data-ttu-id="5e851-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e851-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e851-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5e851-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e851-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="5e851-116">-UserUpn</span></span>
<span data-ttu-id="5e851-117">Specifica il nome dell'entità utente (UPN) di un utente per cui ottenere sessioni RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e851-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="5e851-118">Ad esempio, l'UPN può avere il formato seguente: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="5e851-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="5e851-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e851-119">CommonParameters</span></span>
<span data-ttu-id="5e851-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e851-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e851-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e851-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e851-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e851-122">INPUTS</span></span>

## <span data-ttu-id="5e851-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e851-123">OUTPUTS</span></span>

## <span data-ttu-id="5e851-124">Note</span><span class="sxs-lookup"><span data-stu-id="5e851-124">NOTES</span></span>

## <span data-ttu-id="5e851-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e851-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e851-126">Disconnetti-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="5e851-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="5e851-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="5e851-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="5e851-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="5e851-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


