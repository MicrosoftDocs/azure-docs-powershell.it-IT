---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687078"
---
# <span data-ttu-id="869bb-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="869bb-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="869bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="869bb-102">SYNOPSIS</span></span>
<span data-ttu-id="869bb-103">Recupera i Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="869bb-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="869bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="869bb-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="869bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="869bb-105">DESCRIPTION</span></span>
<span data-ttu-id="869bb-106">Il cmdlet **Get-AzureRmSiteRecoveryVault** ottiene un elenco dei Vault di ripristino di siti di Azure o di uno specifico Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="869bb-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="869bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="869bb-107">EXAMPLES</span></span>

## <span data-ttu-id="869bb-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="869bb-108">PARAMETERS</span></span>

### <span data-ttu-id="869bb-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="869bb-109">-Name</span></span>
<span data-ttu-id="869bb-110">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="869bb-110">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="869bb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="869bb-111">-ResourceGroupName</span></span>
<span data-ttu-id="869bb-112">Specifica il nome del gruppo di risorse Azure da cui ottenere l'oggetto servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="869bb-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

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

### <span data-ttu-id="869bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869bb-113">-DefaultProfile</span></span>
<span data-ttu-id="869bb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="869bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869bb-115">CommonParameters</span></span>
<span data-ttu-id="869bb-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869bb-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869bb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869bb-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="869bb-118">INPUTS</span></span>

## <span data-ttu-id="869bb-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="869bb-119">OUTPUTS</span></span>

### <span data-ttu-id="869bb-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="869bb-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="869bb-121">Note</span><span class="sxs-lookup"><span data-stu-id="869bb-121">NOTES</span></span>

## <span data-ttu-id="869bb-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="869bb-122">RELATED LINKS</span></span>

[<span data-ttu-id="869bb-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="869bb-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="869bb-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="869bb-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
