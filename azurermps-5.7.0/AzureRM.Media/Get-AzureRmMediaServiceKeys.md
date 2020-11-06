---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 368423076003b03524272977ff8721db57721232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515644"
---
# <span data-ttu-id="09195-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="09195-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="09195-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09195-102">SYNOPSIS</span></span>
<span data-ttu-id="09195-103">Ottiene le informazioni chiave per l'accesso all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="09195-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09195-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09195-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09195-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09195-105">DESCRIPTION</span></span>
<span data-ttu-id="09195-106">Il cmdlet **Get-AzureRmMediaServiceKeys** ottiene le informazioni chiave per l'accesso all'endpoint REST (Representational State Transfer) associato al servizio di Azure Media.</span><span class="sxs-lookup"><span data-stu-id="09195-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="09195-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09195-107">EXAMPLES</span></span>

### <span data-ttu-id="09195-108">Esempio 1: ottenere le informazioni chiave per l'accesso al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="09195-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="09195-109">Questo comando consente di ottenere le informazioni chiave per l'accesso al servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="09195-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="09195-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09195-110">PARAMETERS</span></span>

### <span data-ttu-id="09195-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09195-111">-AccountName</span></span>
<span data-ttu-id="09195-112">Specifica il nome del servizio multimediale da cui questo cmdlet ottiene i tasti del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="09195-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09195-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09195-113">-DefaultProfile</span></span>
<span data-ttu-id="09195-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09195-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09195-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09195-115">-ResourceGroupName</span></span>
<span data-ttu-id="09195-116">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="09195-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="09195-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09195-117">CommonParameters</span></span>
<span data-ttu-id="09195-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09195-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09195-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09195-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09195-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09195-120">INPUTS</span></span>

### <span data-ttu-id="09195-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09195-121">None</span></span>
<span data-ttu-id="09195-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="09195-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09195-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09195-123">OUTPUTS</span></span>

### <span data-ttu-id="09195-124">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="09195-124">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="09195-125">Note</span><span class="sxs-lookup"><span data-stu-id="09195-125">NOTES</span></span>

## <span data-ttu-id="09195-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09195-126">RELATED LINKS</span></span>

[<span data-ttu-id="09195-127">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="09195-127">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


