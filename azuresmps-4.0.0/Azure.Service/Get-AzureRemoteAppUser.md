---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029778"
---
# <span data-ttu-id="2de9d-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="2de9d-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="2de9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2de9d-102">SYNOPSIS</span></span>
<span data-ttu-id="2de9d-103">Elenca gli utenti in una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="2de9d-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2de9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2de9d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2de9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2de9d-105">DESCRIPTION</span></span>
<span data-ttu-id="2de9d-106">Il cmdlet **Get-AzureRemoteAppUser** elenca gli utenti in una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="2de9d-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2de9d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2de9d-107">EXAMPLES</span></span>

### <span data-ttu-id="2de9d-108">Esempio 1: elencare gli utenti di una raccolta</span><span class="sxs-lookup"><span data-stu-id="2de9d-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="2de9d-109">Questo comando elenca gli utenti che hanno accesso alla raccolta RemoteApp di Azure denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="2de9d-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="2de9d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2de9d-110">PARAMETERS</span></span>

### <span data-ttu-id="2de9d-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="2de9d-111">-Alias</span></span>
<span data-ttu-id="2de9d-112">Specifica un alias di programma pubblicato.</span><span class="sxs-lookup"><span data-stu-id="2de9d-112">Specifies a published program alias.</span></span>
<span data-ttu-id="2de9d-113">Puoi usare questo parametro solo in modalità di pubblicazione per-app.</span><span class="sxs-lookup"><span data-stu-id="2de9d-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="2de9d-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="2de9d-114">-CollectionName</span></span>
<span data-ttu-id="2de9d-115">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="2de9d-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="2de9d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="2de9d-116">-Profile</span></span>
<span data-ttu-id="2de9d-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2de9d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2de9d-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2de9d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2de9d-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="2de9d-119">-UserUpn</span></span>
<span data-ttu-id="2de9d-120">Specifica il nome dell'entità utente (UPN) di un utente per cui elencare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="2de9d-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="2de9d-121">Ad esempio, PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="2de9d-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="2de9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de9d-122">CommonParameters</span></span>
<span data-ttu-id="2de9d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de9d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de9d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de9d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2de9d-125">INPUTS</span></span>

## <span data-ttu-id="2de9d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2de9d-126">OUTPUTS</span></span>

## <span data-ttu-id="2de9d-127">Note</span><span class="sxs-lookup"><span data-stu-id="2de9d-127">NOTES</span></span>

## <span data-ttu-id="2de9d-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2de9d-128">RELATED LINKS</span></span>

[<span data-ttu-id="2de9d-129">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="2de9d-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="2de9d-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="2de9d-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="2de9d-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="2de9d-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


