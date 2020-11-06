---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519356"
---
# <span data-ttu-id="5c515-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5c515-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="5c515-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c515-102">SYNOPSIS</span></span>
<span data-ttu-id="5c515-103">Aggiorna le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5c515-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c515-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c515-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c515-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c515-105">DESCRIPTION</span></span>
<span data-ttu-id="5c515-106">Il cmdlet **Update-AzureRmSiteRecoveryServicesProvider** aggiorna le informazioni ricevute dal provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5c515-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="5c515-107">Puoi usare questo cmdlet per attivare un aggiornamento delle informazioni ricevute dal provider di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5c515-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="5c515-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c515-108">EXAMPLES</span></span>

## <span data-ttu-id="5c515-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c515-109">PARAMETERS</span></span>

### <span data-ttu-id="5c515-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c515-110">-DefaultProfile</span></span>
<span data-ttu-id="5c515-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c515-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c515-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5c515-112">-ServicesProvider</span></span>
<span data-ttu-id="5c515-113">Specifica l'oggetto provider di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5c515-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c515-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c515-114">CommonParameters</span></span>
<span data-ttu-id="5c515-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c515-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c515-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c515-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c515-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c515-117">INPUTS</span></span>

### <span data-ttu-id="5c515-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5c515-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="5c515-119">Il parametro ' ServicesProvider ' accetta il valore di tipo ' ASRRecoveryServicesProvider ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5c515-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="5c515-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c515-120">OUTPUTS</span></span>

## <span data-ttu-id="5c515-121">Note</span><span class="sxs-lookup"><span data-stu-id="5c515-121">NOTES</span></span>

## <span data-ttu-id="5c515-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c515-122">RELATED LINKS</span></span>

[<span data-ttu-id="5c515-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5c515-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="5c515-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5c515-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
