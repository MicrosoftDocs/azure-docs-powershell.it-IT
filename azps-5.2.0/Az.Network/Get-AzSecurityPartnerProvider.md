---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzSecurityPartnerProvider.md
ms.openlocfilehash: 8dd23c7eba3dd9306527c11afe5170740a464d2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364402"
---
# <span data-ttu-id="3191a-101">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3191a-101">Get-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="3191a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3191a-102">SYNOPSIS</span></span>
<span data-ttu-id="3191a-103">Ottenere un Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3191a-103">Get an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3191a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3191a-104">SYNTAX</span></span>

### <span data-ttu-id="3191a-105">SecurityPartnerProviderNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3191a-105">SecurityPartnerProviderNameParameterSet (Default)</span></span>
```
Get-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3191a-106">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3191a-106">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Get-AzSecurityPartnerProvider -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3191a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3191a-107">DESCRIPTION</span></span>
<span data-ttu-id="3191a-108">Il cmdlet **Get-AzSecurityPartnerProvider** ottiene un SecurityPartnerProvider di Azure</span><span class="sxs-lookup"><span data-stu-id="3191a-108">The **Get-AzSecurityPartnerProvider** cmdlet gets an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="3191a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3191a-109">EXAMPLES</span></span>

### <span data-ttu-id="3191a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3191a-110">Example 1</span></span>
```powershell
Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```


### <span data-ttu-id="3191a-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3191a-111">Example 2</span></span>
```powershell
$securityPartnerProviderId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/securityPartnerProviderRG/providers/Microsoft.Network/securityPartnerProvider/securityPartnerProvider'
Get-AzSecurityPartnerProvider -ResourceId $securityPartnerProviderId
```

## <span data-ttu-id="3191a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3191a-112">PARAMETERS</span></span>

### <span data-ttu-id="3191a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3191a-113">-DefaultProfile</span></span>
<span data-ttu-id="3191a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3191a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3191a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3191a-115">-Name</span></span>
<span data-ttu-id="3191a-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3191a-116">The resource name.</span></span>

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

### <span data-ttu-id="3191a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3191a-117">-ResourceGroupName</span></span>
<span data-ttu-id="3191a-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3191a-118">The resource group name.</span></span>

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

### <span data-ttu-id="3191a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3191a-119">-ResourceId</span></span>
<span data-ttu-id="3191a-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3191a-120">The resource Id.</span></span>

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

### <span data-ttu-id="3191a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3191a-121">CommonParameters</span></span>
<span data-ttu-id="3191a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3191a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3191a-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3191a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3191a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3191a-124">INPUTS</span></span>

### <span data-ttu-id="3191a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3191a-125">System.String</span></span>

## <span data-ttu-id="3191a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3191a-126">OUTPUTS</span></span>

### <span data-ttu-id="3191a-127">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3191a-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="3191a-128">Note</span><span class="sxs-lookup"><span data-stu-id="3191a-128">NOTES</span></span>

## <span data-ttu-id="3191a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3191a-129">RELATED LINKS</span></span>
