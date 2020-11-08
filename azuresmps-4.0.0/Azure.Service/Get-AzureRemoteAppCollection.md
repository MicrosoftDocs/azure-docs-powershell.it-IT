---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029791"
---
# <span data-ttu-id="71bec-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="71bec-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="71bec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71bec-102">SYNOPSIS</span></span>
<span data-ttu-id="71bec-103">Recupera informazioni su una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="71bec-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="71bec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71bec-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71bec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71bec-105">DESCRIPTION</span></span>
<span data-ttu-id="71bec-106">Il cmdlet **Get-AzureRemoteAppCollection** recupera informazioni sulle raccolte RemoteApp di Azure in Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71bec-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="71bec-107">Restituisce un oggetto con informazioni su una raccolta specifica o se non è specificata alcuna raccolta, per tutte le raccolte della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="71bec-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="71bec-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71bec-108">EXAMPLES</span></span>

### <span data-ttu-id="71bec-109">Esempio 1: ottenere un elenco di tutte le raccolte</span><span class="sxs-lookup"><span data-stu-id="71bec-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="71bec-110">Questo comando restituisce un elenco di tutte le raccolte RemoteApp di Azure nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="71bec-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="71bec-111">Esempio 2: ottenere informazioni su una raccolta specificata</span><span class="sxs-lookup"><span data-stu-id="71bec-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="71bec-112">Questo comando restituisce informazioni sulla raccolta RemoteApp di Azure denominata ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="71bec-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="71bec-113">Esempio 3: ottenere un elenco di raccolte usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="71bec-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="71bec-114">Questo comando restituisce un elenco di tutte le raccolte RemoteApp di Azure che corrispondono a Finance \*.</span><span class="sxs-lookup"><span data-stu-id="71bec-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="71bec-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71bec-115">PARAMETERS</span></span>

### <span data-ttu-id="71bec-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="71bec-116">-CollectionName</span></span>
<span data-ttu-id="71bec-117">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="71bec-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="71bec-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="71bec-118">-Profile</span></span>
<span data-ttu-id="71bec-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71bec-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71bec-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="71bec-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71bec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bec-121">CommonParameters</span></span>
<span data-ttu-id="71bec-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71bec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bec-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71bec-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bec-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71bec-124">INPUTS</span></span>

## <span data-ttu-id="71bec-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71bec-125">OUTPUTS</span></span>

## <span data-ttu-id="71bec-126">Note</span><span class="sxs-lookup"><span data-stu-id="71bec-126">NOTES</span></span>

## <span data-ttu-id="71bec-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71bec-127">RELATED LINKS</span></span>

[<span data-ttu-id="71bec-128">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="71bec-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="71bec-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="71bec-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="71bec-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="71bec-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="71bec-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="71bec-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


