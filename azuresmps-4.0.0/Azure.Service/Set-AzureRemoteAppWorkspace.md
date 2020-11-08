---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029513"
---
# <span data-ttu-id="93832-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="93832-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="93832-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93832-102">SYNOPSIS</span></span>
<span data-ttu-id="93832-103">Imposta le proprietà di un'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="93832-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="93832-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93832-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="93832-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93832-105">DESCRIPTION</span></span>
<span data-ttu-id="93832-106">Il cmdlet **set-AzureRemoteAppWorkspace** imposta le proprietà di un'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="93832-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="93832-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93832-107">EXAMPLES</span></span>

### <span data-ttu-id="93832-108">Esempio 1: impostare il nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="93832-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="93832-109">Questo comando imposta il nome dell'area di lavoro RemoteApp di Azure per le applicazioni lavorative di contoso.</span><span class="sxs-lookup"><span data-stu-id="93832-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="93832-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93832-110">PARAMETERS</span></span>

### <span data-ttu-id="93832-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="93832-111">-Profile</span></span>
<span data-ttu-id="93832-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93832-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93832-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="93832-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93832-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="93832-114">-WorkspaceName</span></span>
<span data-ttu-id="93832-115">Specifica il nome dell'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="93832-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93832-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93832-116">CommonParameters</span></span>
<span data-ttu-id="93832-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93832-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93832-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93832-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93832-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93832-119">INPUTS</span></span>

## <span data-ttu-id="93832-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93832-120">OUTPUTS</span></span>

## <span data-ttu-id="93832-121">Note</span><span class="sxs-lookup"><span data-stu-id="93832-121">NOTES</span></span>
* <span data-ttu-id="93832-122">All'interno di un'area di lavoro condivisa sono presenti tutte le raccolte RemoteApp di Azure per un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="93832-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="93832-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93832-123">RELATED LINKS</span></span>

[<span data-ttu-id="93832-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="93832-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


