---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: 8c62bf114feee8f9b87e2b7ca35b4c67b423ed66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673862"
---
# <span data-ttu-id="3fe14-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3fe14-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="3fe14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fe14-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe14-103">Verifica se il nome di un servizio multimediale è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3fe14-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="3fe14-104">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="3fe14-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="3fe14-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fe14-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="3fe14-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fe14-106">DESCRIPTION</span></span>
<span data-ttu-id="3fe14-107">Il cmdlet **Get-AzMediaServiceNameAvailability** controlla se è disponibile un nome di servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="3fe14-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="3fe14-108">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="3fe14-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="3fe14-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fe14-109">EXAMPLES</span></span>

### <span data-ttu-id="3fe14-110">Esempio 1: verificare se il nome di un servizio multimediale è disponibile</span><span class="sxs-lookup"><span data-stu-id="3fe14-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="3fe14-111">Questo comando verifica se è disponibile il nome MediaService1.</span><span class="sxs-lookup"><span data-stu-id="3fe14-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="3fe14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fe14-112">PARAMETERS</span></span>

### <span data-ttu-id="3fe14-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3fe14-113">-AccountName</span></span>
<span data-ttu-id="3fe14-114">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe14-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3fe14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe14-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe14-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3fe14-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fe14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe14-117">CommonParameters</span></span>
<span data-ttu-id="3fe14-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe14-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe14-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe14-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fe14-120">INPUTS</span></span>

### <span data-ttu-id="3fe14-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3fe14-121">None</span></span>

## <span data-ttu-id="3fe14-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fe14-122">OUTPUTS</span></span>

### <span data-ttu-id="3fe14-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="3fe14-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="3fe14-124">Note</span><span class="sxs-lookup"><span data-stu-id="3fe14-124">NOTES</span></span>

## <span data-ttu-id="3fe14-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fe14-125">RELATED LINKS</span></span>

[<span data-ttu-id="3fe14-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe14-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="3fe14-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe14-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="3fe14-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe14-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="3fe14-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe14-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


