---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191465"
---
# <span data-ttu-id="a39ca-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a39ca-101">Get-AzMediaService</span></span>

## <span data-ttu-id="a39ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a39ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ca-103">Ottiene le informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="a39ca-103">Gets information about a media service.</span></span>

## <span data-ttu-id="a39ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a39ca-104">SYNTAX</span></span>

### <span data-ttu-id="a39ca-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39ca-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a39ca-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39ca-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a39ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a39ca-107">DESCRIPTION</span></span>
<span data-ttu-id="a39ca-108">Il cmdlet **Get-AzMediaService** ottiene le informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="a39ca-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="a39ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a39ca-109">EXAMPLES</span></span>

### <span data-ttu-id="a39ca-110">Esempio 1: ottenere tutti i servizi multimediali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a39ca-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="a39ca-111">Questo comando consente di ottenere le proprietà per tutti i servizi multimediali nel gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="a39ca-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="a39ca-112">Esempio 2: ottenere le proprietà del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="a39ca-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="a39ca-113">Questo comando consente di ottenere le proprietà del servizio multimediale denominato MediaService1 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="a39ca-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="a39ca-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a39ca-114">PARAMETERS</span></span>

### <span data-ttu-id="a39ca-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a39ca-115">-AccountName</span></span>
<span data-ttu-id="a39ca-116">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39ca-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ca-117">-DefaultProfile</span></span>
<span data-ttu-id="a39ca-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a39ca-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="a39ca-120">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="a39ca-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ca-121">CommonParameters</span></span>
<span data-ttu-id="a39ca-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ca-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a39ca-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ca-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a39ca-124">INPUTS</span></span>

### <span data-ttu-id="a39ca-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a39ca-125">System.String</span></span>

## <span data-ttu-id="a39ca-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a39ca-126">OUTPUTS</span></span>

### <span data-ttu-id="a39ca-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="a39ca-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="a39ca-128">Note</span><span class="sxs-lookup"><span data-stu-id="a39ca-128">NOTES</span></span>

## <span data-ttu-id="a39ca-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a39ca-129">RELATED LINKS</span></span>

[<span data-ttu-id="a39ca-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a39ca-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="a39ca-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a39ca-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="a39ca-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a39ca-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


