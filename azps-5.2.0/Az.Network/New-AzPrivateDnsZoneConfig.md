---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368129"
---
# <span data-ttu-id="1ddac-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="1ddac-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="1ddac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ddac-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddac-103">Crea la configurazione della zona DNS del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="1ddac-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="1ddac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ddac-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ddac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ddac-105">DESCRIPTION</span></span>
<span data-ttu-id="1ddac-106">Il cmdlet **New-AzPrivateDnsZoneConfig** consente di creare un nuovo oggetto di configurazione della zona DNS che verrà impostato nel gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="1ddac-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="1ddac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ddac-107">EXAMPLES</span></span>

### <span data-ttu-id="1ddac-108">Crea la configurazione della zona DNS</span><span class="sxs-lookup"><span data-stu-id="1ddac-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="1ddac-109">L'esempio precedente crea la zona DNS e quindi crea la configurazione della zona DNS.</span><span class="sxs-lookup"><span data-stu-id="1ddac-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="1ddac-110">`New-AzPrivateDnsZone` cmdlet è stato dimostrato dal modulo AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="1ddac-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="1ddac-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ddac-111">PARAMETERS</span></span>

### <span data-ttu-id="1ddac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ddac-112">-DefaultProfile</span></span>
<span data-ttu-id="1ddac-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ddac-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ddac-114">-Name</span></span>
<span data-ttu-id="1ddac-115">Nome della risorsa univoco all'interno di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ddac-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="1ddac-116">Questo nome può essere usato per accedere alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="1ddac-116">This name can be used to access the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ddac-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="1ddac-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="1ddac-118">ID risorsa della zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="1ddac-118">The resource id of the private dns zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ddac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddac-119">CommonParameters</span></span>
<span data-ttu-id="1ddac-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ddac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddac-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ddac-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddac-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ddac-122">INPUTS</span></span>

### <span data-ttu-id="1ddac-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ddac-123">None</span></span>

## <span data-ttu-id="1ddac-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ddac-124">OUTPUTS</span></span>

### <span data-ttu-id="1ddac-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="1ddac-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="1ddac-126">Note</span><span class="sxs-lookup"><span data-stu-id="1ddac-126">NOTES</span></span>

## <span data-ttu-id="1ddac-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ddac-127">RELATED LINKS</span></span>
