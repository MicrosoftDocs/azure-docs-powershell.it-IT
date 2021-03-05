---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006622"
---
# <span data-ttu-id="b02b7-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b02b7-101">Get-AzMediaService</span></span>

## <span data-ttu-id="b02b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b02b7-103">Ottiene informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b02b7-103">Gets information about a media service.</span></span>

## <span data-ttu-id="b02b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b02b7-104">SYNTAX</span></span>

### <span data-ttu-id="b02b7-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02b7-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b02b7-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b02b7-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b02b7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b02b7-107">DESCRIPTION</span></span>
<span data-ttu-id="b02b7-108">Il cmdlet **Get-AzMediaService** ottiene informazioni su un servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b02b7-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="b02b7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b02b7-109">EXAMPLES</span></span>

### <span data-ttu-id="b02b7-110">Esempio 1: Ottenere tutti i servizi multimediali in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b02b7-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="b02b7-111">Questo comando recupera le proprietà per tutti i servizi multimediali del gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="b02b7-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="b02b7-112">Esempio 2: Ottenere le proprietà del servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="b02b7-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="b02b7-113">Questo comando ottiene le proprietà del servizio multimediale denominato MediaService1 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="b02b7-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="b02b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02b7-114">PARAMETERS</span></span>

### <span data-ttu-id="b02b7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b02b7-115">-AccountName</span></span>
<span data-ttu-id="b02b7-116">Specifica il nome del servizio multimediale che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b02b7-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b02b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02b7-117">-DefaultProfile</span></span>
<span data-ttu-id="b02b7-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b02b7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b02b7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02b7-119">-ResourceGroupName</span></span>
<span data-ttu-id="b02b7-120">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b02b7-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b02b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02b7-121">CommonParameters</span></span>
<span data-ttu-id="b02b7-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02b7-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b02b7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02b7-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="b02b7-124">INPUTS</span></span>

### <span data-ttu-id="b02b7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b02b7-125">System.String</span></span>

## <span data-ttu-id="b02b7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b02b7-126">OUTPUTS</span></span>

### <span data-ttu-id="b02b7-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b02b7-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b02b7-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="b02b7-128">NOTES</span></span>

## <span data-ttu-id="b02b7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b02b7-129">RELATED LINKS</span></span>

[<span data-ttu-id="b02b7-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b02b7-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="b02b7-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b02b7-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="b02b7-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b02b7-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


