---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685934"
---
# <span data-ttu-id="0f545-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f545-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="0f545-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f545-102">SYNOPSIS</span></span>
<span data-ttu-id="0f545-103">Ottiene un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0f545-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f545-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f545-104">SYNTAX</span></span>

### <span data-ttu-id="0f545-105">Predefinita</span><span class="sxs-lookup"><span data-stu-id="0f545-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f545-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f545-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f545-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f545-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f545-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f545-108">DESCRIPTION</span></span>
<span data-ttu-id="0f545-109">Il cmdlet **Get-AzureRmPublicIpPrefix** ottiene uno o più prefissi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f545-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="0f545-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f545-110">EXAMPLES</span></span>

### <span data-ttu-id="0f545-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f545-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="0f545-112">Questo comando ottiene una risorsa prefisso IP pubblico con $prefixName nel gruppo risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="0f545-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="0f545-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f545-113">PARAMETERS</span></span>

### <span data-ttu-id="0f545-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f545-114">-DefaultProfile</span></span>
<span data-ttu-id="0f545-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f545-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f545-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f545-116">-Name</span></span>
<span data-ttu-id="0f545-117">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f545-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f545-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f545-118">-ResourceGroupName</span></span>
<span data-ttu-id="0f545-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f545-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f545-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f545-120">-ResourceId</span></span>
<span data-ttu-id="0f545-121">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f545-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f545-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f545-122">CommonParameters</span></span>
<span data-ttu-id="0f545-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f545-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0f545-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f545-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f545-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f545-125">INPUTS</span></span>

### <span data-ttu-id="0f545-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0f545-126">System.String</span></span>


## <span data-ttu-id="0f545-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f545-127">OUTPUTS</span></span>

### <span data-ttu-id="0f545-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f545-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="0f545-129">Note</span><span class="sxs-lookup"><span data-stu-id="0f545-129">NOTES</span></span>

## <span data-ttu-id="0f545-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f545-130">RELATED LINKS</span></span>
