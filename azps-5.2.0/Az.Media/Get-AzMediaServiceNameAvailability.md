---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344887"
---
# <span data-ttu-id="98631-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="98631-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="98631-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98631-102">SYNOPSIS</span></span>
<span data-ttu-id="98631-103">Verifica se il nome di un servizio multimediale è disponibile.</span><span class="sxs-lookup"><span data-stu-id="98631-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="98631-104">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="98631-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="98631-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98631-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="98631-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98631-106">DESCRIPTION</span></span>
<span data-ttu-id="98631-107">Il cmdlet **Get-AzMediaServiceNameAvailability** controlla se è disponibile un nome di servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="98631-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="98631-108">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="98631-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="98631-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98631-109">EXAMPLES</span></span>

### <span data-ttu-id="98631-110">Esempio 1: verificare se il nome di un servizio multimediale è disponibile</span><span class="sxs-lookup"><span data-stu-id="98631-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="98631-111">Questo comando verifica se è disponibile il nome MediaService1.</span><span class="sxs-lookup"><span data-stu-id="98631-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="98631-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98631-112">PARAMETERS</span></span>

### <span data-ttu-id="98631-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="98631-113">-AccountName</span></span>
<span data-ttu-id="98631-114">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98631-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="98631-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98631-115">-DefaultProfile</span></span>
<span data-ttu-id="98631-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98631-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98631-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98631-117">CommonParameters</span></span>
<span data-ttu-id="98631-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98631-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98631-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98631-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98631-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98631-120">INPUTS</span></span>

### <span data-ttu-id="98631-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="98631-121">None</span></span>

## <span data-ttu-id="98631-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98631-122">OUTPUTS</span></span>

### <span data-ttu-id="98631-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="98631-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="98631-124">Note</span><span class="sxs-lookup"><span data-stu-id="98631-124">NOTES</span></span>

## <span data-ttu-id="98631-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98631-125">RELATED LINKS</span></span>

[<span data-ttu-id="98631-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="98631-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="98631-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="98631-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="98631-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="98631-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="98631-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="98631-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


