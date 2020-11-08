---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030011"
---
# <span data-ttu-id="d90d0-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="d90d0-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="d90d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d90d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d90d0-103">Ottiene il contesto della risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="d90d0-103">Gets the current resource context.</span></span>

## <span data-ttu-id="d90d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d90d0-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d90d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d90d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d90d0-106">Il cmdlet **Get-AzureStorSimpleResourceContext** ottiene il contesto della risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="d90d0-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="d90d0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d90d0-107">EXAMPLES</span></span>

### <span data-ttu-id="d90d0-108">Esempio 1: ottenere il contesto corrente</span><span class="sxs-lookup"><span data-stu-id="d90d0-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="d90d0-109">Il primo comando imposta il contesto corrente come la risorsa denominata Contoso63-Tsqa usando il cmdlet **Select-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="d90d0-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="d90d0-110">Il secondo comando ottiene il contesto della risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="d90d0-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="d90d0-111">Esempio 2: tentativo di ottenere il contesto corrente</span><span class="sxs-lookup"><span data-stu-id="d90d0-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="d90d0-112">Questo comando ottiene il contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="d90d0-112">This command gets the current context.</span></span>
<span data-ttu-id="d90d0-113">In questo esempio non è stato impostato alcun contesto.</span><span class="sxs-lookup"><span data-stu-id="d90d0-113">In this example, no context has been set.</span></span>
<span data-ttu-id="d90d0-114">Il comando restituisce un messaggio che spiega il problema.</span><span class="sxs-lookup"><span data-stu-id="d90d0-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="d90d0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d90d0-115">PARAMETERS</span></span>

### <span data-ttu-id="d90d0-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="d90d0-116">-Profile</span></span>
<span data-ttu-id="d90d0-117">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="d90d0-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d90d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90d0-118">CommonParameters</span></span>
<span data-ttu-id="d90d0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90d0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d90d0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90d0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d90d0-121">INPUTS</span></span>

### <span data-ttu-id="d90d0-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d90d0-122">None</span></span>

## <span data-ttu-id="d90d0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d90d0-123">OUTPUTS</span></span>

### <span data-ttu-id="d90d0-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="d90d0-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="d90d0-125">Questo cmdlet restituisce un oggetto **ResourceContext** .</span><span class="sxs-lookup"><span data-stu-id="d90d0-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="d90d0-126">Note</span><span class="sxs-lookup"><span data-stu-id="d90d0-126">NOTES</span></span>

## <span data-ttu-id="d90d0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d90d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="d90d0-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="d90d0-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="d90d0-129">Selezionare-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="d90d0-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


