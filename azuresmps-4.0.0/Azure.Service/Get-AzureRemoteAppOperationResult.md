---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029784"
---
# <span data-ttu-id="dc1af-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="dc1af-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="dc1af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc1af-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1af-103">Recupera il risultato di un'operazione RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1af-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="dc1af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc1af-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc1af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc1af-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1af-106">Il cmdlet **Get-AzureRemoteAppOperationResult** Recupera il risultato di un'operazione RemoteApp di Azure a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="dc1af-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="dc1af-107">Azure RemoteApp USA operazioni a esecuzione prolungata per molte azioni che richiedono l'elaborazione da parte del servizio e non possono tornare immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dc1af-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="dc1af-108">Esempi di cmdlet che restituiscono gli ID di rilevamento includono **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** e altri.</span><span class="sxs-lookup"><span data-stu-id="dc1af-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="dc1af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc1af-109">EXAMPLES</span></span>

### <span data-ttu-id="dc1af-110">Esempio 1: usare un ID di rilevamento per ottenere un risultato dell'operazione</span><span class="sxs-lookup"><span data-stu-id="dc1af-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="dc1af-111">Questo comando Salva l'ID di rilevamento restituito da un'operazione RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1af-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="dc1af-112">L'ID di rilevamento viene passato a **Get-AzureRemoteAppOperationResult** nel comando seguente.</span><span class="sxs-lookup"><span data-stu-id="dc1af-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="dc1af-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc1af-113">PARAMETERS</span></span>

### <span data-ttu-id="dc1af-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc1af-114">-Profile</span></span>
<span data-ttu-id="dc1af-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc1af-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc1af-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="dc1af-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc1af-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="dc1af-117">-TrackingId</span></span>
<span data-ttu-id="dc1af-118">Specifica l'ID di rilevamento di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc1af-118">Specifies the tracking ID of an operation.</span></span>

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

### <span data-ttu-id="dc1af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1af-119">CommonParameters</span></span>
<span data-ttu-id="dc1af-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1af-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1af-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc1af-122">INPUTS</span></span>

## <span data-ttu-id="dc1af-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc1af-123">OUTPUTS</span></span>

## <span data-ttu-id="dc1af-124">Note</span><span class="sxs-lookup"><span data-stu-id="dc1af-124">NOTES</span></span>

## <span data-ttu-id="dc1af-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc1af-125">RELATED LINKS</span></span>

[<span data-ttu-id="dc1af-126">Disconnetti-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="dc1af-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="dc1af-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc1af-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="dc1af-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="dc1af-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


