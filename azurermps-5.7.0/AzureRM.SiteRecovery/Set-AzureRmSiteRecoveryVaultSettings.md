---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: b6016857054d2560602c7ea37a508317ff895d37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514095"
---
# <span data-ttu-id="b9e18-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b9e18-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="b9e18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9e18-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e18-103">Imposta il contesto del Vault di ripristino del sito per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="b9e18-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9e18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e18-104">SYNTAX</span></span>

### <span data-ttu-id="b9e18-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9e18-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e18-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e18-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e18-108">Il cmdlet **set-AzureRmSiteRecoveryVaultSettings** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="b9e18-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="b9e18-109">Questo problema non si applica ai Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9e18-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="b9e18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e18-110">EXAMPLES</span></span>

## <span data-ttu-id="b9e18-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9e18-111">PARAMETERS</span></span>

### <span data-ttu-id="b9e18-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-112">-ARSVault</span></span>
<span data-ttu-id="b9e18-113">Specifica un oggetto **ARSVault** .</span><span class="sxs-lookup"><span data-stu-id="b9e18-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e18-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-114">-ASRVault</span></span>
<span data-ttu-id="b9e18-115">Specifica un oggetto **ASRVault** .</span><span class="sxs-lookup"><span data-stu-id="b9e18-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e18-116">-DefaultProfile</span></span>
<span data-ttu-id="b9e18-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9e18-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e18-118">CommonParameters</span></span>
<span data-ttu-id="b9e18-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e18-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e18-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e18-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e18-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9e18-121">INPUTS</span></span>

### <span data-ttu-id="b9e18-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-122">ARSVault</span></span>
<span data-ttu-id="b9e18-123">Il parametro ' ARSVault ' accetta il valore di tipo ' ARSVault ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b9e18-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="b9e18-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="b9e18-124">ASRVault</span></span>
<span data-ttu-id="b9e18-125">Il parametro ' ASRVault ' accetta il valore di tipo ' ASRVault ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b9e18-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="b9e18-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e18-126">OUTPUTS</span></span>

### <span data-ttu-id="b9e18-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b9e18-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b9e18-128">Note</span><span class="sxs-lookup"><span data-stu-id="b9e18-128">NOTES</span></span>

## <span data-ttu-id="b9e18-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e18-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9e18-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b9e18-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
