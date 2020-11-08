---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023512"
---
# <span data-ttu-id="97ea9-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="97ea9-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="97ea9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="97ea9-103">Ottiene tutte le risorse create.</span><span class="sxs-lookup"><span data-stu-id="97ea9-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="97ea9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97ea9-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97ea9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97ea9-105">DESCRIPTION</span></span>
<span data-ttu-id="97ea9-106">Il cmdlet **Get-AzureStorSimpleResource** ottiene tutte le risorse create con Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="97ea9-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="97ea9-107">Il cmdlet ottiene i dettagli che è possibile usare per connettersi alle risorse.</span><span class="sxs-lookup"><span data-stu-id="97ea9-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="97ea9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97ea9-108">EXAMPLES</span></span>

### <span data-ttu-id="97ea9-109">Esempio 1: ottenere tutte le risorse</span><span class="sxs-lookup"><span data-stu-id="97ea9-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="97ea9-110">Questo comando consente di ottenere tutte le risorse create.</span><span class="sxs-lookup"><span data-stu-id="97ea9-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="97ea9-111">In questo esempio sono disponibili tre risorse.</span><span class="sxs-lookup"><span data-stu-id="97ea9-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="97ea9-112">Esempio 2: ottenere una risorsa usando il relativo nome</span><span class="sxs-lookup"><span data-stu-id="97ea9-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="97ea9-113">Questo comando consente di ottenere la risorsa denominata Contoso63-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="97ea9-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="97ea9-114">Esempio 3: tentativo di ottenere una risorsa inesistente</span><span class="sxs-lookup"><span data-stu-id="97ea9-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="97ea9-115">Questo comando tenta di ottenere la risorsa denominata Contoso64-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="97ea9-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="97ea9-116">Non esiste una risorsa con questo nome.</span><span class="sxs-lookup"><span data-stu-id="97ea9-116">There is no resource that has this name.</span></span>
<span data-ttu-id="97ea9-117">Questo esempio non restituisce alcuna risorsa.</span><span class="sxs-lookup"><span data-stu-id="97ea9-117">This example does not return any resource.</span></span>

## <span data-ttu-id="97ea9-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97ea9-118">PARAMETERS</span></span>

### <span data-ttu-id="97ea9-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="97ea9-119">-Profile</span></span>
<span data-ttu-id="97ea9-120">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="97ea9-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="97ea9-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="97ea9-121">-ResourceName</span></span>
<span data-ttu-id="97ea9-122">Specifica il nome della risorsa ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97ea9-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ea9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ea9-123">CommonParameters</span></span>
<span data-ttu-id="97ea9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ea9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ea9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ea9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ea9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97ea9-126">INPUTS</span></span>

### <span data-ttu-id="97ea9-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97ea9-127">None</span></span>

## <span data-ttu-id="97ea9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97ea9-128">OUTPUTS</span></span>

### <span data-ttu-id="97ea9-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="97ea9-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="97ea9-130">Questo cmdlet restituisce gli oggetti **ResourceCredentials** che contengono le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="97ea9-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="97ea9-131">**ResourceName**</span><span class="sxs-lookup"><span data-stu-id="97ea9-131">**ResourceName**</span></span>
- <span data-ttu-id="97ea9-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="97ea9-132">**ResouceId**</span></span>
- <span data-ttu-id="97ea9-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="97ea9-133">**ResourceState**</span></span>

## <span data-ttu-id="97ea9-134">Note</span><span class="sxs-lookup"><span data-stu-id="97ea9-134">NOTES</span></span>

## <span data-ttu-id="97ea9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97ea9-135">RELATED LINKS</span></span>

[<span data-ttu-id="97ea9-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="97ea9-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="97ea9-137">Selezionare-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="97ea9-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


