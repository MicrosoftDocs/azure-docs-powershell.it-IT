---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687163"
---
# <span data-ttu-id="10d16-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="10d16-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="10d16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10d16-102">SYNOPSIS</span></span>
<span data-ttu-id="10d16-103">Verifica se il nome di un servizio multimediale è disponibile.</span><span class="sxs-lookup"><span data-stu-id="10d16-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="10d16-104">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="10d16-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d16-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10d16-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="10d16-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10d16-106">DESCRIPTION</span></span>
<span data-ttu-id="10d16-107">Il cmdlet **Get-AzureRmMediaServiceNameAvailability** controlla se è disponibile un nome di servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="10d16-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="10d16-108">I nomi dei servizi multimediali sono univoci globalmente.</span><span class="sxs-lookup"><span data-stu-id="10d16-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="10d16-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10d16-109">EXAMPLES</span></span>

### <span data-ttu-id="10d16-110">Esempio 1: verificare se il nome di un servizio multimediale è disponibile</span><span class="sxs-lookup"><span data-stu-id="10d16-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="10d16-111">Questo comando verifica se è disponibile il nome MediaService1.</span><span class="sxs-lookup"><span data-stu-id="10d16-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="10d16-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10d16-112">PARAMETERS</span></span>

### <span data-ttu-id="10d16-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="10d16-113">-AccountName</span></span>
<span data-ttu-id="10d16-114">Specifica il nome del servizio multimediale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d16-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="10d16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d16-115">-DefaultProfile</span></span>
<span data-ttu-id="10d16-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10d16-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d16-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d16-117">CommonParameters</span></span>
<span data-ttu-id="10d16-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d16-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d16-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d16-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d16-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10d16-120">INPUTS</span></span>

## <span data-ttu-id="10d16-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10d16-121">OUTPUTS</span></span>

### <span data-ttu-id="10d16-122">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="10d16-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="10d16-123">Note</span><span class="sxs-lookup"><span data-stu-id="10d16-123">NOTES</span></span>

## <span data-ttu-id="10d16-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10d16-124">RELATED LINKS</span></span>

[<span data-ttu-id="10d16-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="10d16-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="10d16-126">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="10d16-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="10d16-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="10d16-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="10d16-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="10d16-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


