---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193735"
---
# <span data-ttu-id="ce1bf-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce1bf-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ce1bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1bf-103">Ottenere un Provider SecurityPartnerProvider di Azure</span><span class="sxs-lookup"><span data-stu-id="ce1bf-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ce1bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce1bf-104">SYNTAX</span></span>

### <span data-ttu-id="ce1bf-105">SecurityPartnerProviderNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce1bf-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce1bf-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce1bf-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce1bf-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce1bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ce1bf-108">Il cmdlet **Get-AzSecurityPartnerProvider** ottiene un provider di Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce1bf-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ce1bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce1bf-109">EXAMPLES</span></span>

### <span data-ttu-id="ce1bf-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce1bf-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="ce1bf-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce1bf-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="ce1bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce1bf-112">PARAMETERS</span></span>

### <span data-ttu-id="ce1bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1bf-113">-DefaultProfile</span></span>
<span data-ttu-id="ce1bf-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce1bf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ce1bf-115">-Name</span></span>
<span data-ttu-id="ce1bf-116">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce1bf-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1bf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce1bf-119">-ResourceId</span></span>
<span data-ttu-id="ce1bf-120">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce1bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1bf-121">CommonParameters</span></span>
<span data-ttu-id="ce1bf-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1bf-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce1bf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1bf-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce1bf-124">INPUTS</span></span>

### <span data-ttu-id="ce1bf-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ce1bf-125">System.String</span></span>

## <span data-ttu-id="ce1bf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce1bf-126">OUTPUTS</span></span>

### <span data-ttu-id="ce1bf-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce1bf-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ce1bf-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce1bf-128">NOTES</span></span>

## <span data-ttu-id="ce1bf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce1bf-129">RELATED LINKS</span></span>
