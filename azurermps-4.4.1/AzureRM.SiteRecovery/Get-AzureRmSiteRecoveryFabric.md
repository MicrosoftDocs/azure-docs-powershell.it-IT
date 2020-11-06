---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512919"
---
# <span data-ttu-id="450fa-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="450fa-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="450fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="450fa-102">SYNOPSIS</span></span>
<span data-ttu-id="450fa-103">Ottenere le proprietà di un tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="450fa-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="450fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="450fa-104">SYNTAX</span></span>

### <span data-ttu-id="450fa-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="450fa-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="450fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="450fa-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="450fa-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="450fa-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="450fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="450fa-108">DESCRIPTION</span></span>
<span data-ttu-id="450fa-109">Il cmdlet **Get-AzureRmSiteRecoveryFabric** ottiene le proprietà di un determinato tessuto di recupero del sito di Azure o di tutti i tessuti di ripristino di Azure site in un caveau di un servizio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="450fa-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="450fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="450fa-110">EXAMPLES</span></span>

## <span data-ttu-id="450fa-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="450fa-111">PARAMETERS</span></span>

### <span data-ttu-id="450fa-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="450fa-112">-FriendlyName</span></span>
<span data-ttu-id="450fa-113">Specifica il nome descrittivo del tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="450fa-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450fa-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="450fa-114">-Name</span></span>
<span data-ttu-id="450fa-115">Specifica il nome del tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="450fa-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450fa-116">-DefaultProfile</span></span>
<span data-ttu-id="450fa-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="450fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="450fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450fa-118">CommonParameters</span></span>
<span data-ttu-id="450fa-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450fa-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450fa-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450fa-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="450fa-121">INPUTS</span></span>

## <span data-ttu-id="450fa-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="450fa-122">OUTPUTS</span></span>

### <span data-ttu-id="450fa-123">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="450fa-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="450fa-124">Note</span><span class="sxs-lookup"><span data-stu-id="450fa-124">NOTES</span></span>

## <span data-ttu-id="450fa-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="450fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="450fa-126">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="450fa-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="450fa-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="450fa-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
