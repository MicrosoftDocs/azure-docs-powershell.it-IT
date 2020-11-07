---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687434"
---
# <span data-ttu-id="d4404-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d4404-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="d4404-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4404-102">SYNOPSIS</span></span>
<span data-ttu-id="d4404-103">Recupera i Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d4404-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4404-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4404-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4404-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4404-105">DESCRIPTION</span></span>
<span data-ttu-id="d4404-106">Il cmdlet **Get-AzureRmSiteRecoveryVault** ottiene un elenco dei Vault di ripristino di siti di Azure o di uno specifico Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d4404-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="d4404-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4404-107">EXAMPLES</span></span>

## <span data-ttu-id="d4404-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4404-108">PARAMETERS</span></span>

### <span data-ttu-id="d4404-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4404-109">-DefaultProfile</span></span>
<span data-ttu-id="d4404-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4404-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4404-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d4404-111">-Name</span></span>
<span data-ttu-id="d4404-112">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="d4404-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4404-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4404-113">-ResourceGroupName</span></span>
<span data-ttu-id="d4404-114">Specifica il nome del gruppo di risorse Azure da cui ottenere l'oggetto servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d4404-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4404-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4404-115">CommonParameters</span></span>
<span data-ttu-id="d4404-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4404-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4404-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4404-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4404-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4404-118">INPUTS</span></span>

### <span data-ttu-id="d4404-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d4404-119">None</span></span>
<span data-ttu-id="d4404-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d4404-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4404-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4404-121">OUTPUTS</span></span>

### <span data-ttu-id="d4404-122">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="d4404-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="d4404-123">Note</span><span class="sxs-lookup"><span data-stu-id="d4404-123">NOTES</span></span>

## <span data-ttu-id="d4404-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4404-124">RELATED LINKS</span></span>

[<span data-ttu-id="d4404-125">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d4404-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="d4404-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="d4404-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
