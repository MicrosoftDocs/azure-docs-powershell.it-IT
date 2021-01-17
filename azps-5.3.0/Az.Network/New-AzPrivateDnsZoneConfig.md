---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatednszoneconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateDnsZoneConfig.md
ms.openlocfilehash: b80889f1838945f6ba119f539c5badd59b43de61
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474512"
---
# <span data-ttu-id="8500a-101">New-AzPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="8500a-101">New-AzPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="8500a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8500a-102">SYNOPSIS</span></span>
<span data-ttu-id="8500a-103">Crea la configurazione della zona DNS del gruppo di aree private DNS.</span><span class="sxs-lookup"><span data-stu-id="8500a-103">Creates DNS zone configuration of the private dns zone group.</span></span>

## <span data-ttu-id="8500a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8500a-104">SYNTAX</span></span>

```
New-AzPrivateDnsZoneConfig -Name <String> [-PrivateDnsZoneId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8500a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8500a-105">DESCRIPTION</span></span>
<span data-ttu-id="8500a-106">Il cmdlet **New-AzPrivateDnsZoneConfig** consente di creare un nuovo oggetto di configurazione della zona DNS che verrà impostato nel gruppo di aree DNS.</span><span class="sxs-lookup"><span data-stu-id="8500a-106">The **New-AzPrivateDnsZoneConfig** cmdlet enables you to create a new DNS zone configuration object which will be set on DNS zone group.</span></span>

## <span data-ttu-id="8500a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8500a-107">EXAMPLES</span></span>

### <span data-ttu-id="8500a-108">Crea la configurazione della zona DNS</span><span class="sxs-lookup"><span data-stu-id="8500a-108">Creates DNS zone configuration</span></span>
```powershell
PS C:\> $dnsZone = New-AzPrivateDnsZone -ResourceGroupName "rg" -Name "test.vault.azure.com"
PS C:\> $config = New-AzPrivateDnsZoneConfig -Name "test-vault-azure-com" -PrivateDnsZoneId $dnsZone.ResourceId
```

<span data-ttu-id="8500a-109">L'esempio precedente crea la zona DNS e quindi crea la configurazione della zona DNS.</span><span class="sxs-lookup"><span data-stu-id="8500a-109">The above example creates DNS zone and then creates DNS zone configuration.</span></span> <span data-ttu-id="8500a-110">`New-AzPrivateDnsZone` cmdlet è stato dimostrato dal modulo AZ. PrivateDns.</span><span class="sxs-lookup"><span data-stu-id="8500a-110">`New-AzPrivateDnsZone` cmdlet is proveded by module Az.PrivateDns.</span></span>

## <span data-ttu-id="8500a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8500a-111">PARAMETERS</span></span>

### <span data-ttu-id="8500a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8500a-112">-DefaultProfile</span></span>
<span data-ttu-id="8500a-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8500a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8500a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8500a-114">-Name</span></span>
<span data-ttu-id="8500a-115">Nome della risorsa univoco all'interno di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8500a-115">Name of the resource that is unique within a resource group.</span></span>
<span data-ttu-id="8500a-116">Questo nome può essere usato per accedere alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="8500a-116">This name can be used to access the resource.</span></span>

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

### <span data-ttu-id="8500a-117">-PrivateDnsZoneId</span><span class="sxs-lookup"><span data-stu-id="8500a-117">-PrivateDnsZoneId</span></span>
<span data-ttu-id="8500a-118">ID risorsa della zona DNS privata.</span><span class="sxs-lookup"><span data-stu-id="8500a-118">The resource id of the private dns zone.</span></span>

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

### <span data-ttu-id="8500a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8500a-119">CommonParameters</span></span>
<span data-ttu-id="8500a-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8500a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8500a-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8500a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8500a-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8500a-122">INPUTS</span></span>

### <span data-ttu-id="8500a-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8500a-123">None</span></span>

## <span data-ttu-id="8500a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8500a-124">OUTPUTS</span></span>

### <span data-ttu-id="8500a-125">Microsoft. Azure. Commands. Network. Models. PSPrivateDnsZoneConfig</span><span class="sxs-lookup"><span data-stu-id="8500a-125">Microsoft.Azure.Commands.Network.Models.PSPrivateDnsZoneConfig</span></span>

## <span data-ttu-id="8500a-126">Note</span><span class="sxs-lookup"><span data-stu-id="8500a-126">NOTES</span></span>

## <span data-ttu-id="8500a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8500a-127">RELATED LINKS</span></span>
