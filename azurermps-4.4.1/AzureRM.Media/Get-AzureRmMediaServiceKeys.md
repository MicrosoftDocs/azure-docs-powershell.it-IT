---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688277"
---
# <span data-ttu-id="b892a-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b892a-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="b892a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b892a-102">SYNOPSIS</span></span>
<span data-ttu-id="b892a-103">Ottiene le informazioni chiave per l'accesso all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b892a-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b892a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b892a-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b892a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b892a-105">DESCRIPTION</span></span>
<span data-ttu-id="b892a-106">Il cmdlet **Get-AzureRmMediaServiceKeys** ottiene le informazioni chiave per l'accesso all'endpoint REST (Representational State Transfer) associato al servizio di Azure Media.</span><span class="sxs-lookup"><span data-stu-id="b892a-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="b892a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b892a-107">EXAMPLES</span></span>

### <span data-ttu-id="b892a-108">Esempio 1: ottenere le informazioni chiave per l'accesso al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="b892a-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="b892a-109">Questo comando consente di ottenere le informazioni chiave per l'accesso al servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="b892a-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="b892a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b892a-110">PARAMETERS</span></span>

### <span data-ttu-id="b892a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b892a-111">-AccountName</span></span>
<span data-ttu-id="b892a-112">Specifica il nome del servizio multimediale da cui questo cmdlet ottiene i tasti del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b892a-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b892a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b892a-113">-ResourceGroupName</span></span>
<span data-ttu-id="b892a-114">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="b892a-114">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b892a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b892a-115">-DefaultProfile</span></span>
<span data-ttu-id="b892a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b892a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b892a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b892a-117">CommonParameters</span></span>
<span data-ttu-id="b892a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b892a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b892a-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b892a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b892a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b892a-120">INPUTS</span></span>

## <span data-ttu-id="b892a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b892a-121">OUTPUTS</span></span>

### <span data-ttu-id="b892a-122">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="b892a-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="b892a-123">Note</span><span class="sxs-lookup"><span data-stu-id="b892a-123">NOTES</span></span>

## <span data-ttu-id="b892a-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b892a-124">RELATED LINKS</span></span>

[<span data-ttu-id="b892a-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="b892a-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


