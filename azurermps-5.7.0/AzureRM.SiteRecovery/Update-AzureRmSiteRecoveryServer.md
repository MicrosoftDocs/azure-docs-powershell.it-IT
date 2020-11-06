---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: ce38334d3ae37864d53830970d895e29755f6687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507920"
---
# <span data-ttu-id="8a7a9-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8a7a9-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="8a7a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7a9-103">Aggiorna un server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8a7a9-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a7a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a7a9-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a7a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7a9-106">Il cmdlet **Update-AzureRmSiteRecoveryServer Aggiorna** un server di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7a9-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="8a7a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a7a9-107">EXAMPLES</span></span>

## <span data-ttu-id="8a7a9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a7a9-108">PARAMETERS</span></span>

### <span data-ttu-id="8a7a9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7a9-109">-DefaultProfile</span></span>
<span data-ttu-id="8a7a9-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a7a9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a7a9-111">-Server</span><span class="sxs-lookup"><span data-stu-id="8a7a9-111">-Server</span></span>
<span data-ttu-id="8a7a9-112">Specifica il server di ripristino del sito che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="8a7a9-112">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a7a9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7a9-113">CommonParameters</span></span>
<span data-ttu-id="8a7a9-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a7a9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7a9-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7a9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7a9-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a7a9-116">INPUTS</span></span>

### <span data-ttu-id="8a7a9-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="8a7a9-117">ASRServer</span></span>
<span data-ttu-id="8a7a9-118">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8a7a9-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="8a7a9-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a7a9-119">OUTPUTS</span></span>

## <span data-ttu-id="8a7a9-120">Note</span><span class="sxs-lookup"><span data-stu-id="8a7a9-120">NOTES</span></span>

## <span data-ttu-id="8a7a9-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a7a9-121">RELATED LINKS</span></span>

[<span data-ttu-id="8a7a9-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8a7a9-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="8a7a9-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8a7a9-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
