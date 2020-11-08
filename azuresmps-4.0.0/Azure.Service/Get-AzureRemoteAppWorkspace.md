---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023577"
---
# <span data-ttu-id="1cc93-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cc93-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="1cc93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1cc93-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc93-103">Recupera informazioni su un'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc93-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1cc93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc93-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1cc93-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cc93-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc93-106">Il cmdlet **Get-AzureRemoteAppWorkspace** recupera le informazioni su un'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc93-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1cc93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc93-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc93-108">Esempio 1: recuperare informazioni su un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1cc93-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="1cc93-109">Questo comando recupera le informazioni sull'area di lavoro RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc93-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="1cc93-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1cc93-110">PARAMETERS</span></span>

### <span data-ttu-id="1cc93-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="1cc93-111">-Profile</span></span>
<span data-ttu-id="1cc93-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc93-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1cc93-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1cc93-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1cc93-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc93-114">CommonParameters</span></span>
<span data-ttu-id="1cc93-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc93-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc93-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc93-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc93-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1cc93-117">INPUTS</span></span>

## <span data-ttu-id="1cc93-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc93-118">OUTPUTS</span></span>

## <span data-ttu-id="1cc93-119">Note</span><span class="sxs-lookup"><span data-stu-id="1cc93-119">NOTES</span></span>

## <span data-ttu-id="1cc93-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc93-120">RELATED LINKS</span></span>

[<span data-ttu-id="1cc93-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cc93-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


