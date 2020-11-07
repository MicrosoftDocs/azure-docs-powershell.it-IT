---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860682"
---
# <span data-ttu-id="ffd68-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ffd68-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="ffd68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ffd68-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd68-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="ffd68-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="ffd68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffd68-104">SYNTAX</span></span>

### <span data-ttu-id="ffd68-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="ffd68-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffd68-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="ffd68-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffd68-107">DESCRIPTION</span></span>
<span data-ttu-id="ffd68-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ffd68-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ffd68-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffd68-109">EXAMPLES</span></span>

### <span data-ttu-id="ffd68-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ffd68-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ffd68-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ffd68-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ffd68-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ffd68-112">PARAMETERS</span></span>

### <span data-ttu-id="ffd68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd68-113">-DefaultProfile</span></span>
<span data-ttu-id="ffd68-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd68-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffd68-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ffd68-115">-ExpandResource</span></span>
<span data-ttu-id="ffd68-116">Riferimento alla risorsa da espandere.</span><span class="sxs-lookup"><span data-stu-id="ffd68-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="ffd68-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffd68-117">-Name</span></span>
<span data-ttu-id="ffd68-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ffd68-118">The resource name.</span></span>

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

### <span data-ttu-id="ffd68-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd68-119">-ResourceGroupName</span></span>
<span data-ttu-id="ffd68-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ffd68-120">The resource group name.</span></span>

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

### <span data-ttu-id="ffd68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd68-121">CommonParameters</span></span>
<span data-ttu-id="ffd68-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd68-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd68-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd68-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ffd68-124">INPUTS</span></span>

### <span data-ttu-id="ffd68-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd68-125">System.String</span></span>

## <span data-ttu-id="ffd68-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffd68-126">OUTPUTS</span></span>

### <span data-ttu-id="ffd68-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ffd68-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ffd68-128">Note</span><span class="sxs-lookup"><span data-stu-id="ffd68-128">NOTES</span></span>

## <span data-ttu-id="ffd68-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffd68-129">RELATED LINKS</span></span>

