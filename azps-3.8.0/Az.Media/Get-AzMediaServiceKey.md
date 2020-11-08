---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022494"
---
# <span data-ttu-id="8897b-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8897b-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="8897b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8897b-102">SYNOPSIS</span></span>
<span data-ttu-id="8897b-103">Ottiene le informazioni chiave per l'accesso all'endpoint REST associato al servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8897b-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="8897b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8897b-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8897b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8897b-105">DESCRIPTION</span></span>
<span data-ttu-id="8897b-106">Il cmdlet **Get-AzMediaServiceKey** ottiene le informazioni chiave per l'accesso all'endpoint REST (Representational State Transfer) associato al servizio di Azure Media.</span><span class="sxs-lookup"><span data-stu-id="8897b-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="8897b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8897b-107">EXAMPLES</span></span>

### <span data-ttu-id="8897b-108">Esempio 1: ottenere le informazioni chiave per l'accesso al servizio multimediale</span><span class="sxs-lookup"><span data-stu-id="8897b-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="8897b-109">Questo comando consente di ottenere le informazioni chiave per l'accesso al servizio multimediale denominato MediaService001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="8897b-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="8897b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8897b-110">PARAMETERS</span></span>

### <span data-ttu-id="8897b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8897b-111">-AccountName</span></span>
<span data-ttu-id="8897b-112">Specifica il nome del servizio multimediale da cui questo cmdlet ottiene i tasti del servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8897b-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="8897b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8897b-113">-DefaultProfile</span></span>
<span data-ttu-id="8897b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8897b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8897b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8897b-115">-ResourceGroupName</span></span>
<span data-ttu-id="8897b-116">Specifica il nome del gruppo di risorse che contiene il servizio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8897b-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="8897b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8897b-117">CommonParameters</span></span>
<span data-ttu-id="8897b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8897b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8897b-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8897b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8897b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8897b-120">INPUTS</span></span>

### <span data-ttu-id="8897b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8897b-121">System.String</span></span>

## <span data-ttu-id="8897b-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8897b-122">OUTPUTS</span></span>

### <span data-ttu-id="8897b-123">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="8897b-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="8897b-124">Note</span><span class="sxs-lookup"><span data-stu-id="8897b-124">NOTES</span></span>

## <span data-ttu-id="8897b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8897b-125">RELATED LINKS</span></span>

[<span data-ttu-id="8897b-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="8897b-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


