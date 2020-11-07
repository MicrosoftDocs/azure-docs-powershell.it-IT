---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686505"
---
# <span data-ttu-id="79342-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="79342-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="79342-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79342-102">SYNOPSIS</span></span>
<span data-ttu-id="79342-103">Ottiene le informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="79342-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79342-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79342-104">SYNTAX</span></span>

### <span data-ttu-id="79342-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="79342-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79342-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79342-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79342-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79342-107">DESCRIPTION</span></span>
<span data-ttu-id="79342-108">Il cmdlet **Get-AzureRmMediaService** ottiene le informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="79342-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="79342-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79342-109">EXAMPLES</span></span>

### <span data-ttu-id="79342-110">Esempio 1: ottenere tutti i servizi multimediali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="79342-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="79342-111">Questo comando consente di ottenere le proprietà per tutti i servizi multimediali nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="79342-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="79342-112">Esempio 2: ottenere le proprietà del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="79342-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="79342-113">Questo comando consente di ottenere le proprietà del servizio multimediale denominato MediaService1 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="79342-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="79342-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79342-114">PARAMETERS</span></span>

### <span data-ttu-id="79342-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="79342-115">-AccountName</span></span>
<span data-ttu-id="79342-116">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79342-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79342-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79342-117">-DefaultProfile</span></span>
<span data-ttu-id="79342-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79342-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79342-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79342-119">-ResourceGroupName</span></span>
<span data-ttu-id="79342-120">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="79342-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79342-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79342-121">CommonParameters</span></span>
<span data-ttu-id="79342-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79342-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79342-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79342-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79342-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79342-124">INPUTS</span></span>

### <span data-ttu-id="79342-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79342-125">None</span></span>
<span data-ttu-id="79342-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79342-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79342-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79342-127">OUTPUTS</span></span>

### <span data-ttu-id="79342-128">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="79342-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="79342-129">Note</span><span class="sxs-lookup"><span data-stu-id="79342-129">NOTES</span></span>

## <span data-ttu-id="79342-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79342-130">RELATED LINKS</span></span>

[<span data-ttu-id="79342-131">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="79342-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="79342-132">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="79342-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="79342-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="79342-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


