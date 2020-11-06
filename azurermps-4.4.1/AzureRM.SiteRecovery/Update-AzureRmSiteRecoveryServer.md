---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519497"
---
# <span data-ttu-id="61372-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="61372-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="61372-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61372-102">SYNOPSIS</span></span>
<span data-ttu-id="61372-103">Aggiorna un server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="61372-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61372-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61372-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61372-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61372-105">DESCRIPTION</span></span>
<span data-ttu-id="61372-106">Il cmdlet **Update-AzureRmSiteRecoveryServer Aggiorna** un server di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="61372-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="61372-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61372-107">EXAMPLES</span></span>

## <span data-ttu-id="61372-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61372-108">PARAMETERS</span></span>

### <span data-ttu-id="61372-109">-Server</span><span class="sxs-lookup"><span data-stu-id="61372-109">-Server</span></span>
<span data-ttu-id="61372-110">Specifica il server di ripristino del sito che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="61372-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61372-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61372-111">-DefaultProfile</span></span>
<span data-ttu-id="61372-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61372-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61372-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61372-113">CommonParameters</span></span>
<span data-ttu-id="61372-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61372-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61372-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61372-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61372-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61372-116">INPUTS</span></span>

### <span data-ttu-id="61372-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="61372-117">ASRServer</span></span>
<span data-ttu-id="61372-118">Il parametro ' server ' accetta il valore di tipo ' ASRServer ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="61372-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="61372-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61372-119">OUTPUTS</span></span>

## <span data-ttu-id="61372-120">Note</span><span class="sxs-lookup"><span data-stu-id="61372-120">NOTES</span></span>

## <span data-ttu-id="61372-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61372-121">RELATED LINKS</span></span>

[<span data-ttu-id="61372-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="61372-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="61372-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="61372-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
