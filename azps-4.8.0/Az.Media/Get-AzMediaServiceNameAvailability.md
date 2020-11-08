---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191460"
---
# <span data-ttu-id="f394e-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f394e-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="f394e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f394e-102">SYNOPSIS</span></span>
<span data-ttu-id="f394e-103">Verifica se il nome di un servizio multimediale è disponibile.</span><span class="sxs-lookup"><span data-stu-id="f394e-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="f394e-104">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="f394e-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="f394e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f394e-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="f394e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f394e-106">DESCRIPTION</span></span>
<span data-ttu-id="f394e-107">Il cmdlet **Get-AzMediaServiceNameAvailability** controlla se è disponibile un nome di servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="f394e-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="f394e-108">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="f394e-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="f394e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f394e-109">EXAMPLES</span></span>

### <span data-ttu-id="f394e-110">Esempio 1: verificare se il nome di un servizio multimediale è disponibile</span><span class="sxs-lookup"><span data-stu-id="f394e-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="f394e-111">Questo comando verifica se è disponibile il nome MediaService1.</span><span class="sxs-lookup"><span data-stu-id="f394e-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="f394e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f394e-112">PARAMETERS</span></span>

### <span data-ttu-id="f394e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f394e-113">-AccountName</span></span>
<span data-ttu-id="f394e-114">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f394e-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f394e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f394e-115">-DefaultProfile</span></span>
<span data-ttu-id="f394e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f394e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f394e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f394e-117">CommonParameters</span></span>
<span data-ttu-id="f394e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f394e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f394e-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f394e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f394e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f394e-120">INPUTS</span></span>

### <span data-ttu-id="f394e-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f394e-121">None</span></span>

## <span data-ttu-id="f394e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f394e-122">OUTPUTS</span></span>

### <span data-ttu-id="f394e-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="f394e-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="f394e-124">Note</span><span class="sxs-lookup"><span data-stu-id="f394e-124">NOTES</span></span>

## <span data-ttu-id="f394e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f394e-125">RELATED LINKS</span></span>

[<span data-ttu-id="f394e-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f394e-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="f394e-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f394e-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="f394e-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f394e-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f394e-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f394e-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

