---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 0b70fe2636ae0bc460afd05f9428708c0ff4963b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687425"
---
# <span data-ttu-id="e3cd7-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e3cd7-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="e3cd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cd7-103">Crea un Vault di servizi di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3cd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3cd7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3cd7-105">DESCRIPTION</span></span>
<span data-ttu-id="e3cd7-106">Il cmdlet **New-AzureRmSiteRecoveryVault** crea un Vault di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="e3cd7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-107">EXAMPLES</span></span>

## <span data-ttu-id="e3cd7-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-108">PARAMETERS</span></span>

### <span data-ttu-id="e3cd7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cd7-109">-DefaultProfile</span></span>
<span data-ttu-id="e3cd7-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3cd7-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3cd7-111">-Location</span></span>
<span data-ttu-id="e3cd7-112">Specifica il nome della posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-112">Specifies the geographical location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3cd7-113">-Name</span></span>
<span data-ttu-id="e3cd7-114">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3cd7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3cd7-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cd7-117">CommonParameters</span></span>
<span data-ttu-id="e3cd7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cd7-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3cd7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cd7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-120">INPUTS</span></span>

### <span data-ttu-id="e3cd7-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3cd7-121">None</span></span>
<span data-ttu-id="e3cd7-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e3cd7-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3cd7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3cd7-123">OUTPUTS</span></span>

## <span data-ttu-id="e3cd7-124">Note</span><span class="sxs-lookup"><span data-stu-id="e3cd7-124">NOTES</span></span>

## <span data-ttu-id="e3cd7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3cd7-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3cd7-126">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e3cd7-126">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="e3cd7-127">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="e3cd7-127">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
