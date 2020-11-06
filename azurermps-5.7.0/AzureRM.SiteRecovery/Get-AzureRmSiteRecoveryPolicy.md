---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509603"
---
# <span data-ttu-id="eb6a1-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="eb6a1-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="eb6a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6a1-103">Ottiene i criteri di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb6a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb6a1-104">SYNTAX</span></span>

### <span data-ttu-id="eb6a1-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb6a1-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6a1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="eb6a1-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb6a1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="eb6a1-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6a1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb6a1-108">DESCRIPTION</span></span>
<span data-ttu-id="eb6a1-109">Il cmdlet **Get-AzureRmSiteRecoveryPolicy** Ottiene l'elenco dei criteri di protezione del ripristino di Azure site configurati o di uno specifico criterio di protezione per nome.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="eb6a1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb6a1-110">EXAMPLES</span></span>

## <span data-ttu-id="eb6a1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb6a1-111">PARAMETERS</span></span>

### <span data-ttu-id="eb6a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6a1-112">-DefaultProfile</span></span>
<span data-ttu-id="eb6a1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb6a1-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="eb6a1-114">-FriendlyName</span></span>
<span data-ttu-id="eb6a1-115">Specifica il nome descrittivo dei criteri di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6a1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb6a1-116">-Name</span></span>
<span data-ttu-id="eb6a1-117">Specifica il nome del criterio di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-117">Specifies the name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb6a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6a1-118">CommonParameters</span></span>
<span data-ttu-id="eb6a1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6a1-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6a1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6a1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb6a1-121">INPUTS</span></span>

### <span data-ttu-id="eb6a1-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eb6a1-122">None</span></span>
<span data-ttu-id="eb6a1-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="eb6a1-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb6a1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb6a1-124">OUTPUTS</span></span>

### <span data-ttu-id="eb6a1-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="eb6a1-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="eb6a1-126">Note</span><span class="sxs-lookup"><span data-stu-id="eb6a1-126">NOTES</span></span>

## <span data-ttu-id="eb6a1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb6a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb6a1-128">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="eb6a1-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="eb6a1-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="eb6a1-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
