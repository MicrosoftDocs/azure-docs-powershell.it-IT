---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519506"
---
# <span data-ttu-id="2aa1e-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2aa1e-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="2aa1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2aa1e-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa1e-103">Rimuove un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="2aa1e-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aa1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2aa1e-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aa1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aa1e-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa1e-106">Il cmdlet **Remove-AzureRmSiteRecoveryVault** Elimina un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="2aa1e-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2aa1e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2aa1e-107">EXAMPLES</span></span>

## <span data-ttu-id="2aa1e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2aa1e-108">PARAMETERS</span></span>

### <span data-ttu-id="2aa1e-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="2aa1e-109">-Vault</span></span>
<span data-ttu-id="2aa1e-110">Specifica l'oggetto del Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="2aa1e-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa1e-111">-DefaultProfile</span></span>
<span data-ttu-id="2aa1e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa1e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aa1e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa1e-113">CommonParameters</span></span>
<span data-ttu-id="2aa1e-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa1e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa1e-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aa1e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa1e-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2aa1e-116">INPUTS</span></span>

### <span data-ttu-id="2aa1e-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="2aa1e-117">ASRVault</span></span>
<span data-ttu-id="2aa1e-118">Il parametro "Vault" accetta il valore di tipo "ASRVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="2aa1e-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="2aa1e-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2aa1e-119">OUTPUTS</span></span>

## <span data-ttu-id="2aa1e-120">Note</span><span class="sxs-lookup"><span data-stu-id="2aa1e-120">NOTES</span></span>

## <span data-ttu-id="2aa1e-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2aa1e-121">RELATED LINKS</span></span>

[<span data-ttu-id="2aa1e-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2aa1e-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="2aa1e-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2aa1e-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
