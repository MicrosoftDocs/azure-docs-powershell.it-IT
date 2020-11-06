---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 2c980b981679ddfa3fb2eda473b495f9281c227d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511111"
---
# <span data-ttu-id="ae601-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ae601-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="ae601-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae601-102">SYNOPSIS</span></span>
<span data-ttu-id="ae601-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="ae601-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae601-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae601-104">SYNTAX</span></span>

### <span data-ttu-id="ae601-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ae601-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae601-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="ae601-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae601-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae601-107">DESCRIPTION</span></span>
<span data-ttu-id="ae601-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ae601-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ae601-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae601-109">EXAMPLES</span></span>

### <span data-ttu-id="ae601-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae601-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ae601-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ae601-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ae601-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae601-112">PARAMETERS</span></span>

### <span data-ttu-id="ae601-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae601-113">-DefaultProfile</span></span>
<span data-ttu-id="ae601-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae601-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae601-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ae601-115">-ExpandResource</span></span>
<span data-ttu-id="ae601-116">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="ae601-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae601-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae601-117">-Name</span></span>
<span data-ttu-id="ae601-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae601-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae601-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae601-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae601-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae601-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae601-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae601-121">CommonParameters</span></span>
<span data-ttu-id="ae601-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae601-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae601-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae601-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae601-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae601-124">INPUTS</span></span>

### <span data-ttu-id="ae601-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ae601-125">System.String</span></span>

## <span data-ttu-id="ae601-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae601-126">OUTPUTS</span></span>

### <span data-ttu-id="ae601-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ae601-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ae601-128">Note</span><span class="sxs-lookup"><span data-stu-id="ae601-128">NOTES</span></span>

## <span data-ttu-id="ae601-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae601-129">RELATED LINKS</span></span>
